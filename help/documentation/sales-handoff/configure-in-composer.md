---
title: Ativar Chat ao Vivo e Reserva de Reunião
description: Conecte as integrações do Live Chat e da Reserva de reuniões no Composer e ative a Transmissão para a habilidade de vendas, para que seu concierge saiba quando oferecer um humano.
role: User, Admin
level: Beginner
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
source-git-commit: 4751ce408fb2aa6d1affae4dd7a5d81ca43ffc8a
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%
---
# Ativar reserva do Live Chat e da Reunião {#configure-in-composer}

Duas coisas precisam estar no lugar do Composer. As integrações da **[!UICONTROL Reserva de Reunião]** e do **[!UICONTROL Bate-papo ao Vivo]** oferecem ao concierge a *capacidade* de verificar a disponibilidade, iniciar um chat e reservar um slot. A habilidade **[!UICONTROL Transferir para vendas]** informa a ele *quando* para usar essa habilidade.

>[!NOTE]
>
>Conclua [Configurar representantes no Adobe Marketo Qualifier](representative-setup.md) primeiro. As integrações verificam se há calendários conectados e disponibilidade de bate-papo ao vivo, e não serão ativadas sem eles.

## Conectar a integração da Reserva de Reunião {#connect-meeting-booking}

1. No Composer, abra sua portaria e selecione **[!UICONTROL Integrações]** > **[!UICONTROL Procurar integrações]**.

   A **[!UICONTROL Reserva de Reunião]** e o **[!UICONTROL Chat ao Vivo]** aparecem em **[!UICONTROL Integrações Internas]**.

   ![Navegue pelo painel de integrações no Composer, mostrando os cartões de chat ao vivo e de reserva de reunião em Integrações internas](../assets/sales-handoff-composer-1.png){width="800" zoomable="yes"}

1. Selecione **[!UICONTROL Reserva de Reunião]** e **[!UICONTROL Configurar]**.

1. Insira um nome e uma descrição.

   Nomeie a integração para o que ela faz nesta concierge, como `Meeting booking - US region` ou `Meeting booking - round robin`. Você pode conectar mais de um, então o nome é como você os distingue mais tarde.

1. Verifique o status de conexão do calendário.

   A integração verifica se pelo menos um representante em sua organização conectou um calendário.

   * Se nenhum tiver sido ativado, um erro informará que você deve se conectar a pelo menos um calendário antes de ativar a reserva da reunião. Volte para [!DNL Adobe Marketo Qualifier] e conclua [Conectar seu calendário](representative-setup.md#connect).
   * Se pelo menos um tiver, uma confirmação mostrará que os representantes estão disponíveis.

1. Selecione um tipo de roteamento: **[!UICONTROL Round robin]**, **[!UICONTROL Agente direto]** ou **[!UICONTROL Roteamento personalizado]**.

   Se você selecionar **[!UICONTROL Agente direto]**, escolha o representante que recebe cada reunião reservada através desta concierge. Se você selecionar **[!UICONTROL Roteamento personalizado]**, as regras de roteamento que você criou em [!DNL Adobe Marketo Qualifier] serão aplicadas. Para saber como cada um se comporta, consulte [Rotear conversas para representantes](routing-rules.md).

1. Selecione **[!UICONTROL Conectar]**.

## Conectar a integração do Live Chat {#connect-live-chat}

1. Em **[!UICONTROL Procurar integrações]**, selecione **[!UICONTROL Chat ao Vivo]** e **[!UICONTROL Configurar]**.

1. Insira um nome e uma descrição, por exemplo `Live chat - round robin`.

1. Verifique o status de disponibilidade do chat ao vivo.

   A integração verifica se pelo menos um representante definiu a disponibilidade do chat ao vivo.

   * Se nenhum tiver sido, uma mensagem solicitará que você adicione representantes que configuraram a disponibilidade de bate-papo ao vivo. Volte para [!DNL Adobe Marketo Qualifier] e conclua [Definir disponibilidade do chat ao vivo](representative-setup.md#chat-availability).
   * Se pelo menos um tiver, uma confirmação mostrará que os representantes estão disponíveis.

1. Selecione um tipo de roteamento.

   O chat ao vivo é compatível com os mesmos três tipos de roteamento que a reserva de reunião. Com o **[!UICONTROL Round robin]**, todos os representantes qualificados são notificados imediatamente e o primeiro a aceitar entra no chat.

1. Selecione **[!UICONTROL Conectar]**.

## Ativar a Transferência para habilidade de vendas {#activate-skill}

As integrações agora estão conectadas, mas o concierge ainda precisa saber quando oferecê-las. Esse é o trabalho da habilidade.

1. No Composer, selecione **[!UICONTROL Habilidades]** > **[!UICONTROL Pesquisar habilidades]** e selecione **[!UICONTROL Transferir para vendas]**.

   O painel de detalhes mostra a descrição da habilidade, suas **[!UICONTROL Condições Usar quando]**, as **[!UICONTROL Integrações]** recomendadas e as **[!UICONTROL Instruções da habilidade]**.

   ![Navegue pelo painel de habilidades com a Transferência para a habilidade de vendas selecionada, mostrando Usar quando condições, integrações recomendadas e instruções de habilidade](../assets/sales-handoff-composer-2.png){width="800" zoomable="yes"}

1. Selecione **[!UICONTROL Modificar]**.

   ![Transferir para habilidade de vendas no modo de modificação com nome de habilidade editável, descrição e Usar quando condições](../assets/sales-handoff-composer-3.png){width="800" zoomable="yes"}

1. Revise o nome e a descrição da habilidade, e edite-os se desejar.

1. Revise as condições **[!UICONTROL Usar quando]**.

   Essas são as intenções que acionam uma entrega. A habilidade é fornecida com um conjunto padrão:

   | Condição | Acionadores ativados |
   | --- | --- |
   | Acesso do consultor | Reservar ou agendar uma reunião, iniciar um chat ao vivo ou pedir para se conectar com um representante da empresa |
   | Vendas e Compras | Preços, cotações, descontos, assistência na compra ou licenciamento corporativo |
   | Comparação competitiva | Comparar suas soluções com alternativas, diferenciação ou migração de concorrentes |
   | Acesso de avaliação e POC | Configurações de avaliação, acesso ao playground, provas de conceito ou pilotos |
   | Alterações de contrato e licenciamento | Renovações de contrato, extensões de prazo ou atualizações de plano |
   | RFP ou RFI de aquisição | Envios, respostas, questionários de fornecedores, formulários de aquisição ou documentação de conformidade |
   | Demonstrações | Demonstrações ou apresentações do produto |

   Selecione **[!UICONTROL Adicionar condição]** para adicionar sua própria intenção ou excluir qualquer condição que não se aplique à sua empresa.

1. Adicione as integrações conectadas.

   Adicione o **[!UICONTROL Chat ao Vivo]**, a **[!UICONTROL Reserva de Reunião]** ou ambos, dependendo do que você deseja que esta concierge ofereça.

1. Revise as **[!UICONTROL instruções da habilidade]**.

   As instruções são geradas para você a partir das condições e integrações selecionadas, portanto, na maioria dos casos, nenhuma edição é necessária.

   Edite-as em linguagem simples quando quiser um controle mais fino sobre qual intenção leva a qual opção. Por exemplo, você pode instruir o porteiro a oferecer bate-papo ao vivo para perguntas sobre preços, oferecer uma reunião para solicitações de demonstração e oferecer ambos para perguntas sobre aquisição.

1. Selecione **[!UICONTROL Salvar]**.

## Testar e publicar {#test-and-publish}

Abra a visualização e peça ao concierge algo que corresponda a uma das condições de **[!UICONTROL Usar quando]**, como solicitar uma demonstração. O concierge deve oferecer-se para conectá-lo com um especialista, mostrar a opção de chat, a opção de reunião, ou ambos, e apresentar disponibilidade real.

Quando o comportamento estiver certo, publique sua portaria para ativar a entrega no site.

## Próxima etapa {#next}

Seus representantes agora podem receber chats. Consulte [Caixa de entrada de chat](chat-inbox.md).
