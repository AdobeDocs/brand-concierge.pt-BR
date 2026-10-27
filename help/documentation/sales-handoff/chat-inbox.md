---
title: Caixa de entrada do chat
description: Saiba como um representante de vendas recebe, lida com, marca e encerra um bate-papo ao vivo do Brand Concierge na caixa de entrada do bate-papo do Adobe Marketo Qualifier.
role: User
level: Beginner
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
    internal-label: Brand Concierge
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 1%
---
# Caixa de entrada do chat {#chat-inbox}

Quando um visitante pede para falar com alguém, o chat chega na **[!UICONTROL Caixa de entrada do chat]** em [!DNL Adobe Marketo Qualifier]. Esta página é a visão do representante de um bate-papo ao vivo: o que você vê quando ele chega, o contexto que você recebe e o que você precisa fazer antes de fechar.

Para abrir a caixa de entrada do chat, no painel esquerdo em **[!UICONTROL Atividades]**, selecione **[!UICONTROL Caixa de entrada do chat]**.

## Receber um chat {#receive}

Seu status aparece no canto superior direito da caixa de entrada. **[!UICONTROL Disponível]** significa que você pode receber bate-papos agora. O seu horário de disponibilidade de bate-papo ao vivo decide se você está qualificado. Consulte [Definir disponibilidade de bate-papo ao vivo](representative-setup.md#chat-availability).

A forma como um chat chega a você depende do tipo de roteamento definido na integração do **[!UICONTROL Live Chat]**:

* Com rodízio, cada representante elegível é notificado ao mesmo tempo e o primeiro a aceitar conversa.
* Com o agente direto, o bate-papo sempre chega ao representante nomeado.
* Com o roteamento personalizado, o chat vai para os representantes atribuídos à regra de prioridade mais alta correspondida pelo visitante.

Duas guias organizam suas conversas:

* **[!UICONTROL Ativo]** — conversas em andamento.
* **[!UICONTROL Todos]** — todas as conversas, inclusive as que foram encerradas.

## Pegar a conversa {#pick-up}

Você nunca começa com frio. Antes de digitar qualquer coisa, a caixa de entrada fornece tudo o que o visitante já disse à secretária.

![Caixa de entrada do chat mostrando o resumo da conversa do visitante com um resumo e tópicos discutidos e o painel de detalhes do perfil](../assets/sales-handoff-inbox-1.png){width="800" zoomable="yes"}

| O que você vê | O que isso te dá |
| --- | --- |
| **[!UICONTROL Resumo da conversa do visitante]** | Um **[!UICONTROL Resumo]** da conversa que o visitante teve com o concierge, e os **[!UICONTROL Tópicos discutidos]** |
| Transcrição da conversa | A troca completa com o concierge, acima do ponto onde o chat ao vivo foi iniciado |
| **[!UICONTROL Detalhes do formulário]** | O que o visitante inseriu no formulário pré-chat antes de você entrar, como email, interesse no produto e empresa |

A transcrição marca a entrega com duas linhas do sistema, `Live chat session has been initiated` e `Agent <name> has joined the chat`, para que você sempre possa saber qual parte da conversa foi o porteiro e qual parte é sua.

Digite na caixa de mensagem e selecione **[!UICONTROL Enviar]** para responder.

![Chat ao vivo em andamento entre o representante e o visitante](../assets/sales-handoff-inbox-2.png){width="800" zoomable="yes"}

## Pontuar a conversa {#conversation-score}

Antes de terminar um chat, avalie o nível de qualificação do visitante. A pontuação é definida por você, o representante que realmente falou com o visitante, que é o que o torna confiável downstream.

No painel **[!UICONTROL Detalhes do perfil]**, em **[!UICONTROL Pontuação da conversa]**, selecione uma classificação. O traço significa sem pontuação, e os ícones de chama classificam a conversa de menos para mais qualificada.

![Dica de ferramenta de pontuação da conversa explicando que as pontuações são armazenadas no registro de cliente potencial como 0, 1, 2 e 3](../assets/sales-handoff-inbox-4.png){width="600" zoomable="yes"}

| Seleção | Valor armazenado | Significado |
| --- | --- | --- |
| Traço | 0 | Menos qualificado |
| Uma chama | 1 | Um pouco qualificado |
| Duas chamas | 2 | Qualificado |
| Três chamas | 3 | Mais qualificado |

>[!IMPORTANT]
>
>A pontuação é obrigatória. Se você tentar fechar um bate-papo sem marcá-lo, o erro `Please score the conversation before you close the chat` aparecerá e o bate-papo permanecerá aberto. Depois de marcá-la, uma confirmação é exibida e você pode fechar o bate-papo.

![Confirmação de que a pontuação da conversa foi salva](../assets/sales-handoff-inbox-3.png){width="800" zoomable="yes"}

A pontuação é gravada na atividade **[!UICONTROL Engage with Live Chat in Concierge]** em [!DNL Marketo Engage], onde está disponível como uma restrição em filtros e acionadores. Use-a para direcionar redirecionamento, pontuação de clientes potenciais, personalização e entrega do CRM. Consulte [dados do Brand Concierge no Marketo Engage](marketo-activities.md).

## Encerrar o chat {#end-chat}

Selecione **[!UICONTROL Encerrar chat]** para fechar a conversa. O visitante também pode encerrá-lo pelo lado dele e é solicitado a confirmar primeiro.

Quando um chat é fechado, seu status de conversa é registrado como um dos dois valores:

* **Encerrado** — a conversa foi encerrada deliberadamente, por você ou pelo visitante.
* **Ignorado** — o visitante saiu do site e a conversa atingiu o tempo limite por inatividade.

>[!NOTE]
>
>As conversas de chat ao vivo são mantidas por 30 dias.

## Próxima etapa {#next}

Veja o que tudo isso grava de volta no banco de dados de marketing em [dados do Brand Concierge no Marketo Engage](marketo-activities.md).
