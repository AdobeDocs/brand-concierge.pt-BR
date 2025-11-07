---
title: Visão geral do Adobe Brand Concierge
description: Saiba mais sobre o Adobe Brand Concierge, uma solução de descoberta e envolvimento de produtos alimentados por IA para propriedades digitais da marca.
source-git-commit: 2fa41c76a52d9e2ca30801cab842aadd98b69be0
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 1%

---

# Visão geral do Adobe Brand Concierge

O Adobe Brand Concierge capacita você a criar experiências de conversação personalizadas e orientadas por IA que se alinhem à voz, ao conhecimento e às metas da sua marca.

## Visão geral {#overview}

O Brand Concierge é uma solução de descoberta e envolvimento de produtos alimentados por IA para propriedades digitais da marca. Ele ajuda as marcas a fornecer experiências conversacionais e personalizadas em jornadas de consumidores e compradores de negócios, orientando os visitantes desde a exploração até a decisão.

**Benefícios**

* Experiências de descoberta multimodal alimentadas por IA com recomendações guiadas e comparações de produtos

* Experiências de conversa que se adaptam em tempo real à intenção do cliente, criando engajamento contextual e contínuo entre canais

* Transição contínua de IA para pessoa, incluindo escalonamento para uma pessoa ativa ou agendamento de uma reunião com um representante de vendas para B2B

## Recursos {#features}

**Configurando o Concierge**

* **Integração guiada**: configuração passo a passo do conhecimento, das habilidades e da expressão de marca.

* **Integração de Conhecimento**: carregue e gerencie fontes como arquivos CSV com links de sites.

* **Configuração de habilidade**: habilidades pré-criadas (por exemplo, consultoria de produto)

* **Controles de marca**: voz, tom e duração de resposta ajustáveis.

* **Modo de Visualização**: Simular conversas com ajustes ao vivo.

* **Sistema de feedback**: aumenta/diminui as classificações com formulários detalhados em cobertura, tom, qualidade e recursos.

* **Painel do Analytics**: baseado na tecnologia do Customer Journey Analytics (CJA) para métricas como conversas, sentimentos e envolvimento.

## Introdução {#getting-started}

1. Acesse o Brand Concierge pelo painel do Adobe Experience Cloud.

1. Siga a apresentação do usuário pela primeira vez na página inicial.

1. Configuração completa: nomeie o concierge, adicione conhecimento, configure habilidades e defina a expressão da marca.

1. Visualizar, testar e iterar com base em comentários.

**O que você deve saber**

* Todas as configurações podem ser editadas após a configuração para atender às necessidades da marca.

## Página inicial {#homepage}

A página inicial serve como hub central para o Brand Concierge. Após o primeiro logon, ele apresenta uma apresentação guiada para simplificar a configuração. À medida que você avança, ele é atualizado para mostrar o status de conclusão, conteúdo inspirador e links rápidos.

**Elementos-chave**

* **Apresentação de usuário pela primeira vez**: um banner principal com etapas para configurar sua concierge (nome/finalidade, fontes de conhecimento, habilidades, expressão de marca).

* **Rastreador de Progresso**: indicadores visuais de componentes de instalação concluídos vs. pendentes.

* **Seção Inspiradora**: vídeos e demonstrações que mostram recursos de concierge (por exemplo, recomendações de produtos).

* **Links de documentação**: acesso rápido aos recursos do Experience League para obter insights técnicos mais profundos.

* **Resumo da Configuração**: exibição pós-configuração de todos os detalhes, com guias para refinamento.

### Fluxo de trabalho {#workflow}

1. Role até o banner de apresentação e clique em **Introdução**.

1. Nomeie seu concierge e defina seu propósito (por exemplo, &quot;Recomendar produtos personalizados&quot;).

1. Prossiga pelas etapas vinculadas (detalhadas nas páginas subsequentes).

1. Após a configuração, volte aqui para monitorar ou editar.

**O que você deve saber**

* O progresso é salvo automaticamente; configurações incompletas não bloquearão visualizações, mas poderão limitar a funcionalidade.

### Página Fontes de conhecimento {#knowledge-sources-page}

Essa página lateral gerencia fontes de dados que potencializam as respostas da concierge. Ele é acessível após fazer upload dos arquivos iniciais e lista todas as fontes criadas.

**Elementos-chave**

* **Lista do Source**: exibe os itens carregados (por exemplo, arquivos CSV com links de sites) com status (processado/pendente).

* **Carregar Interface**: arraste e solte ou procure arquivos CSV contendo URLs para rastrear conhecimento.

* **Opções de Conexão**: vincular fontes a habilidades específicas para uso direcionado.

**Fluxo de trabalho**

1. Na home page, selecione **Adicionar Knowledge Source**.

1. Carregar um arquivo CSV (formato: uma coluna para URLs de site).

1. Aguarde o processamento (normalmente rápido, atualizações de status em tempo real).

1. Depois de adicionado, volte à página inicial — a origem aparece aqui para gerenciamento.

1. Edite ou exclua fontes conforme necessário; reconecte-se às habilidades se ocorrerem alterações.

### Página Configuração de habilidades {#skills-configuration-page}

Defina a experiência do porteiro configurando habilidades (por exemplo, consultoria de produto). Esta página usa um questionário para coletar entradas, que os consultores da Adobe usam para engenharia de prompt.

**Elementos-chave**

* **Seletor de habilidades**: escolha entre as habilidades disponíveis (por exemplo, Consultoria de produtos para recomendações).

* **Questionário**: série de prompts para conhecimento do produto, regras de negócios, evitar palavras-chave e conexões de origem.

* **Painel de Visualização**: ajustes ao vivo opcionais para ver os impactos da resposta (links para a página de visualização).

* **Habilitar Reserva de Reunião**: permitir que o visitante agende uma reunião diretamente com representantes comerciais

**Fluxo de trabalho**

1. No rastreador de progresso da página inicial, clique em **Configurar habilidades**.

1. Selecione uma habilidade (por exemplo, Aviso do produto).

1. Responder perguntas:

   * O que o concierge deve saber sobre os produtos? (por exemplo, recursos, preços).
   * Regras comerciais? (por exemplo, &quot;Priorizar opções ecológicas&quot;).
   * Palavras-chave a serem evitadas? (por exemplo, &quot;esgotado&quot;).

1. Conecte fontes de conhecimento relevantes.

1. Habilite a reserva da reunião clicando em adicionar e defina as regras de ativação (por exemplo, intenções para as quais agendar uma opção de reunião a ser agendada).

1. Enviar — os consultores refinam em segundo plano.

### Página de expressão da marca {#brand-expression-page}

Personalize a personalidade e o estilo das respostas do seu porteiro. Essa página pode ser acessada na barra lateral de configuração ou pré-visualização para ajustes contínuos.

**Elementos-chave**

* **Configurações de Voz e Tom**: menus suspensos/controles deslizantes para opções como &quot;Amigável&quot;, &quot;Profissional&quot; ou &quot;Energético&quot;.

* **Duração da Resposta**: controle deslizante para saídas curtas/médias/longas.

* **Botão Atualizar**: aplica as alterações instantaneamente nas visualizações.

**Fluxo de trabalho**

1. Na página inicial, selecione **Expressão da Marca**.

1. Definir voz (por exemplo, &quot;Conversacional&quot;), tom (por exemplo, &quot;Empático&quot;) e comprimento (por exemplo, &quot;Conciso&quot;).

1. Salvar — as alterações serão refletidas em todas as respostas futuras.

1. Reveja o painel de visualização para testes A/B.

### Visualizar página {#preview-page}

Teste seu concierge em um ambiente de conversa simulado. Esta página permite interação em tempo real e ajustes rápidos.

**Elementos-chave**

* **Interface de Conversa**: janela de chat para entradas de usuário e respostas de concierge.

* **Painel à Direita**: acesso flexível às configurações de expressão da marca (voz, tom, comprimento).

* **Botão Compartilhar**: no cabeçalho, gera um link para o feedback da equipe.

* **Alternar para Modo de Exibição de Testador**: alternar para simulação de usuário final.

**Fluxo de trabalho**

1. Na página inicial, clique em **Visualizar** após a instalação.

1. Comece a digitar consultas (por exemplo, &quot;Recomende um notebook abaixo de US$ 1.000&quot;).

1. Ajuste as configurações no painel - consulte atualizações instantâneas no bate-papo.

1. Use compartilhar para enviar o link de visualização.

1. Alternar exibições ou sair para a página inicial.

### Exibição do testador {#tester-view}

Um modo dedicado na visualização para coletar feedback. Simula a experiência do usuário final com ferramentas de classificação.

**Elementos-chave**

* **Chat de interação**: o mesmo que a visualização, mas com miniaturas para cima/para baixo após cada resposta.

* **Formulário de Feedback**: acionado por miniaturas para baixo/para cima; quatro categorias com sim/não e comentários.

   * Cobertura e correção de resposta: abordou a intenção?
   * Tom de marca: alinhado com a personalidade?
   * Qualidade da resposta: clara e estruturada?
   * Feedback do recurso de resposta: acompanhamentos úteis?

**Fluxo de trabalho**

1. Na visualização, alterne para **Modo de Exibição do Testador**.

1. Conversor e taxa de respostas (polegares para cima/para baixo).

1. Para baixo, preencha as categorias do formulário e adicione comentários.

1. Enviar — roteiros de feedback para o painel do profissional de marketing.

1. Voltar para visualização.

### Guia Feedback {#feedback-tab}

Após os testes, essa guia na página inicial fornece visões gerais de desempenho e revisões detalhadas. Ideal para iteração.

**Elementos-chave**

* **Instantâneo de Desempenho**: cartões do total de conversas, usuários únicos, tendências de sentimento, taxa de engajamento.

* **Botão Exibir Relatório**: abre um painel habilitado para CJA com métricas avançadas.

* **Lista de Comentários**: tabela de sessões; clique nas linhas para obter a transcrição completa do chat.

* **Painel de Comentários**: cartões do lado direito para classificações; passe o mouse/clique destaca as referências de bate-papo.

**Fluxo de trabalho**

1. Na página inicial, selecione a guia **Comentários**.

1. Analise o instantâneo de tendências de alto nível.

1. Clique em **Exibir relatório** para aprofundar o CJA.

1. Lista de navegação: selecione uma linha para carregar o bate-papo; inspecione o painel para ver se há comentários conectados.

1. Exportar ou anotar insights para refinamentos.

### Guia Configuração {#configuration-tab}

Uma exibição de resumo somente leitura (com links de edição) da configuração completa da concierge. Espelha a página inicial após a configuração.

**Elementos-chave**

* **Seção de Detalhes**: nome, finalidade, status geral.

* **Fontes de Conhecimento**: lista com links para página universal.

* **Habilidades**: itens configurados com botões de edição.

* **Expressão da marca**: resumo das configurações atuais.

**Fluxo de trabalho**

1. Na página inicial, continue na guia **Configuração** (pós-configuração padrão).

1. Verificar seções para verificar se estão completas.

1. Clique nos ícones de edição para ir para páginas relevantes (por exemplo, _habilidades_).

1. Use como referência antes das visualizações ou compartilhamentos.
