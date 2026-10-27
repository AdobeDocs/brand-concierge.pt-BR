---
title: Visão Geral do Chat ao Vivo e da Reserva de Reunião
description: Saiba como o Brand Concierge entrega um visitante a um humano, seja como um bate-papo ao vivo com um representante disponível ou como uma reunião reservada no calendário de um representante.
role: User, Admin
level: Beginner
TQID: https://experienceleague.adobe.com/vfX6M2-ts7d2-AxKGjaP1Ygkk3FGSGRl4CHslcKYSXU
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%
---
# Visão geral do chat ao vivo e da reserva de reunião {#overview}

Um concierge responde sozinho à maioria das perguntas. Algumas conversas precisam de uma pessoa: uma negociação de preços, um questionário de aquisição, uma solicitação de demonstração. O chat ao vivo e a reserva de reunião são as duas maneiras pelas quais o Brand Concierge entrega essa conversa a um humano sem perder o contexto que o visitante já forneceu.

* O bate-papo ao vivo conecta o visitante a um representante disponível imediatamente, na mesma janela de bate-papo.
* A reserva da reunião oferece ao visitante espaços abertos reais do calendário de um representante e agenda a reunião.

Ambos são oferecidos pela mesma habilidade, **[!UICONTROL Transferência para vendas]**, e ambos percorrem [!DNL Adobe Marketo Qualifier] (antigo [!DNL Sales Qualifier]), onde seus representantes conectam seus calendários, definem sua disponibilidade e fazem bate-papos.

## Como funciona uma entrega {#how-it-works}

Quatro partes precisam ser alinhadas antes que um visitante possa alcançar uma pessoa.

| Peça | O que faz | Onde você o configurou |
| --- | --- | --- |
| Perfil representativo | Conecta um calendário e declara quando o representante está disponível para reuniões e bate-papo | [!DNL Adobe Marketo Qualifier] > **[!UICONTROL Configurações de perfil]** |
| Roteamento | Decide *qual* representante recebe este visitante | [!DNL Adobe Marketo Qualifier] > **[!UICONTROL Regras de roteamento]** e o tipo de roteamento em cada integração |
| Integrações | A **[!UICONTROL Reserva de Reunião]** e o **[!UICONTROL Bate-papo ao Vivo]** oferecem ao concierge a capacidade de verificar a disponibilidade, iniciar um chat e reservar um slot | Compositor > **[!UICONTROL Procurar integrações]** |
| Habilidade | **[!UICONTROL Transferência para vendas]** decide *quando* oferecer uma transferência, com base na intenção do visitante | Compositor > **[!UICONTROL Pesquisar habilidades]** |

No tempo de execução, o visitante informa algo que corresponde a uma das condições **[!UICONTROL Use when]** da habilidade. A habilidade é acionada e chama qualquer integração que estiver anexada a ela. O roteamento resolve um representante, e o visitante recebe uma oferta de bate-papo, reunião ou ambos.

>[!NOTE]
>
>Habilidades e integrações são os blocos de construção gerais de um concierge. Para o modelo subjacente, consulte [Estrutura de Habilidades e Integrações](../skills-and-integrations.md).

## A experiência do visitante {#visitor-experience}

Quando a habilidade é disparada, o porteiro explica as opções e as apresenta como botões na conversa.

![Resposta concierge oferecendo uma entrega, com o Chat com um especialista agora e os botões de Agendar reunião abaixo dele](../assets/sales-handoff-visitor-1.png){width="800" zoomable="yes"}

### Bate-papo ao vivo {#visitor-live-chat}

Se o visitante optar por bater papo, o concierge mostrará um estado de conexão enquanto o roteamento encontrar um representante disponível.

![Atendimento ao cliente mostrando uma Conexão com um status de especialista depois que o visitante seleciona Chat com um especialista agora](../assets/sales-handoff-visitor-2.png){width="800" zoomable="yes"}

Antes de o representante se juntar, o visitante preenche um curto formulário pré-bate-papo. Essas respostas viajam com a conversa e são exibidas para o representante como **[!UICONTROL Detalhes do formulário]** na caixa de entrada do chat, para que o visitante não precise repetir nada.

O visitante pode encerrar o bate-papo a qualquer momento e precisa confirmar.

![Encerre a caixa de diálogo de confirmação do chat solicitando que o visitante confirme o encerramento do chat com o especialista](../assets/sales-handoff-visitor-4.png){width="800" zoomable="yes"}

### Reserva da reunião {#visitor-meeting-booking}

Se o visitante optar por marcar uma reunião, o concierge mostrará um calendário com os slots que estão realmente abertos no calendário do representante roteado, no fuso horário do próprio visitante.

![Reserve um cartão de reunião na conversa mostrando um calendário mensal e uma lista de intervalos de tempo disponíveis](../assets/sales-handoff-visitor-3.png){width="800" zoomable="yes"}

Depois que o visitante confirmar um slot, ele receberá o email de confirmação do representante, que, opcionalmente, inclui um link [!DNL Microsoft Teams]. O contexto da conversa vai para o representante com o convite.

## O que é necessário antes de começar {#prerequisites}

* Acesso a [!DNL Adobe Marketo Qualifier], com seus representantes adicionados como usuários em [!DNL Adobe Admin Console].
* Pelo menos um representante que conectou um calendário. A integração da **[!UICONTROL Reserva de Reunião]** não pode ser ativada até que seja concluída.
* Pelo menos um representante que definiu a disponibilidade do chat ao vivo. A integração do **[!UICONTROL Chat ao Vivo]** não pode ser ativada até que um tenha.
* Uma concierge no Composer que você pode adicionar integrações e habilidades ao.

>[!NOTE]
>
>O chat ao vivo e a reserva de reunião não exigem [!DNL Adobe Marketo Engage]. Sem ele, os dados de representante, reunião e chat permanecem em [!DNL Adobe Marketo Qualifier]. Duas coisas exigem [!DNL Marketo Engage]: regras de roteamento personalizadas, que são criadas em [!DNL Marketo] atributos de cliente potencial e de empresa, e os tipos de atividade de concierge que são gravados de volta no registro de pessoa [!DNL Marketo].

## Configurar o chat ao vivo e a reserva da reunião {#setup-path}

Analise esses itens em ordem.

1. [Configurar representantes no Adobe Marketo Qualifier](representative-setup.md) — conecte um calendário, defina o email de confirmação e defina o calendário e a disponibilidade do chat ao vivo.
1. [Rotear conversas para representantes](routing-rules.md) — escolha round robin, um agente direto ou regras personalizadas compiladas em [!DNL Marketo] atributos.
1. [Ativar chat ao vivo e reserva de reunião](configure-in-composer.md) — conecte as duas integrações e ative a habilidade **[!UICONTROL Transmissão para vendas]**.
1. [Caixa de entrada de chat](chat-inbox.md) — o que os representantes fazem quando um chat chega, incluindo a pontuação da conversa.
1. [Dados do Brand Concierge no Marketo Engage](marketo-activities.md) — os campos de cliente potencial e os tipos de atividade gravados em [!DNL Marketo] e como usá-los em Campanhas Inteligentes.
1. [Monitorar reuniões e bate-papos ao vivo](monitor.md) — a lista de reservas e o painel de desempenho.

## Retenção de dados {#retention}

As conversas de chat ao vivo são mantidas por 30 dias.
