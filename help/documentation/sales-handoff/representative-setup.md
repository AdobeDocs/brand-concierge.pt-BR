---
title: Configurar representantes no Adobe Marketo Qualifier
description: Conecte-se ao calendário do Outlook ou Google de um representante, defina o email de confirmação da reunião, o calendário e a disponibilidade do bate-papo ao vivo, e analise quem está configurado.
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
source-git-commit: 91cbec8d6f4e4800e3bdc8c8f60bfe9ed168a963
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%
---
# Configurar representantes no Adobe Marketo Qualifier {#representative-setup}

Para que uma secretária possa oferecer uma reunião ou um chat ao vivo, pelo menos um representante deve ser configurado em [!DNL Adobe Marketo Qualifier]. Cada representante faz isso uma vez, em seu próprio perfil.

A sequência é: um administrador adiciona os usuários, então cada representante conecta um calendário, escreve seu email de confirmação e declara quando eles estão disponíveis para reuniões e bate-papo.

## Adicionar usuários à organização {#add-users}

Um administrador adiciona cada representante de vendas como um usuário no [!DNL Adobe Admin Console] e concede a ele acesso a [!DNL Adobe Marketo Qualifier]. Para obter o procedimento geral, consulte [Adicionar usuário à organização](../user-and-access-management/add-a-user-to-the-org.md) e [Adicionar usuário à função](../user-and-access-management/add-a-user-to-the-role.md).

Os próprios representantes completam as etapas restantes.

## Conectar seu calendário {#connect}

A conexão do calendário é o que torna a disponibilidade real visível para um concierge. Sem ele, o representante não é elegível para a reserva da reunião.

1. Entre na [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} e selecione **[!UICONTROL Adobe Marketo Qualifier]**.

   ![Página inicial da Adobe Experience Cloud com o cartão da Adobe Marketo Qualifier](../assets/meetings-connect-1.png){width="800" zoomable="yes"}

1. No painel esquerdo, em **[!UICONTROL Configuração]**, selecione **[!UICONTROL Configurações de perfil]** e abra a guia **[!UICONTROL Configuração de calendário]**.

1. Escolha o calendário que deseja conectar, [!DNL Microsoft Outlook] ou [!DNL Google Calendar].

   ![Guia de configuração de calendário mostrando as opções de conexão de calendário do Outlook e do Google](../assets/meetings-connect-2.png){width="600" zoomable="yes"}

1. Entre com uma conta existente ou adicione uma nova e conceda as permissões solicitadas.

   ![Seletor de conta da Microsoft mostrado durante a conexão do calendário](../assets/meetings-connect-3.png){width="600" zoomable="yes"}

1. Revise o email de confirmação que um visitante recebe quando reserva uma reunião com você.

   Uma linha de assunto e um corpo padrão estão definidos para você. Edite qualquer um e escolha se deseja incluir um link de reunião [!DNL Microsoft Teams] no convite.

   ![Configurações de email de confirmação da reunião com corpo e linha de assunto editáveis](../assets/meetings-connect-4.png){width="600" zoomable="yes"}

1. Selecione **[!UICONTROL Salvar]**.

## Definir disponibilidade do calendário {#calendar-availability}

A conexão de um calendário informa [!DNL Adobe Marketo Qualifier] quando você está *ocupado*. A disponibilidade do calendário informa quando você está *disposto* a participar de uma reunião. Ambos são aplicados.

1. Em **[!UICONTROL Configurações de perfil]**, abra a guia **[!UICONTROL Disponibilidade do calendário]**.

   ![Guia de disponibilidade de calendário antes de qualquer disponibilidade ser definida](../assets/meetings-availability-1.png){width="600" zoomable="yes"}

1. Defina suas regras de reunião.

   | Configuração | O que ele controla |
   | --- | --- |
   | Duração da reunião | Por quanto tempo uma reunião reservada é executada e, portanto, a duração de cada slot oferecido |
   | Tempo de buffer | O intervalo entre o fim de uma reunião e o início da próxima |
   | Aviso mínimo | O quão longe um visitante deve reservar. Por exemplo, defina 4 horas para impedir que os visitantes reservem um slot que comece em 10 minutos |
   | Fuso horário | O fuso horário em que suas horas de disponibilidade são expressas. Os visitantes sempre veem slots convertidos em seu próprio fuso horário |

1. Defina as horas disponíveis para cada dia da semana.

   Um dia pode ser um bloco contínuo, como de 8h às 17h, ou vários blocos, como de 8h às 12h e de 2h às 17h. Deixe um dia em branco para não participar de nenhuma reunião naquele dia.

   >[!NOTE]
   >
   >Para adicionar outro bloco de tempo a um dia, selecione o sinal de adição (![ícone do sinal de adição](../assets/icon-plus-sign.png)).

   ![Guia de disponibilidade de calendário com horas da semana e intervalo de tempo dividido configurado](../assets/meetings-availability-2.png){width="600" zoomable="yes"}

1. Selecione **[!UICONTROL Salvar]**.

### Como um slot se torna reservável {#slot-logic}

Um intervalo de tempo é oferecido a um visitante somente quando ele se mantém em todas as três verificações:

1. Ele se enquadra nas horas disponíveis que você definiu aqui.
1. Ele ainda não está ocupado por um evento no calendário conectado. Uma reunião existente às 9h remove o slot às 9h.
1. Ele satisfaz seu aviso mínimo e tempo de buffer.

## Definir disponibilidade do chat ao vivo {#chat-availability}

A disponibilidade do chat ao vivo é separada da disponibilidade do calendário. Um representante pode estar disponível para bate-papo, mas não participar de reuniões, ou o inverso.

1. Em **[!UICONTROL Configurações de perfil]**, abra a guia **[!UICONTROL Disponibilidade do chat ao vivo]**.

1. Defina seu fuso horário e, em seguida, defina os dias e horas em que você está disposto a receber um chat ao vivo. Os finais de semana podem ser incluídos.

   ![Guia de disponibilidade de chat ao vivo com dias e horas configuradas](../assets/meetings-availability-3.png){width="600" zoomable="yes"}

1. Selecione **[!UICONTROL Salvar]**.

>[!NOTE]
>
>As horas de disponibilidade tornam você *qualificado* para chats. Seu status ao vivo na caixa de entrada do bate-papo decide se você os receberá agora. Consulte [Caixa de entrada de chat](chat-inbox.md).

## Analisar quem está configurado {#manage-members}

Esta seção é somente para administradores do. Em **[!UICONTROL Administração]**, selecione **[!UICONTROL Gerenciar membros]** para ver o estado de cada representante em um local: que conectou um calendário, que definiu a disponibilidade do chat ao vivo e que desconectou um calendário.

Use-a antes de ativar as integrações no Composer. Um representante que aparece aqui sem um calendário conectado não está qualificado para reserva de reunião, e um representante sem disponibilidade de chat ao vivo não está qualificado para bate-papo ao vivo.

![Gerenciar representantes da página de membros e seu calendário e estado de configuração do chat ao vivo](../assets/manage-members-1.png){width="800" zoomable="yes"}

## Próxima etapa {#next}

Com pelo menos um representante definido, decida como os visitantes são correspondidos aos representantes. Consulte [Rotear conversas para representantes](routing-rules.md).
