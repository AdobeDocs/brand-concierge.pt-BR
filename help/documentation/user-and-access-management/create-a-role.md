---
title: Criar uma função com permissão do Brand Concierge
description: Saiba como criar uma função e conceder a ela a permissão necessária para acessar o Brand Concierge.
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---


# Criar uma função com permissão do Brand Concierge

Crie uma função nas Permissões do Adobe Experience Platform para conceder aos usuários acesso ao Brand Concierge.

>[!PREREQUISITES]
>
>- Você deve ter as permissões de administrador necessárias para gerenciar funções e permissões.
>- O usuário deve ser adicionado primeiro à organização da Adobe Experience Platform. Para obter mais informações, consulte [Adicionar um usuário à organização](./add-a-user-to-the-org.md).

## Criar a função

1. Entrar em `experienceplatform.adobe.com`.

1. Na navegação à esquerda, role até **Permissões** e selecione-as.
1. Vá para **Funções** para exibir as funções existentes e selecione **Criar uma nova função**.
1. Insira um nome para a função, como `Brand Concierge Access Users`, adicione uma descrição e confirme a criação.
1. Abra a nova função e atribua permissões:

   1. Pesquisar a lista de permissões para **Brand Concierge**.
   1. Selecione **Gerenciar Brand Concierge**.

   No momento, o **Gerenciar Brand Concierge** é a única permissão do Brand Concierge disponível; as camadas de permissão granulares ainda não estão disponíveis.

1. Selecione a sandbox ou sandboxes que a função pode acessar.

   Uma organização pode conter várias sandboxes, que são espaços de trabalho isolados. Selecione somente as sandboxes apropriadas para essa função.

1. Selecione **Salvar**.

## Próximas etapas

Depois que a função for criada, adicione usuários a ela. Para obter mais informações, consulte [Adicionar usuários à função do Brand Concierge](./add-a-user-to-the-role.md).
