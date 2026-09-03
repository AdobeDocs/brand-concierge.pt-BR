---
title: Guia do desenvolvedor e de personalização
description: Saiba como instalar o Brand Concierge Web SDK e o Web Client, personalizar a aparência e o conteúdo, lidar com eventos do lado do cliente e exportar dados de conversação.
role: Developer,Admin
level: Experienced
toc: true
source-git-commit: 13db0491c987a08492820ac216e20feb87f30e44
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 4%

---


# Guia do desenvolvedor e de personalização {#developer-customization-guide}

Este guia é para desenvolvedores e equipes técnicas que implementam ou personalizam uma implantação do Brand Concierge. Ela aborda a instalação do Web SDK e do Web Client, a personalização da aparência e do conteúdo, a escuta de eventos do lado do cliente por meio de funções de retorno de chamada e a exportação de dados de conversação para relatórios.

## Instalação do Web SDK e do Web Client {#installation}

### Pré-requisitos {#prerequisites}

* A organização é um cliente da Adobe Experience Platform (AEP).
* A página é instrumentada com o Adobe Experience Platform Web SDK.
* A ID de sequência de dados usada na página é ativada para o Brand Concierge.

### Etapa 1: inserir o Web SDK {#inject-web-sdk}

Adicione o seguinte à seção `<head>` da página:

```html
<script>
  !(function (n, o) {
    o.forEach(function (o) {
      n[o] ||
        ((n.__alloyNS = n.__alloyNS || []).push(o),
        (n[o] = function () {
          var u = arguments;
          return new Promise(function (i, l) {
            n[o].q.push([i, l, u]);
          });
        }),
        (n[o].q = []));
    });
  })(window, ["alloy"]);
</script>
<script src="https://cdn1.adoberesources.net/alloy/2.31.1/alloy.min.js"></script>
```

### Etapa 2: Inserir o cliente da Web {#inject-web-client}

Adicione o seguinte após o script do Web SDK, ainda na seção `<head>`:

```html
<script src="https://experience.adobe.net/solutions/experience-platform-brand-concierge-web-agent/static-assets/main.js"></script>
```

### Etapa 3: configurar o Web SDK {#configure-web-sdk}

Chame `alloy("configure", ...)` com os valores da sua organização no lugar dos espaços reservados abaixo:

```javascript
alloy("configure", {
  defaultConsent: "in",
  edgeDomain: "edge.adobedc.net",
  edgeBasePath: "ee",
  datastreamId: "YOUR_DATASTREAM_ID",
  orgId: "YOUR_IMS_ORG_ID",
  debugEnabled: true,
  idMigrationEnabled: false,
  thirdPartyCookiesEnabled: false,
  prehidingStyle: ".personalization-container { opacity: 0 !important }",
  onBeforeEventSend: (options) => {
    const x = options.xdm;
    const params = new URLSearchParams(window.location.search);
    const titleParam = params.get("title");
    if (titleParam) {
      x.web.webPageDetails.name = titleParam;
    } else {
      x.web.webPageDetails.name = "default-page";
    }
    return true;
  }
});
alloy("sendEvent", {});
```

| Campo | Descrição |
|---|---|
| `datastreamId` | A ID da sequência de dados configurada para esta página, ativada para o Brand Concierge. |
| `orgId` | A ID da organização IMS em que o concierge está configurado. |
| `debugEnabled` | Defina como `false` na produção depois que a integração for verificada. |
| `prehidingStyle` | CSS aplicado antes do carregamento do conteúdo de personalização, para evitar um flash de conteúdo não estilizado. |
| `onBeforeEventSend` | Gancho opcional para modificar a carga XDM antes de ser enviada — geralmente usado para definir o nome ou o contexto da página. |

### Etapa 4: inicializar o Web Client {#initialize-web-client}

Após a chamada de configuração do Web SDK, inicialize o Web Client chamando a API de inicialização:

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "alloy",
  stylingConfigurations: window.styleConfigurations,
  selector: "#brand-concierge-mount"
});
```

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `instanceName` | string | Sim | O nome da instância do Web SDK. |
| `stylingConfigurations` | objeto JSON | Sim | A configuração de estilo do Web Client (consulte [Personalização visual e de conteúdo](#customization)). |
| `selector` | string | Sim | Seletor de CSS para o elemento HTML no qual o Cliente da Web é montado. |
| `onEvent` | função | Não | Retorno de chamada para eventos do lado cliente (consulte [Eventos do lado cliente e funções de retorno de chamada](#events)). |

## Personalização visual e de conteúdo {#customization}

O objeto `stylingConfigurations` passado para `bootstrap()` controla a aparência, o comportamento e o texto em todo o Web Client. Ele é organizado em várias áreas.

### Metadados {#metadata}

```javascript
"metadata": {
  "brandName": "Your Brand",
  "version": "1.0.0",
  "language": "en-US",
  "namespace": "brand-concierge"
}
```

### Comportamento {#behavior}

Controla o comportamento funcional de recursos de bate-papo individuais.

```javascript
"behavior": {
  "input": {
    "enableVoiceInput": true
  },
  "chat": {
    "messageAlignment": "left",
    "messageWidth": "80%"
  },
  "privacyNotice": {
    "title": "Privacy Notice",
    "text": "By using this automated chatbot, you consent that any personal information you provide in the chat may be collected, used, analyzed, disclosed, and retained by Adobe and its service providers, in accordance with the Adobe Privacy Policy. Please do not enter any sensitive personal information (e.g., financial or health data)."
  },
  "disclaimer": {
    "attachWithInput": true
  },
  "chatTranscript": {
    "enabled": true,
    "maxSessions": 1,
    "maxMessagesPerSession": 20,
    "cleanupInterval": 24
  },
  "meetingForm": {
    "fieldsPerRow": 2,
    "title": { "text": "Schedule meeting", "alignment": "left" },
    "subtitle": { "text": "I'd be happy to help you schedule a meeting! Please fill out the form below, and we'll follow up with a calendar to confirm your day and time.", "alignment": "left" },
    "buttons": {
      "submit": { "text": "Schedule meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  },
  "calendarWidget": {
    "title": { "text": "Book a meeting", "alignment": "left" },
    "subtitle": { "text": "Thanks! Here's a calendar where you can choose a time that works best for your schedule:", "alignment": "left" },
    "postTitle": { "text": "Once confirmed, you'll receive a calendar invite with all the details.", "alignment": "left" },
    "buttons": {
      "confirm": { "text": "Schedule a meeting", "alignment": "left" },
      "cancel": { "text": "Cancel", "alignment": "left" }
    }
  }
}
```

### Aviso {#disclaimer}

```javascript
"disclaimer": {
  "text": "AI responses may be inaccurate or misleading. Be sure to double check answers and sources."
}
```

### Cadeias de texto {#text-strings}

Toda cópia voltada para o usuário pode ser substituída por meio do objeto `text`. Chaves comuns:

| Chave | Finalidade |
|---|---|
| `welcome.heading` / `welcome.subheading` | Título e subtexto da tela de boas-vindas |
| `input.placeholder` | Texto do espaço reservado do campo de entrada |
| `input.messageInput.aria` / `input.send.aria` / `input.mic.aria` | Rótulos de acessibilidade para controles de entrada |
| `error.network` / `error.general` | Mensagens de erro exibidas para o visitante |
| `loading.message` | Texto exibido enquanto uma resposta é gerada |
| `feedback.dialog.title.positive` / `.negative` | Títulos da caixa de diálogo de comentários |
| `feedback.dialog.question.positive` / `.negative` | Texto do prompt da caixa de diálogo de feedback |
| `feedback.toast.success` | Notificação do sistema de confirmação após o envio do feedback |
| `feedback.thumbsUp.aria` / `feedback.thumbsDown.aria` | Rótulos de acessibilidade para botões de feedback |

### Matrizes {#arrays}

Listas de conteúdo configuráveis:

```javascript
"arrays": {
  "welcome.examples": [
    {
      "text": "I want to edit and enhance my photos",
      "image": "https://example.com/idea-1.png",
      "backgroundColor": "#66BFE7"
    }
  ],
  "feedback.positive.options": [
    "Helpful and relevant recommendations",
    "Clear and easy to understand",
    "Friendly and conversational tone",
    "Visually appealing presentation",
    "Other"
  ],
  "feedback.negative.options": [
    "Not helpful or relevant",
    "Confusing or unclear",
    "Too formal or robotic",
    "Poor visual presentation",
    "Other"
  ]
}
```

### Ativos {#assets}

```javascript
"assets": {
  "icons": {
    "company": "<svg>...</svg>"
  }
}
```

### Tema {#theme}

Propriedades personalizadas de CSS que controlam cores, fontes e layout:

```css
"theme": {
  "--color-primary": "#1473e6",
  "--color-primary-hover": "#0056b3",
  "--color-button-primary": "#3B63FB",
  "--color-accent": "#9085ED",
  "--color-button-submit": "#4759e6",
  "--color-button-submit-hover": "#3a4bce",
  "--color-message-user": "#1473e6",
  "--font-family": "'Adobe Clean', adobe-clean, 'Trebuchet MS', sans-serif",
  "--main-container-background": "linear-gradient(135deg, #66ccff, #cc99ff, #ffcc99, #ccff99)",
  "--submit-button-fill-color": "white",
  "--card-text-background": "var(--color-background)",
  "--card-text-border-radius": "var(--border-radius-card)",
  "--message-concierge-link-decoration": "underline",
  "--message-max-width": "100%"
}
```

## Eventos do lado do cliente e funções de retorno de chamada {#events}

O sistema de retorno de chamada do evento permite que uma página observe eventos de ciclo de vida do cliente da Web, interações do usuário, respostas, feedback e erros em tempo real, úteis para enviar dados de engajamento para a Adobe Analytics, o Google Analytics ou outros sistemas de terceiros.

### Principais características {#key-characteristics}

* **Retorno de chamada único** — uma função `onEvent` recebe todos os tipos de evento, diferenciados por `event.eventType`.
* **Somente leitura** — os dados do evento são um instantâneo clonado e não podem ser usados para modificar o comportamento do cliente.
* **Isolado por erro** — as exceções lançadas dentro do retorno de chamada são capturadas e registradas em log; elas não interrompem o Web Client.
* **Registrado via`bootstrap()`** — passado da mesma forma que `onBeforeEventSend`.

### Início rápido {#quick-start}

```javascript
window.adobe.concierge.bootstrap({
  instanceName: "my-instance",
  selector: "#brand-concierge-mount",
  stylingConfigurations: { /* ... */ },
  onEvent: (event) => {
    console.log(event.eventType, event.timestamp, event.data);
  }
});
```

### Filtrar por tipo de evento {#filtering}

```javascript
onEvent: (event) => {
  switch (event.eventType) {
    case "query:submitted":
      console.log("User query:", event.data.query);
      break;
    case "response:completed":
      console.log("Response received:", event.data.conversationId);
      break;
    case "card:clicked":
      console.log("Card clicked:", event.data.element.entity_info.productName);
      break;
    case "error:occurred":
      console.log("Error:", event.data.errorMessage);
      break;
  }
}
```

### Tipos de evento {#event-types}

| Tipo de evento | Valor | Categoria | Quando ele dispara |
|---|---|---|---|
| `WEBCLIENT_INITIALIZED` | `webclient:initialized` | Ciclo de vida | O cliente conclui a inicialização (montado em DOM, conteúdo carregado) |
| `QUERY_SUBMITTED` | `query:submitted` | Interação do usuário | O usuário envia uma mensagem (digitada ou da sugestão) |
| `PROMPT_SUGGESTION_CLICKED` | `promptSuggestion:clicked` | Interação do usuário | O usuário clica em uma pílula de sugestão |
| `CARD_CLICKED` | `card:clicked` | Interação do usuário | O usuário clica em um cartão |
| `HISTORY_CLEARED` | `history:cleared` | Interação do usuário | O usuário limpa o histórico do chat |
| `RESPONSE_STARTED` | `response:started` | Resposta | A primeira parte de transmissão chega da API |
| `RESPONSE_COMPLETED` | `response:completed` | Resposta | A resposta completa é recebida e renderizada |
| `CARDS_RENDERED` | `cards:rendered` | Resposta | Renderização de acabamento de cartões (imagem única ou carrossel) |
| `FEEDBACK_SUBMITTED` | `feedback:submitted` | Feedback | O usuário envia um formulário de feedback (miniaturas para cima/para baixo com detalhes) |
| `ERROR_OCCURRED` | `error:occurred` | Erro | Erro (rede, API ou tempo de execução) |

### Eventos de ciclo de vida {#lifecycle-events}

`webclient:initialized` é acionado depois que o cliente é totalmente inicializado: conteúdo carregado, CSS inserido, interface do usuário de chat renderizada no DOM.

```json
{
  "eventType": "webclient:initialized",
  "timestamp": 1741638123789,
  "data": {
    "instanceName": "my-instance"
  }
}
```

### Eventos de interação do usuário {#user-interaction-events}

`query:submitted` é acionado quando o usuário envia uma mensagem, seja digitada, de uma sugestão de prompt ou de uma opção de widget.

```json
{
  "eventType": "query:submitted",
  "timestamp": 1741638124000,
  "data": {
    "query": "What photo editing tools do you offer?"
  }
}
```

`promptSuggestion:clicked` é acionado quando o usuário clica em uma pílula de sugestão de prompt. Dispara *antes* do evento `query:submitted` subsequente.

```json
{
  "eventType": "promptSuggestion:clicked",
  "timestamp": 1741638124100,
  "data": {
    "suggestion": "Tell me more about Photoshop"
  }
}
```

`card:clicked` acionado quando o usuário clica em um cartão.

```json
{
  "eventType": "card:clicked",
  "timestamp": 1741638124200,
  "data": {
    "element": {
      "entity_info": {
        "productName": "Adobe Photoshop",
        "productDescription": "Photo editing software",
        "productPageURL": "https://www.adobe.com/br/products/photoshop.html",
        "productImageURL": "https://example.com/photoshop.png"
      }
    }
  }
}
```

`history:cleared` é acionado quando o usuário clica no botão clear-chat-history.

```json
{
  "eventType": "history:cleared",
  "timestamp": 1741638124400,
  "data": {}
}
```

### Eventos de resposta {#response-events}

`response:started` é acionado quando a primeira parte de transmissão chega da API.

```json
{
  "eventType": "response:started",
  "timestamp": 1741638125000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`response:completed` acionado quando a resposta completa é recebida.

```json
{
  "eventType": "response:completed",
  "timestamp": 1741638126000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456"
  }
}
```

`cards:rendered` é acionado depois que os cartões são renderizados no DOM. Dispara separadamente de `response:completed` e indica o modo de exibição usado.

```json
{
  "eventType": "cards:rendered",
  "timestamp": 1741638126100,
  "data": {
    "element": [
      { "entity_info": { "productName": "Adobe Photoshop" } },
      { "entity_info": { "productName": "Adobe Illustrator" } }
    ],
    "displayMode": "carousel"
  }
}
```

### Eventos de feedback {#feedback-events}

`feedback:submitted` é acionado quando o usuário conclui e envia um formulário de feedback (após miniaturas para cima/para baixo).

```json
{
  "eventType": "feedback:submitted",
  "timestamp": 1741638127000,
  "data": {
    "conversationId": "conv-abc-123",
    "interactionId": "int-xyz-456",
    "feedbackType": "negative",
    "selectedOptions": ["Incorrect information", "Not relevant"],
    "notes": "The response did not address my question about pricing."
  }
}
```

### Eventos de erro {#error-events}

`error:occurred` é acionado quando o cliente encontra um erro de rede, API ou tempo de execução.

```json
{
  "eventType": "error:occurred",
  "timestamp": 1741638128000,
  "data": {
    "errorMessage": "Something went wrong. Please try again."
  }
}
```

### Estrutura do objeto do evento {#event-object-structure}

Todos os eventos compartilham a mesma forma de nível superior:

```typescript
interface BrandConciergeEvent {
  eventType: string;  // e.g. "query:submitted"
  timestamp: number;  // Unix epoch, milliseconds
  data: object;       // Event-specific payload
}
```

### Referência do tipo de dados: Elemento (cartão de produto) {#element-reference}

```typescript
interface Element {
  id?: string;
  type?: string;
  entity_info: {
    productName: string;
    productDescription: string;
    description: string;
    productPageURL: string;
    details: string;
    backgroundColor: string;
    learningResource: string;
    productImageURL: string;
    logo: string;
    variants?: Record<string, ElementVariant>;
    primary: ElementAction;
    secondary: ElementAction;
  };
}

interface ElementAction {
  label: string;
  url: string;
}
```

### Práticas recomendadas {#best-practices}

* **Usar para análise e monitoramento.** Acompanhe o envolvimento, os padrões de consulta e os interesses do produto; encaminhe `error:occurred` para um serviço de rastreamento de erros; rastreie cliques de cartão para análise de conversão.
* **Manter o retorno de chamada rápido.** Ela é executada de forma síncrona no thread principal, portanto, evite bloquear chamadas de rede:

```javascript
// Good — fire and forget
onEvent: (event) => {
  navigator.sendBeacon("/analytics", JSON.stringify(event));
}

// Avoid — blocking network call
onEvent: async (event) => {
  await fetch("/analytics", { body: JSON.stringify(event) });
}
```

* **Não confiar na ordem estrita de eventos** para máquinas de estado. Os eventos são acionados em uma sequência lógica, mas use `conversationId` e `interactionId` para correlacionar eventos relacionados em vez de assumir a ordem.
* **Manipular erros dentro do seu próprio retorno de chamada.** O cliente isola e registra erros de retorno de chamada, mas erros não tratados dentro do retorno de chamada ainda podem perder dados do Analytics:

```javascript
onEvent: (event) => {
  try {
    myAnalytics.track(event);
  } catch (e) {
    console.warn("Analytics tracking failed", e);
  }
}
```

## Exportar conversas usando o Serviço de consulta da AEP {#export-conversations}

A Brand Concierge grava dados de conversas — solicitações, respostas e feedback — nos conjuntos de dados da Adobe Experience Platform (AEP). Você pode consultá-los diretamente com o Serviço de consulta (SQL) para criar relatórios personalizados.

### Localizar o conjunto de dados e o nome da tabela {#find-dataset}

1. Abra o Adobe Experience Platform.

1. Vá para **[!UICONTROL Conjuntos de dados]**.

1. Procure por `cja_brand_concierge` para listar os conjuntos de dados relacionados ao Brand Concierge.

1. Abra o conjunto de dados necessário (por exemplo, respostas em comparação a outros fluxos, se existir mais de um).

1. Na exibição de detalhes do conjunto de dados, localize o **[!UICONTROL Nome da tabela]** usado pelo Serviço de Consulta e inspecione os dados de amostra ou visualização para confirmar as colunas (prompts, respostas, feedback, carimbos de data e hora e assim por diante).

>[!NOTE]
>
>Os nomes das tabelas estão vinculados a cada conjunto de dados e diferem por ambiente e sandbox. Se você tiver várias sandboxes ou implantações, repita essas etapas na sandbox correta para que o nome da tabela corresponda ao local em que os dados são gravados.

### Exemplo de consulta {#example-query}

```sql
SELECT *
FROM cja_brand_concierge_responses_dataset_5f5105bd_1c38_4ebc_8505_bd
WHERE timestamp >= TIMESTAMP '2026-03-16 00:00:00'
  AND timestamp <= NOW()
ORDER BY timestamp ASC;
```

>[!IMPORTANT]
>
>O nome da tabela acima é apenas uma ilustração. Não codifique-o. Confirme o nome real da tabela para seu conjunto de dados na AEP primeiro (consulte [Localizar o conjunto de dados e o nome da tabela](#find-dataset)) e ajuste o filtro de tempo, a ordem de classificação ou outras cláusulas para corresponder às suas necessidades de relatório. Execute a consulta no fluxo de trabalho do Serviço de consulta de sua organização (interface, API ou cliente conectado) usando a mesma sandbox do conjunto de dados.

### Executar uma consulta na interface do usuário do Serviço de consulta {#run-query-ui}

Se você precisar de uma extração manual de dados para relatórios, a interface do usuário do Serviço de consulta fornece uma maneira de executar e baixar os resultados diretamente:

1. No Adobe Experience Platform, vá para **[!UICONTROL Queries]**.

1. Insira a consulta no editor e clique em **[!UICONTROL Executar consulta]**.

1. Os resultados aparecem na guia **[!UICONTROL Resultados]** abaixo do editor após a conclusão da consulta. Você pode baixar os resultados de lá.

### Leitura adicional {#further-reading}

* [Documentação da API de Serviço de Consulta](https://experienceleague.adobe.com/pt-br/docs/experience-platform/query/home){target="_blank"} — a referência oficial da Adobe para comportamento, limites, autenticação e caminhos de API do Serviço de Consulta, que mudam com o tempo, independentemente deste guia.
