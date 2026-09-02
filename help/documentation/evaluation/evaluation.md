---
title: Avaliar um concierge
description: Saiba como criar conjuntos de avaliação e executar avaliações funcionais, fora do escopo e de proteção para avaliar a precisão e a segurança das respostas de um concierge.
hide: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---


# Avaliar um concierge

**Quem é este para:** Profissionais de marketing que usam a experiência de autoatendimento. Não é necessária assistência de TI.

**Tempo necessário:** alguns minutos para criar um conjunto de avaliação. A execução de uma avaliação demora mais dependendo do tamanho do conjunto.

As avaliações ajudam você a criar confiança de que as respostas de um porteiro são precisas antes que o porteiro seja revisado por qualquer pessoa fora da equipe imediata. Diferentemente dos testes ad hoc na experiência de visualização, as avaliações fornecem uma maneira repetível de medir as respostas em relação às respostas esperadas.

## Tipos de avaliação

As avaliações dividem-se em três categorias:

| Tipo | Finalidade |
|---|---|
| Funcional | Verifica respostas para perguntas normais e relevantes sobre seus produtos ou serviços. |
| Fora do escopo | Verifica como o concierge lida com perguntas que não devem ser respondidas, mas que não são prejudiciais, como perguntas sobre um concorrente ou um tópico não relacionado. |
| Salvaguarda | Verifica como o porteiro lida com entradas prejudiciais ou adversárias, incluindo perguntas falsas, profanação e tentativas de manipulá-las. |

## Criar um conjunto de avaliação

Um conjunto de avaliação, também chamado de *conjunto de dados dourado* ou *verdade fundamental*, é uma lista de perguntas de exemplo emparelhadas com as respostas consideradas corretas. As respostas reais do concierge são comparadas com essas respostas esperadas durante uma avaliação.

### Criar um conjunto de avaliação

1. Nomeie o conjunto de avaliação. Por exemplo, `About my products`.

1. Escolha como criar o conjunto:

   * **Gerado por IA:** o Composer lê a fonte de conhecimento e elabora uma lista de perguntas prováveis e respostas esperadas para revisão.
   * **Carregamento manual ou de planilha:** forneça uma lista de perguntas e respostas diretamente.

1. Se você estiver criando um conjunto gerado por IA, verifique se a fonte de conhecimento está totalmente configurada antes de gerar o conjunto. O Composer usa a fonte de conhecimento para elaborar as perguntas e respostas.

1. Revisar cada par de perguntas e respostas gerado:

   * Edite uma resposta para ajustar seu estilo.
   * Exclua uma pergunta que não seja relevante.

1. Como opção, baixe o conjunto como uma planilha para análise por um colega. Após a revisão, faça upload da planilha novamente.

>[!TIP]
>
>Os conjuntos de avaliação gerados por IA são rascunhos com base na fonte de conhecimento. Revise e corrija-as da mesma maneira que você revisa o perfil da marca e as instruções durante a criação do concierge.

## Executar uma avaliação

1. Selecione **Executar Avaliação**.

1. Selecione o conjunto de avaliação a ser executado e selecione **Executar**.

1. Aguarde enquanto o concierge é perguntado em todas as perguntas do conjunto. As respostas reais do concierge são comparadas com as respostas esperadas.

   O tempo de processamento aumenta de acordo com o número de perguntas no conjunto. O andamento é exibido como uma porcentagem.

1. Quando o processamento estiver concluído, analise a pontuação geral e o número de respostas sinalizadas.

Respostas sinalizadas são respostas potencialmente problemáticas que podem exigir revisão adicional.

## Revisar resultados da avaliação

Os **Resultados da Avaliação** exibem todas as execuções anteriores de um conjunto de avaliação, para que você possa acompanhar os resultados ao longo do tempo.

Para revisar uma execução:

1. Abra uma execução de avaliação a partir de **Resultados da Avaliação**.

1. Analise cada pergunta juntamente com a resposta real do porteiro e a resposta esperada.

1. Revise a classificação atribuída a cada resultado. Os resultados recebem uma classificação de **alta**, **média** ou **baixa** e incluem uma observação explicando o raciocínio. Por exemplo, um resultado pode ser marcado como **necessita de atenção** com um motivo para a classificação.

1. Revise as respostas sinalizadas diretamente para se concentrar em resultados potencialmente problemáticos sem ler todos os resultados na execução.

## Práticas recomendadas

* Configure completamente a fonte de conhecimento antes de gerar um conjunto de avaliação baseado em IA. Um conteúdo original mais completo produz melhores perguntas de rascunho.
* Crie pelo menos um pequeno conjunto de avaliações para cada tipo de avaliação: funcional, fora de escopo e de proteção. Cada tipo captura uma classe diferente de problema.
* Execute as avaliações novamente após qualquer alteração significativa na configuração, incluindo alterações nas instruções, medidas de proteção, habilidades ou integrações. Trate as avaliações como uma prática contínua em vez de um portão único.
* Adicione perguntas reais de visitantes do Analytics a um conjunto de avaliação quando elas revelarem uma lacuna que vale a pena testar.
