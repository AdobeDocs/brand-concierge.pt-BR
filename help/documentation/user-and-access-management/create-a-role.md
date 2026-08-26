---
title: Criar uma função com permissão do Brand Concierge
description: Saiba como criar uma função e conceder a ela a permissão necessária para acessar o Brand Concierge.
source-git-commit: 591bd1600e586a0a4ce484dbff3f9fb97e24d43d
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Criar uma função com permissão do Brand Concierge

Crie uma função nas Permissões do Adobe Experience Platform para conceder aos usuários acesso ao Brand Concierge.

## Pré-requisitos

* Você deve ter as permissões de administrador necessárias para gerenciar funções e permissões.
* O usuário deve ser adicionado primeiro à organização da Adobe Experience Platform. Para obter mais informações, consulte &#39;Adicionar um usuário à organização&#39; (LINK).

## Criar a função

1. Entrar em `experienceplatform.adobe.com`.

   >[!NOTE]
   >
   >Confirme o URL de produção com a engenharia antes de publicar esse procedimento. A gravação de origem usou um URL informal ou possivelmente transcrito incorretamente.

2. Na navegação à esquerda, role até **Permissões** e selecione-as.
3. Selecione **Funções** para exibir as funções existentes e selecione **Criar uma nova função**.
4. Insira um nome para a função, como `Brand Concierge Access Users`, adicione uma descrição e confirme a criação.
5. Abra a nova função e atribua permissões:

   1. Pesquisar a lista de permissões para **Brand Concierge**.
   2. Selecione **Gerenciar Brand Concierge**.

   Atualmente, **Gerenciar Brand Concierge** é a única permissão disponível para o Brand Concierge. As camadas de permissão granulares não estão disponíveis no momento.

6. Selecione a sandbox ou sandboxes que a função pode acessar.

   Uma organização pode conter várias sandboxes, que são espaços de trabalho isolados. Selecione somente as sandboxes apropriadas para essa função.

7. Selecione **Salvar**.

## Próximas etapas

Depois que a função for criada, adicione usuários a ela. Para obter mais informações, consulte &#39;Adicionar usuários à função&#39; (LINK).

## Considerações relacionadas

* O processo de criação e gerenciamento de sandboxes está fora do escopo desse procedimento.
* Confirme se permissões granulares adicionais do Brand Concierge estão planejadas antes de definir um modelo de função de longo prazo.
