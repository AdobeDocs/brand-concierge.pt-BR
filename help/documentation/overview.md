---
title: Documentação do produto
description: Saiba como configurar e usar os principais recursos do Brand Concierge.
role: User,Admin
level: Beginner
source-git-commit: 2c3f3d009d8fef3eaf5bf32d73672eeda7ba05c8
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 1%

---

# Ajuda do Brand Concierge

Saiba como configurar e usar os principais recursos do Brand Concierge. Encontre respostas para perguntas comuns sobre configuração, integração de dados, privacidade, personalização, medição de desempenho e requisitos técnicos.

## Recursos principais {#key-features}

O Brand Concierge tem vários recursos principais, incluindo:

* **Integração guiada:** siga uma configuração passo a passo para obter conhecimento, habilidades e expressão de marca.
* **Integração de conhecimento:** carregue e gerencie fontes como arquivos CSV com links de site.
* **Configurar habilidades** Integre habilidades, como consultoria de produto.
* **Marca de controle:** Ajuste a voz, o tom e a duração da resposta para atender ao padrão e à abordagem de sua marca específica.
* **Visualizar e iterar:** use uma interface de visualização abrangente para simular conversas e realizar ajustes ao vivo.
* **Sistema de comentários:** use um sistema de comentários que permita que os usuários forneçam classificações com miniaturas para cima ou para baixo, além de formulários de comentários detalhados que cubram a cobertura da resposta, o tom, a qualidade e os recursos.
* **Painel do Analytics:** aproveite um painel de análise desenvolvido pelo Customer Journey Analytics para métricas como conversas, sentimento e envolvimento.

## Introdução {#getting-started}

Você pode acessar o Brand Concierge no painel do Adobe Experience Cloud. Em um nível superior, você executa essas tarefas na apresentação da Página inicial:

1. [Criar um concierge](#homepage)
1. [Adicionar fontes de conhecimento](#knowledge-sources)
1. [Configurar habilidades](#skills-configuration)
1. [Especifique sua Expressão de Marca](#brand-expression).

Para assistir a um tutorial em vídeo, consulte [Criar sua primeira concierge](../getting-started/create-first-concierge.md)

As seções a seguir descrevem cada tarefa e as opções da interface em detalhes.

## Criar um concierge {#homepage}

A página inicial do Brand Concierge foi projetada para facilitar o uso e aumentar a eficiência, orientando você pelas etapas essenciais de configuração com uma apresentação dedicada para o usuário pela primeira vez. Um banner principal destacado descreve as principais ações, como especificar o nome e o propósito do concierge, adicionar fontes de conhecimento, configurar habilidades relevantes e definir a expressão da marca.

À medida que você avança, um rastreador visual exibe claramente quais componentes da configuração foram concluídos e destaca as tarefas restantes. Para apoiar ainda mais seus esforços, a Página inicial apresenta uma seção inspiradora com vídeos e demonstrações de recursos de concierge, como recomendações de produtos. Você também tem acesso rápido à documentação do Experience League para obter insights técnicos mais detalhados.

Quando a configuração estiver concluída, um resumo da configuração fornecerá uma visão abrangente dos seus detalhes, organizada com guias para facilitar ajustes e refinamentos contínuos.

**Elementos-chave**

* **Apresentação de usuário pela primeira vez**: um banner principal com etapas para configurar sua concierge (nome/finalidade, fontes de conhecimento, habilidades, expressão de marca).
* **Rastreador de Progresso**: indicadores visuais de componentes de instalação concluídos vs. pendentes.
* **Seção Inspiradora**: vídeos e demonstrações que mostram recursos de concierge (por exemplo, recomendações de produtos).
* **Links de documentação**: acesso rápido aos recursos do Experience League para obter insights técnicos mais profundos.
* **Resumo da Configuração**: exibição pós-configuração de todos os detalhes, com guias para refinamento.

**Para criar uma concierge**

1. Navegue até o banner de apresentação e clique em **[!UICONTROL Introdução]**.
1. Insira um nome para a sua portaria e defina sua finalidade (por exemplo, _Recomendar produtos personalizados_).
1. Siga as etapas guiadas para continuar.
1. Quando a configuração for concluída, retorne à Página inicial para monitorar ou editar sua concierge.

>[!TIP]
>
>O Brand Concierge salva seu progresso automaticamente. Uma configuração incompleta pode limitar a funcionalidade, mas não bloqueará as tentativas de visualização.

### Fontes de conhecimento {#knowledge-sources}

As [!UICONTROL Fontes de Conhecimento] ajudam você a gerenciar as fontes de dados que alimentam as respostas do seu concierge. Você pode acessar as [!UICONTROL Fontes de Conhecimento] após carregar os arquivos iniciais. [!UICONTROL Fontes de Conhecimento] tem vários elementos-chave a serem considerados, como:

* **Lista do Source:** Exibe todos os itens carregados, como arquivos CSV com links de site, e indica seu status como processado ou pendente.
* **Interface de Carregamento:** permite que você arraste e solte ou procure arquivos CSV que contenham URLs, que o sistema rastreará para extrair conhecimento.
* **Opções de Conexão:** permite que você vincule fontes de conhecimento específicas a habilidades relevantes para uso mais direcionado.

**Para adicionar uma fonte de conhecimento**

1. Na Página inicial, clique em **[!UICONTROL Fontes de conhecimento]**.

1. Nomeie a fonte de conhecimento.

1. Clique em **[!UICONTROL Adicionar]** para carregar um arquivo CSV.

   Certifique-se de que inclua uma coluna para URLs de site.

1. Aguarde alguns momentos para o processamento.

   Essa etapa é resolvida rapidamente como atualizações de status em tempo real.

1. Depois de adicionado, retorne à Página inicial.

   Nesse ponto, você deve ver a nova fonte adicionada à Página inicial.

   Use a Página inicial para editar ou excluir suas fontes de conhecimento, conforme necessário. Você também pode reconectar uma fonte de conhecimento se ocorrerem alterações.

### Configurar habilidades {#skills-configuration}

Use a interface da [!UICONTROL Configuração de Habilidades] para modelar a experiência de sua concierge, configurando habilidades como o **Product Advisory**. Responda ao questionário para fornecer as entradas que os consultores da Adobe usarão posteriormente para engenharia de prompt. A Configuração de habilidades tem vários elementos-chave a serem considerados, como:

* **Seletor de habilidades:** você pode escolher entre as habilidades disponíveis, como o Product Advisory, para fazer recomendações de produtos.
* **Questionário:** você preencherá uma série de prompts para fornecer conhecimento sobre o produto, regras de negócios, palavras-chave a serem evitadas e conexões de origem.
* **Visualização:** você tem a opção de fazer ajustes ao vivo e ver como seus ajustes afetam as respostas, com links para a página de visualização.
* **Habilitar Reserva de Reunião:** Você pode habilitar os visitantes a agendar reuniões diretamente com representantes comerciais.

**Para configurar habilidades**

1. Navegue até o rastreador de progresso na Página inicial e clique em **[!UICONTROL Configurar habilidades]**.
1. Selecione uma habilidade (por exemplo, Aviso do produto).
1. Responda às perguntas de configuração subsequentes.

   Exemplos de perguntas incluem: _O que o concierge deve saber sobre os produtos?_, _Que regras comerciais devem ser seguidas?_, _Quais palavras-chave devem ser evitadas?_

1. Conectar [fontes de conhecimento](#knowledge-sources) relevantes.
1. Habilitar recursos adicionais (reserva de reunião).
1. Enviar para processamento.

### Expressão da marca {#brand-expression}

Você pode usar a interface da _[!UICONTROL Expressão da marca]_ para personalizar a personalidade e o estilo das respostas de seus porteiros. Você pode acessar a Expressão da marca nos estágios de configuração ou na barra lateral de visualização para alterações em andamento.

Com o Brand Expression, você pode usar controles deslizantes para personalizar as configurações de voz e tom do concierge. Você pode selecionar entre opções como &quot;Amigável&quot;, &quot;Profissional&quot; e &quot;Energético&quot;. Além disso, você pode configurar os comprimentos de resposta à sua vontade. Você pode definir o concierge para retornar saídas curtas, médias ou longas, dependendo da visão da sua marca.

**Para personalizar sua expressão de marca**

1. Na Página inicial, clique em **[!UICONTROL Personalizar expressão da marca]**.
2. Em seguida, configure a voz, o tom e a duração de resposta preferencial da sua marca.
3. Selecione **[!UICONTROL Salvar]** para garantir que as alterações sejam refletidas em respostas futuras.

### Pré-visualização e teste {#preview-and-test}

Teste seu concierge antes de iniciá-lo para clientes que usam os modos Visualização e Visualização do testador.

>[!BEGINTABS]

>[!TAB Modo de visualização]

Use o modo de Visualização para simular conversas enquanto faz ajustes em tempo real.

1. Após a configuração, navegue de volta para a Página inicial e clique em **[!UICONTROL Visualizar]**.
1. Use a interface de chat para inserir sua consulta (por exemplo, _Recomendamos um laptop abaixo de US$ 1000_).
1. Revise as respostas do concierge.
1. Use o painel direito para ajustar as configurações de expressão da marca.
1. Clique em **[!UICONTROL Compartilhar]** para gerar um link para os comentários da equipe.

>[!TAB Modo de exibição de testador]

Use a visualização Testador para coletar feedback estruturado sobre o desempenho da portaria e simular a experiência do usuário final.

1. Na visualização, clique em **[!UICONTROL Exibição do testador]**.
1. Use a view Testador para simular conversas com usuários finais.
1. Use o mecanismo de aumento e diminuição para classificar cada resposta recebida.
1. Formulário de feedback completo para miniaturas:
   **Cobertura de resposta:** Ela solucionou a intenção?
   **Tom da marca:** Alinhado com a personalidade?
   **Qualidade da resposta:** Clara e estruturada?
   **Recursos de resposta:** acompanhamento útil?
1. Adicione comentários e observações específicas.
1. Envie feedback para revisão do painel.

>[!ENDTABS]

### Feedback {#feedback}

Após os testes, você pode usar a guia feedback na página inicial para fornecer feedback e revisões detalhadas.

A seção de feedback fornece vários recursos importantes para ajudar você a monitorar e avaliar o desempenho do Brand Concierge. Os seguintes elementos estão disponíveis:

* **Instantâneo de Desempenho:** Exibe cartões com um resumo das métricas principais, incluindo o total de conversas, usuários únicos, tendências de sentimentos e taxa de engajamento.
* **Botão Exibir Relatório:** permite abrir um painel ativado pela Customer Journey Analytics para obter acesso detalhado a análises avançadas e métricas de desempenho.
* **Lista de Comentários:** Apresenta uma tabela de sessões de comentários. Você pode clicar em linhas individuais para exibir a transcrição completa do chat para cada sessão.
* **Painel de Feedback:** Mostra cartões de classificação no lado direito da interface. Passar o mouse sobre esses cartões ou clicar neles destacará as partes relevantes da transcrição do chat para facilitar a referência.

**Para enviar comentários**

1. Navegue até a página inicial do Brand Concierge e selecione **[!UICONTROL Feedback]**.
1. Use o instantâneo fornecido para exibir informações sobre tendências de alto nível.
1. Para acessar um deep drive habilitado pelo Customer Journey Analytics, selecione **[!UICONTROL Exibir Relatório]**.
1. Você também pode inspecionar o painel em busca de comentários conectados adicionais.
1. Quando terminar, você poderá exportar os insights para uso posterior e refinar seu fluxo de trabalho.

### Configurações  {#configurations}

A guia _[!UICONTROL Configurações]_ é uma exibição de resumo somente leitura que você pode usar para revisar a configuração completa da concierge. Isso espelha diretamente a Página inicial após a conclusão da configuração inicial e fornece resumos de seus detalhes, fontes de conhecimento, habilidades e expressão de marca configurada. Você pode usar esse recurso como referência antes de visualizar ou compartilhar sua concierge.

## O que você pode fazer com o Brand Concierge

Saiba mais sobre os recursos do cliente, os recursos comerciais e os casos de uso do Brand Concierge.

### Recursos do cliente

O Brand Concierge oferece uma interface conversacional que permite aos clientes encontrar produtos, comparar opções e obter respostas usando linguagem natural. Com recomendações personalizadas, comparações avançadas de produtos e a capacidade de escalonar para um agente ativo, os clientes desfrutam de uma experiência contínua e intuitiva. A interação é flexível — os clientes podem usar texto, voz ou imagens — e cada resposta é baseada na documentação confiável de sua marca e no contexto do cliente.

* Faça perguntas em linguagem natural e receba recomendações personalizadas.
* Comparar produtos lado a lado com exibições visuais.
* Obtenha respostas da documentação da sua marca.
* Alterne para um agente ativo com histórico completo da conversa.

### Recursos empresariais

O Brand Concierge capacita as empresas com recursos avançados de IA conversacional para o engajamento do cliente. Ele ajuda as marcas a impulsionar a conversão, orientando os clientes para os produtos certos, reduz os custos de suporte por meio de respostas instantâneas e precisas, e garante a voz e a conformidade consistentes da marca. Com análises robustas, entrega contínua de IA para humanos e profundas integrações da Adobe, a Brand Concierge otimiza a experiência do cliente e o desempenho da empresa.

* Oriente os clientes para os produtos certos a fim de aumentar a conversão.
* Reduza os custos de suporte com respostas instantâneas e precisas.
* Controle os requisitos de voz, tom e conformidade da marca.
* Acompanhe o desempenho com o painel do Customer Journey Analytics.
* Habilite transmissão contínua de IA para humanos, incluindo agendamento de reuniões.
* Integre com o Adobe Experience Platform e o Experience Manager.

## Casos de uso

A Brand Concierge oferece suporte a casos de uso de B2C e B2B em vários setores.

| Setor | Casos de uso |
|---|---|
| Varejo e comércio eletrônico | Os clientes podem descobrir produtos e receber recomendações personalizadas. O Brand Concierge fornece orientação sobre dimensionamento e ajuste, ajuda os usuários a encontrar presentes adequados e corresponde a estilos ou preferências com base na entrada do cliente. |
| Vendas B2B | A Brand Concierge orienta os clientes por meio de avaliações de produtos, oferece comparações detalhadas de recursos e preços, auxilia na programação de reuniões de vendas e fornece recomendações específicas do setor personalizadas para clientes empresariais. |
| Suporte ao cliente | Os usuários podem receber respostas instantâneas diretamente da base de conhecimento. A Brand Concierge fornece informações sobre políticas e procedimentos, ajuda a solucionar problemas e fornece atualizações sobre o status e o rastreamento do pedido. |
| Viagens e hospitalidade | Os clientes recebem recomendações de destino personalizadas, assistência com itinerários de planejamento, suporte durante todo o processo de reserva e respostas a perguntas de política de viagem. |
| Serviços financeiros | A Brand Concierge oferece comparações de produtos para ajudar os clientes a escolher as soluções financeiras certas, fornece informações de conta, fornece orientação de reconhecimento de conformidade e permite a programação de reuniões com consultores financeiros. |

