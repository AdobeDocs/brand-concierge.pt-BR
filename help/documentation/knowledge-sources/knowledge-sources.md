---
title: Criar e gerenciar fontes de conhecimento para o Brand Concierge
description: Saiba como criar fontes de conhecimento do AEM Sites, de Links de sites e de Catálogos de produtos para o Brand Concierge, monitorar o status do processamento e resolver problemas de rastreo.
hide: true
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 1%

---


# Criar e gerenciar fontes de conhecimento para o Brand Concierge

Uma fonte de conhecimento é o conteúdo que um concierge pode usar ao responder perguntas do visitante. Cada concierge requer pelo menos uma fonte de conhecimento configurada. As fontes de conhecimento são criadas de maneira independente e podem ser reutilizadas em várias concierges.

Um concierge responde a perguntas usando apenas suas fontes de conhecimento configuradas. Ela não responde do conhecimento geral do mundo.

>[!NOTE]
>
>Se um visitante perguntar sobre informações fora das fontes de conhecimento configuradas, o concierge foi projetado para indicar que não tem as informações, em vez de gerar uma resposta não compatível. Use o processo de avaliação para verificar esse comportamento.

## Escolha uma fonte de conhecimento

O Brand Concierge oferece suporte aos seguintes tipos de fonte de conhecimento:

| Fonte de conhecimento | Use-o quando | Recurso principal |
| --- | --- | --- |
| AEM Sites (índice IA de conteúdo) | O cliente usa o AEM Sites as a Cloud Service com a IA de conteúdo ativada. | Usa um índice existente da IA de conteúdo e disponibiliza o conteúdo atualizado do AEM Sites sem uma etapa separada de rastrea ou atualização. |
| Links do site | O cliente precisa rastrear de um site, independentemente da plataforma usada para criá-lo. | Rastrea um mapa de site, URLs individuais selecionados ou URLs fornecidos em um arquivo CSV. |
| Catálogo de produtos | O cliente tem um catálogo de produtos ou serviços relativamente pequeno e não está usando o Adobe Commerce. | Habilita deep links de produtos e cartões de produto em respostas de concierge. |

>[!IMPORTANT]
>
>Os clientes que vendem por meio do Adobe Commerce com um grande catálogo devem usar a integração MCP do Commerce. Os detalhes sobre essa integração estão fora do escopo deste artigo.

## Criar uma fonte de conhecimento do AEM Sites

Use uma fonte de conhecimento da AEM Sites quando o cliente já usar o AEM Sites as a Cloud Service com a IA de conteúdo ativada.

1. Selecione a **Build Knowledge Source**.
1. Selecione **AEM Sites** e **Continue**.
1. Insira um nome e uma descrição para a fonte de conhecimento. Por exemplo, use `My main website` como o nome.
1. Selecione um índice da IA de conteúdo na lista. A lista é preenchida a partir da instância do AEM Sites as a Cloud Service.
1. Selecione **Salvar**.

Essa integração nativa disponibiliza o conteúdo atualizado do AEM Sites para o Brand Concierge automaticamente. Não é necessário um rastreo separado ou uma etapa de atualização.

## Criar uma fonte de conhecimento de Links de site

Use uma fonte de conhecimento de Links de Site para um site rastreável. Essa opção funciona em sites criados em qualquer plataforma e é a opção recomendada para a maioria dos usuários iniciantes.

1. Selecione a **Build Knowledge Source**.
1. Escolha **Links do Site** e selecione **Continuar**.
1. Insira um nome para a fonte de conhecimento.
1. Adicione as fontes de conteúdo usando um dos seguintes métodos:

   - **URL do Mapa do Site:** Adicione uma URL que liste as páginas do site. Todas as páginas listadas no mapa do site são rastreadas.
   - **URLs individuais:** Adicione URLs de página específicas, uma de cada vez. Somente as páginas adicionadas são rastreadas.
   - **Carregamento de CSV:** baixe o arquivo de exemplo, adicione as URLs e carregue o arquivo CSV concluído.

1. (Opcional) Agende uma frequência de atualização, como semanalmente, em um dia e hora especificados, para manter a fonte de conhecimento atualizada à medida que o site muda.
1. Selecione **Adicionar** ou **Criar**.

O sistema rastrea os URLs especificados e remove seu conteúdo para criar a fonte de conhecimento.

>[!TIP]
>
>Um mapa de site normalmente está disponível em `yourwebsite.com/sitemap.xml`. Se o site não fornecer um mapa de site, adicione URLs de página individuais.

## Criar uma fonte de conhecimento do Catálogo de Produtos

Use uma fonte de conhecimento do Catálogo de produtos para clientes com um conjunto menor de produtos ou serviços, aproximadamente menos de 100, que não estejam usando o Adobe Commerce.

Quando uma resposta de concierge faz referência a um produto, o catálogo de produtos pode fornecer um deep link para a página do produto e ativar um cartão de produto. Um cartão de produto pode incluir uma imagem, título, descrição e um ou dois botões.

1. Selecione a **Build Knowledge Source**.
1. Escolha o **Catálogo de Produtos** e selecione **Continuar**.
1. Insira um nome para a fonte de conhecimento. Por exemplo, use `My product catalog - US region` como o nome.
1. Selecione um esquema. O esquema define quais campos de produto (como imagem, título, descrição e botões) são exibidos e onde os botões são vinculados.
1. Baixe a planilha de amostra do esquema selecionado.
1. Adicione os dados do produto à planilha e faça upload deles.
1. Selecione **Salvar**.

Configurações de botão diferentes exigem esquemas diferentes.

## Monitorar status da fonte de conhecimento

Cada fonte de conhecimento exibe um status de processamento.

| Status | Significado |
| --- | --- |
| Em andamento | A fonte de conhecimento está sendo processada no momento. |
| Sucesso | A fonte de conhecimento é totalmente processada e pronta para uso. |
| Programado | A fonte de conhecimento será processada em um horário agendado futuro. |
| Sucesso parcial | Algumas páginas foram processadas com êxito e outras falharam. |

A página de detalhes da fonte de conhecimento fornece informações como:

- O criador.
- A data de criação.
- O número de links ou páginas fornecido.
- O número de links ou páginas que tiveram êxito ou falharam.
- A hora da última atualização.
- Os URLs considerados para processamento.

## Solução de problemas de falhas de processamento

Se uma fonte de conhecimento mostrar um status de sucesso parcial, use o relatório de problemas para identificar os URLs que não puderam ser processados.

1. Abra a página de detalhes da fonte de conhecimento.
1. Selecione **Corrigir Problemas** para baixar um arquivo contendo URLs corrompidas ou que não puderam ser removidas, juntamente com seus detalhes de erro.
1. Corrija os URLs inválidos ou remova-os da lista de origem.
1. Carregue a lista de URLs corrigida novamente, se aplicável.
1. Solicite o reprocessamento para que o conteúdo corrigido seja adicionado à fonte de conhecimento.
