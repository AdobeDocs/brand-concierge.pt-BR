---
title: Analisar desempenho de concierge
description: Saiba como revisar análises de concierge, inspecionar transcrições de conversas, adicionar perguntas de visitantes aos conjuntos de avaliação e abrir relatórios do Customer Journey Analytics.
hide: true
source-git-commit: da4b30fa292b911987aebec378af420b293ea594
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---


# Analisar desempenho de concierge

**Quem é este para:** Profissionais de marketing que usam a experiência de autoatendimento. Nenhuma configuração é necessária após a implantação do concierge.

**Cadência recomendada:** analise as análises conforme necessário. Um check-in semanal é um ponto de partida razoável.

O Analytics ajuda você a entender como os visitantes se envolvem com uma concierge ao vivo. Após a implantação, a guia **Analytics** exibe automaticamente as métricas de conversa e fornece acesso a transcrições individuais e a um relatório mais detalhado do Customer Journey Analytics.

## Exibir análises

1. Abra a concierge e selecione a guia **Analytics**.

1. Defina o intervalo de datas do período que deseja revisar.

1. Opcionalmente, filtre os resultados por tipo de conversa.

A guia Analytics exibe as seguintes métricas automaticamente:

| Métrica | Descrição |
|---|---|
| Conversas | O número de conversas durante o período selecionado. |
| Visitantes envolvidos | O número de visitantes que interagiram com o concierge. |
| Sentimento positivo | A quantidade de sentimentos positivos identificados em conversas. |
| Mensagens por conversa | O número médio de mensagens trocadas em uma conversa. |

>[!NOTE]
>
>Nenhuma configuração é necessária para exibir essas métricas após a implantação do concierge.

## Revisar transcrições da conversa

As transcrições da conversa permitem analisar o que os visitantes perguntaram e como o concierge respondeu.

1. Na guia Analytics, selecione uma conversa.

1. Leia a transcrição completa.

1. Analise se os visitantes selecionaram uma classificação de aumento ou diminuição para respostas individuais.

Cada conversa tem uma ID de conversa exclusiva. Use essa ID para corresponder a transcrição aos registros em outros sistemas quando a implementação for compatível com esse fluxo de trabalho.

### Adicionar uma conversa a um conjunto de avaliação

Se um visitante fizer uma pergunta útil para testes futuros, adicione-a diretamente a um conjunto de avaliação da transcrição.

1. Abra a transcrição da conversa.

1. Selecione **Adicionar à Avaliação**.

Adicionar perguntas reais de visitantes ajuda a manter os conjuntos de avaliação baseados nas perguntas que os visitantes realmente fazem. Para obter mais informações sobre conjuntos de avaliação, consulte [Avaliar uma concierge](../evaluation/evaluation.md).

>[!TIP]
>
>Revise as transcrições regularmente e adicione perguntas representativas, não apenas perguntas que receberam feedback negativo, para ajudar a manter um conjunto de avaliação equilibrado.

## Abrir o relatório do Customer Journey Analytics

Selecione **Exibir Relatório** para abrir um painel mais detalhado no Adobe Customer Journey Analytics (CJA). O painel de controle é provisionado automaticamente e não requer configuração adicional.

O painel de controle do CJA inclui:

- Tendências de conversas semanais.
- Repetir o engajamento, incluindo conversas por pessoa.
- Mensagens por conversa.
- Tendências de feedback do visitante.
- Intenção do visitante.
- Sentimento e tom do visitante.
- Recomendações de concierge feitas durante conversas.

Use o painel para examinar tendências ao longo do tempo e identificar alterações no envolvimento, feedback, intenção e sentimento do visitante.

>[!IMPORTANT]
>
>Não trate IDs de conversa como um fluxo de trabalho de exportação. É necessária uma apresentação específica de produto ou engenharia antes de documentar como exportar conversas ou transcrições.
