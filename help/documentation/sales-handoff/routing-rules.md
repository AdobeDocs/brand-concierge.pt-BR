---
title: Rotear conversas para representantes
description: Escolha como a Brand Concierge decide qual representante de vendas recebe um chat ao vivo ou uma reserva de reunião, usando round robin, um agente direto ou regras de roteamento personalizadas.
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
source-wordcount: '764'
ht-degree: 0%
---
# Rotear conversas para representantes {#routing}

O roteamento responde a uma pergunta: quando este visitante pergunta por uma pessoa, *qual* pessoa ela recebe?

Você seleciona um tipo de roteamento separadamente para a integração da **[!UICONTROL Reserva de Reunião]** e da integração do **[!UICONTROL Chat ao Vivo]**, para que um porteiro possa distribuir reuniões uniformemente enquanto envia cada chat para um especialista ou qualquer outra combinação.

## Tipos de roteamento {#routing-types}

| Tipo de roteamento | Quem recebe a conversa | Requer [!DNL Marketo Engage] |
| --- | --- | --- |
| **[!UICONTROL Round robin]** | Distribuído por todos os representantes qualificados | Não |
| **[!UICONTROL Agente direto]** | Um representante que você nomeia | Não |
| **[!UICONTROL Roteamento personalizado]** | Os representantes atribuídos à regra de roteamento de prioridade mais alta para a qual o visitante se qualifica | Sim |

Round robin está disponível por padrão e não precisa de configuração. Você define o tipo de roteamento na própria integração. Consulte [Ativar chat ao vivo e reserva de reunião](configure-in-composer.md).

### Round robin {#round-robin}

Round robin se comporta de forma diferente para reuniões e bate-papos, pois os dois têm objetivos diferentes.

**Para reserva de reunião**, o round robin distribui as reuniões uniformemente. O primeiro representante qualificado que conectou um calendário é oferecido primeiro. Uma vez que uma reunião é reservada com eles, eles são retirados do pool e o próximo representante é oferecido. Com cinco representantes, as primeiras cinco reuniões vão para cinco pessoas diferentes. Depois que todos tiverem recebido um, o pool é redefinido e o ciclo é iniciado novamente.

O pool também é redefinido a cada 24 horas, para que as reuniões de cada dia sejam distribuídas uniformemente.

>[!NOTE]
>
>A redefinição de 24 horas é executada em UTC, não no fuso horário local do representante.

**Para o chat ao vivo**, não há rotação sequencial. Cada representante elegível é notificado do bate-papo ao mesmo tempo, e o primeiro a aceitar leva a conversa.

### Agente direto {#direct-agent}

Cada reunião ou bate-papo desta concierge vai para o representante único que você selecionar. Use-a para uma página de aterrissagem de campanha de propriedade de um executivo de conta ou para uma região com um especialista.

### Roteamento personalizado {#custom-routing}

O roteamento personalizado avalia as regras que você cria no [!DNL Adobe Marketo Qualifier] em relação ao cliente potencial [!DNL Marketo] do visitante e aos atributos da empresa. Use-a quando o representante certo depender de algo que você sabe sobre o visitante, como:

* **Geografia** — os visitantes de um conjunto de países vão para a equipe regional.
* **Interesse no produto** — os visitantes interessados em um produto específico acessam os especialistas do produto.
* **Unidade de negócios, tamanho da empresa ou setor** — qualquer combinação de cliente potencial e atributos da empresa.

>[!IMPORTANT]
>
>O roteamento personalizado é uma parte do chat ao vivo e da reserva de reunião que requer [!DNL Adobe Marketo Engage], pois as regras são criadas em atributos de cliente potencial e empresa [!DNL Marketo]. Round robin e trabalho de agente direto sem ele.

## Criar uma regra de roteamento personalizada {#create-rule}

1. Em [!DNL Adobe Marketo Qualifier], em **[!UICONTROL Administração]**, selecione **[!UICONTROL Regras de roteamento]**.

   A lista mostra cada regra da organização com a prioridade, o nome, o criador e a data de criação.

   ![Página de regras de roteamento listando regras existentes com Prioridade, Nome, Criado por e Criado nas colunas](../assets/sales-handoff-routing-1.png){width="800" zoomable="yes"}

1. Selecione **[!UICONTROL Criar regra]** e dê um nome à regra.

1. Crie os critérios.

   O painel esquerdo lista os atributos de [!DNL Marketo] disponíveis dos objetos **[!UICONTROL Empresa]** e **[!UICONTROL Cliente Potencial]** (pessoa). Procure um atributo e arraste-o até a tela para adicionar uma condição.

1. Defina um operador e um valor para cada condição.

   Os operadores incluem **[!UICONTROL é igual a]**, **[!UICONTROL não é igual a]** e **[!UICONTROL contém]**, entre outros. Por exemplo, `Country` **[!UICONTROL é igual a]** `United States`.

1. Combine condições em grupos.

   Adicione várias condições a um grupo e junte-as com **[!UICONTROL AND]** ou **[!UICONTROL OR]**. Adicione mais grupos e ingresse também nos grupos com **[!UICONTROL AND]** ou **[!UICONTROL OR]**. As condições de aninhamento dentro de grupos dessa maneira permitem que você expresse critérios complexos, como *(o país é Estados Unidos OU Canadá) E (os interesses do produto contêm Analytics)*.

1. Atribua a regra a representantes.

   Na seção de atribuição, procure por um representante por nome e selecione-o na lista. Adicione quantos representantes desejar. Qualquer um deles pode receber uma conversa que corresponda à regra.

1. Selecione **[!UICONTROL Salvar]**.

## Como a prioridade é aplicada {#priority}

Toda regra de roteamento tem uma prioridade. A prioridade só importa quando um visitante se qualifica para mais de uma regra.

Quando isso acontece, somente a regra de correspondência de maior prioridade é aplicada e a conversa é roteada para os representantes atribuídos a essa regra. As regras para as quais o visitante também se qualifica, mas com classificação mais baixa, são ignoradas.

>[!NOTE]
>
>Um número menor significa uma prioridade mais alta. Uma regra com prioridade 1 vence uma regra com prioridade 2. A pessoa que cria uma regra define sua prioridade.

Dentro da regra vencedora, os representantes atribuídos a ela são o pool elegível, e o comportamento round robin e all-agent descrito acima se aplica a esse pool.

## Próxima etapa {#next}

Com os representantes configurados e o roteamento decidido, adicione os recursos a uma concierge. Consulte [Ativar chat ao vivo e reserva de reunião](configure-in-composer.md).
