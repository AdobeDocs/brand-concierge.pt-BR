---
title: Estrutura de habilidades e integrações
description: Saiba como as habilidades e integrações funcionam juntas na estrutura de concierge. As habilidades definem comportamento, enquanto as integrações se conectam aos dados e fornecem capacidade.
role: User, Admin
level: Beginner
source-git-commit: 16136f0d5470a39cbf260f4b1eadc6918d0212b4
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# Estrutura de habilidades e integrações {#skills-and-integrations}

Uma integração (anteriormente conhecida como ferramenta) é uma conexão com uma fonte de dados ou back-end. Uma habilidade é um comportamento.

Uma integração pode ser usada por muitas habilidades. Uma habilidade pode usar várias integrações. Você os configura independentemente e os mapeia juntos.

## Habilidades

Uma habilidade é a camada de comportamento de um porteiro. É uma unidade nomeada e reutilizável que define um único trabalho que o porteiro pode fazer: o que ele lida, quando entra e como responde. Uma habilidade não tem dados próprios; ela empresta a capacidade das integrações anexadas a ela.

Cada habilidade é composta de cinco partes:

| Parte | O que é |
| --- | --- |
| Nome | O identificador da habilidade |
| Descrição | Para que serve a habilidade, seu propósito em termos simples |
| Usar quando | A condição do acionador. Este é o sinal de roteamento que informa ao concierge quando invocar esta habilidade em vez de outra |
| Integrações | As ferramentas específicas que essa habilidade tem permissão para chamar para fazer seu trabalho. Uma habilidade só pode usar o que está anexado aqui |
| Arquivo de instruções | As instruções detalhadas que regem como a habilidade se comporta e como ela interpreta uma solicitação, formata sua resposta e aplica suas medidas de proteção |

Como uma habilidade se comporta no tempo de execução: quando uma mensagem de usuário chega, a plataforma a compara com o acionador &quot;usar quando&quot; de cada habilidade ativa e direciona a mensagem para a habilidade correspondente. Essa habilidade então executa suas instruções e chama somente as integrações anexadas a ela. Suas instruções são compostas no comportamento geral do concierge em tempo de execução ao lado do perfil da marca e de quaisquer outras habilidades ativas.

Uma habilidade decide o que fazer e quando. Ela mesma não se conecta a nenhum dado; essa é a função da integração.

_Exemplo da habilidade de Consultoria de Site_

![Painel de detalhes de habilidades do Site Advisory mostrando sua descrição, Use quando acionadores, integração da Pesquisa da Base de Dados de Conhecimento anexada e instruções de habilidades](assets/skills-and-integrations-1.png){width="800" zoomable="yes"}

## Integrações

Uma integração é a camada de capacidade de um concierge. É uma conexão com um sistema externo ou de back-end (uma base de conhecimento, uma fonte de conteúdo, um catálogo de comércio ao vivo) que realmente busca dados ou executa uma ação. Quando uma habilidade é julgamento, uma integração é capacidade.

Cada integração tem estas características:

| Característica | O que significa |
| --- | --- |
| Conexão e credenciais | Uma integração é autenticada em seu backend usando sua própria configuração do, por exemplo, uma ID de ambiente de comércio e uma chave de API. Essa configuração é o que a aponta para a fonte de dados correta |
| Recursos expostos | Uma integração disponibiliza um ou mais recursos chamáveis, as ações individuais que uma habilidade pode invocar. O Commerce MCP, por exemplo, expõe a pesquisa de produtos, detalhes de produtos, variantes e descoberta de facetas como recursos separados |
| Reutilizável | Uma integração pode ser anexada a muitas habilidades, e a mesma integração serve a muitos clientes e concierges. Essa reutilização é a principal eficiência da estrutura |

Como uma integração se comporta no tempo de execução: quando uma habilidade é acionada e decide que precisa de dados, ela chama uma das ferramentas da integração. A integração executa essa chamada no back-end em tempo real e retorna dados estruturados à habilidade, que a habilidade usa para formar sua resposta.

Uma integração fornece capacidade, mas não exerce julgamento. Ele aguarda para ser chamado por uma habilidade, faz o trabalho específico solicitado e retorna o resultado.

### Recursos e limites (o limite de autoatendimento)

- **Autoatendimento, sem engenharia:** Edite instruções, edite os disparadores &quot;usar quando&quot;, anexe ou desanexe integrações existentes, habilite ou desabilite uma habilidade e conecte uma integração com suporte (como o Commerce MCP com credenciais válidas).

- **Não é de autoatendimento, precisa de engenharia:** Crie uma ferramenta ou um conector totalmente novo que ainda não exista no catálogo, adicione uma nova categoria de garantia para a qual a estrutura não oferece suporte ou altere os dados que uma infraestrutura expõe.

- **O acionamento da sobreposição entre duas habilidades é um risco de configuração:** Se duas habilidades puderem ser acionadas na mesma mensagem, o roteamento poderá ser inconsistente. Grave acionadores para evitar ambiguidade genuína em vez de depender do roteador para resolvê-la.

## Integrações disponíveis prontas para uso

Abaixo estão as quatro integrações mostradas no painel **Procurar integrações** do Composer.

| Integração | O que faz | Notas |
| --- | --- | --- |
| Pesquisa na knowledge base | Source para informações de produto, preços, recursos e documentação de uma marca, preenchido por meio de um rastreo de sites | Este é criado automaticamente na criação do concierge, preenchido pelo rastreo de sites |
| Pesquisa com IA de conteúdo | Pesquisa o conteúdo da marca via IA de conteúdo | Uma fonte de conteúdo alternativa; geralmente, apenas uma das Pesquisas com IA de Pesquisa ou Conteúdo da Base de Dados de Conhecimento é necessária por vez |
| Vinculação de entidade/mapeamento de catálogo de produtos | Resolve o produto ou as menções de marca na mensagem de um usuário para entidades de catálogo específicas | Integração de suporte, usada junto com uma integração de pesquisa em vez de sozinha |
| COMMERCE MCP | Servidor MCP do Commerce gerenciado pela Adobe: pesquisa de produtos, detalhes, variantes e descoberta de facetas/atributos, com o apoio do Adobe Live Search | Não está na linha de base; adicionado manualmente para casos de uso do Commerce |

![Painel de integrações de navegação mostrando quatro cartões de integração: Pesquisa com IA de Conteúdo, Vinculação de Entidade, Pesquisa na Base de Dados de Conhecimento e Commerce MCP](assets/skills-and-integrations-2.png){width="800" zoomable="yes"}

## Habilidades disponíveis imediatamente

Quatro habilidades estão no catálogo. Cada uma lista suas integrações recomendadas.

| Habilidade | Para que serve? | Integrações recomendadas |
| --- | --- | --- |
| Aviso do site | Perguntas gerais sobre a marca: políticas, perguntas frequentes, programas, instruções e suporte | Pesquisa na knowledge base, Pesquisa com IA de conteúdo e vinculação da entidade |
| Aviso do produto | Descubra e pesquise produtos: cartões de produto com base em nome e perguntas sobre produtos em prosa | Pesquisa na Base de Dados de Conhecimento, Vinculação de Entidade/Mapeamento de Catálogo |
| Descoberta do catálogo Adobe Commerce | Pesquise, navegue, filtre e obtenha detalhes completos sobre os produtos em relação a um catálogo em tempo real | Ferramentas do Commerce MCP: Pesquisar produtos Commerce, detalhes do produto, variantes de produto, aspectos do produto e atributos pesquisáveis |
| Comparação de produtos do Adobe Commerce | Comparação lado a lado de dois ou mais produtos nomeados em uma tabela para o Commerce | Ferramentas do Commerce MCP: pesquise produtos da Commerce, detalhes do produto |

As duas habilidades de comércio são recursos exclusivos de catálogo e dependem da integração do MCP do Commerce, que não faz parte da linha de base. Em um concierge não comercial, o Site Advisory e o Product Advisory são executados em relação à Pesquisa da knowledge base criada automaticamente.

![Painel de habilidades de navegação que mostra quatro cartões de habilidade: Consultoria de Produtos, Descoberta do Catálogo Adobe Commerce, Comparação de Produtos Adobe Commerce e Consultoria de Sites](assets/skills-and-integrations-3.png){width="800" zoomable="yes"}

## O que está programado na criação de concierge

Quando um concierge é criado por meio da configuração de um clique, a linha de base é montada para você.

| Conectado na criação | Detalhe |
| --- | --- |
| Knowledge base (dados) | O rastreo inicial cria uma base de conhecimento das 10 a 15 páginas principais do site, encontrada no mapa do site. Este é o armazenamento de conteúdo, não uma habilidade ou integração |
| Pesquisa na knowledge base (integração) | Integração integrada, conectada à base de conhecimento rastreada e usada para pesquisá-la. O rastreo não cria isso; ele aponta o que o rastreo produziu |
| Consultoria do site (habilidade) | Ativo na linha de base, com fio para chamar a Pesquisa da Base de Dados de Conhecimento, que consulta a base de dados de conhecimento rastreada |

## Perguntas frequentes

**Qual é a diferença entre uma habilidade e uma integração?**

Uma integração é uma conexão com uma fonte de dados ou back-end; é o que o concierge pode acessar, como uma base de conhecimento ou um catálogo de comércio em tempo real. Uma habilidade é um comportamento; ela decide o que o porteiro faz, quando faz, e quais integrações ele pode usar.

**Regra geral:** uma integração é uma capacidade; uma habilidade é o julgamento sobre quando e como usar essa capacidade.

**A mesma integração pode ser usada por mais de uma habilidade?**

Sim, e isso é intencional. As ferramentas do Commerce MCP são compartilhadas com a Detecção de Catálogos e a Comparação de Produtos. Criar uma integração uma vez e reutilizá-la em várias habilidades e muitos clientes é a principal eficiência da estrutura 2.0; é isso que remove a criação personalizada por cliente.

**Um profissional pode adicionar um recurso totalmente novo sem engenharia?**

Somente se uma integração para ele já existir no catálogo. Um profissional pode mapear, configurar e instruir livremente qualquer integração existente, ou seja, autoatendimento. Mas se o recurso exigir um back-end ou conector que ainda não existe (uma nova API ou um novo tipo de fonte de dados), essa é uma tarefa de engenharia para criar a integração primeiro. Depois de existir no catálogo, a configuração se torna autoatendimento novamente.

**Qual é a diferença em relação ao prompt de sistema único do BC 1.0?**

Na versão 1.0, o comportamento era orientado por um prompt de sistema grande (o manifesto), que era difícil de editar com segurança e geralmente exigia que a engenharia mudasse. Na versão 2.0, o manifesto ainda existe, mas é composto por peças modulares em vez de escrito como um bloco. Isso é o que torna o comportamento configurável por um profissional e torna as medidas de proteção e instruções individuais legíveis e auditáveis, em vez de serem enterradas em uma única solicitação.

**O que exatamente é criado pelo rastreo anterior?**

O rastreo cria uma base de conhecimento, um armazenamento pesquisável do conteúdo do site, criada a partir das 10 principais a 15 páginas encontradas por meio do mapa do site. Essa é apenas a camada de dados. O rastreo não cria uma habilidade ou uma integração; ele produz o conteúdo sobre o qual atuarão posteriormente.

**Se o rastreo criar a base de dados de conhecimento, qual é a integração da Pesquisa na Base de Dados de Conhecimento?**

A Pesquisa na base de conhecimento é uma integração incorporada cujo trabalho é pesquisar essa base de conhecimento. A base de conhecimento são os dados; a Pesquisa na base de conhecimento é o recurso que a consulta. São duas coisas separadas: um é o conteúdo, o outro é a ferramenta que lê o conteúdo. É um erro comum tratá-las da mesma forma; não são.

**Como o concierge responde a uma pergunta geral na criação, de ponta a ponta?**

Três camadas funcionam em sequência e são mapeadas exatamente de acordo com a habilidade, a integração e o modelo de dados:

- O rastreo inicial cria a base de conhecimento das páginas do site (dados).
- A integração integrada da Pesquisa na base de conhecimento pesquisa essa base de conhecimento (integração).
- A habilidade do Site Advisory está conectada para chamar a Pesquisa da knowledge base (comportamento).
