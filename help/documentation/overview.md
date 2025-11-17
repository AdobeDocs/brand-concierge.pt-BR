---
title: Visão geral do Adobe Brand Concierge
description: Saiba mais sobre o Adobe Brand Concierge, uma solução de descoberta e envolvimento de produtos alimentados por IA para propriedades digitais da marca.
source-git-commit: ee6b768579e620044ca92f5e8b9d06f39a60583d
workflow-type: tm+mt
source-wordcount: '2952'
ht-degree: 1%

---

# Visão geral do Adobe Brand Concierge

O Brand Concierge é um assistente digital alimentado por IA para propriedades digitais da marca que combina IA gerativa com o conteúdo da sua marca e os dados do cliente. Use o Brand Concierge para encontrar produtos, comparar opções e obter respostas por meio de conversas naturais, fornecendo experiências de conversação e personalizadas em jornadas de consumidores e compradores de negócios.

## Visão geral {#overview}

O Brand Concierge é uma solução de descoberta e envolvimento de produtos alimentados por IA para propriedades digitais da marca. Ele ajuda as marcas a fornecer experiências conversacionais e personalizadas em jornadas de consumidores e compradores de negócios, orientando os visitantes desde a exploração até a decisão.

Com o Brand Concierge, você obtém experiências de descoberta multimodal e alimentadas por IA, que o orientam para os produtos certos com recomendações personalizadas e comparações de produtos fáceis de entender. As conversas se adaptam em tempo real às suas necessidades e intenções, fornecendo engajamento contextual e contínuo, independentemente do canal que você usa. E quando você precisa de mais ajuda, o Brand Concierge facilita a conexão perfeita com uma pessoa ativa ou, em cenários B2B, a programação de uma reunião com um representante de vendas.

## Recursos principais {#key-features}

O Brand Concierge tem vários recursos principais, incluindo:

* **Integração guiada:** siga uma configuração passo a passo para obter conhecimento, habilidades e expressão de marca.
* **Integração de conhecimento:** carregue e gerencie fontes como arquivos CSV com links de site.
* **Configurar habilidades** Integre habilidades, como consultoria de produto.
* **Marca de controle:** Ajuste a voz, o tom e a duração da resposta para atender ao padrão e à abordagem de sua marca específica.
* **Visualizar e iterar:** use uma interface de visualização abrangente para simular conversas e realizar ajustes ao vivo.
* **Sistema de comentários:** use um sistema de comentários que permita que os usuários forneçam classificações com miniaturas para cima ou para baixo, além de formulários de comentários detalhados que cubram a cobertura da resposta, o tom, a qualidade e os recursos.
* **Painel do Analytics:** aproveite um painel de análise desenvolvido pelo Customer Journey Analytics para métricas como conversas, sentimento e envolvimento.

## Introdução {#getting-started}

Você pode acessar o Brand Concierge no painel do Adobe Experience Cloud. Para começar, siga a apresentação do usuário pela primeira vez na Página inicial do Brand Concierge. Forneça o nome do seu concierge, adicione fontes de conhecimento, configure as habilidades que deseja usar e defina a Expressão da marca.

## Página inicial {#homepage}

A página inicial do Brand Concierge foi projetada para facilitar o uso e aumentar a eficiência, orientando você pelas etapas essenciais de configuração com uma apresentação dedicada para o usuário pela primeira vez. Um banner principal destacado descreve as principais ações, como especificar o nome e o propósito do concierge, adicionar fontes de conhecimento, configurar habilidades relevantes e definir a expressão da marca. À medida que você avança, um rastreador visual exibe claramente quais componentes da configuração foram concluídos e destaca as tarefas restantes. Para apoiar ainda mais seus esforços, a Página inicial apresenta uma seção inspiradora com vídeos e demonstrações de recursos de concierge, como recomendações de produtos. Você também tem acesso rápido à documentação do Experience League para obter insights técnicos mais detalhados. Quando a configuração estiver concluída, um resumo da configuração fornecerá uma visão abrangente dos seus detalhes, organizada com guias para facilitar ajustes e refinamentos contínuos.

**Elementos-chave**

* **Apresentação de usuário pela primeira vez**: um banner principal com etapas para configurar sua concierge (nome/finalidade, fontes de conhecimento, habilidades, expressão de marca).
* **Rastreador de Progresso**: indicadores visuais de componentes de instalação concluídos vs. pendentes.
* **Seção Inspiradora**: vídeos e demonstrações que mostram recursos de concierge (por exemplo, recomendações de produtos).
* **Links de documentação**: acesso rápido aos recursos do Experience League para obter insights técnicos mais profundos.
* **Resumo da Configuração**: exibição pós-configuração de todos os detalhes, com guias para refinamento.

**Fluxo de trabalho**

1. Para começar a usar a Página inicial, navegue até o banner de apresentação e selecione **[!UICONTROL Introdução]**.
2. Em seguida, forneça um nome para o concierge e defina a finalidade dele (por exemplo, &quot;Recomendar produtos personalizados&quot;).
3. Siga as etapas guiadas para continuar.
4. Quando a configuração for concluída, retorne à Página inicial para monitorar ou editar sua concierge.

>[!TIP]
>
>O Brand Concierge salva seu progresso automaticamente. Uma configuração incompleta pode limitar a funcionalidade, mas não bloqueará as tentativas de visualização.

### Fontes de conhecimento {#knowledge-sources}

Você pode usar Fontes de conhecimento para gerenciar as fontes de dados que alimentam as respostas do seu concierge. Você pode acessar as Fontes de conhecimento depois de fazer upload dos arquivos iniciais. As Fontes de conhecimento têm vários elementos-chave a serem considerados, como:

* **Lista do Source:** A Lista do Source exibe todos os itens carregados, como arquivos CSV com links de site, e indica seu status como processado ou pendente.
* **Interface de Carregamento:** A Interface de Carregamento permite que você arraste e solte ou procure arquivos CSV que contenham URLs, que o sistema rastreará para extrair conhecimento.
* **Opções de Conexão:** As Opções de Conexão permitem vincular fontes de conhecimento específicas a habilidades relevantes para uso mais direcionado.

**Fluxo de trabalho**

1. Na Página Inicial, selecione **[!UICONTROL Adicionar Knowledge Source]**.
2. Em seguida, faça upload de um arquivo CSV e verifique se ele inclui uma coluna para os URLs do site.
3. Aguarde alguns momentos para o processamento. Essa etapa é resolvida rapidamente como atualizações de status em tempo real.
4. Depois de adicionado, retorne à Página inicial. Nesse ponto, você deve ver a nova fonte adicionada à Página inicial.
5. Use a Página inicial para editar ou excluir suas fontes de conhecimento, conforme necessário. Você também pode reconectar uma fonte de conhecimento se ocorrerem alterações.

### Configuração de habilidades {#skills-configuration}

Use a interface de Configuração de Habilidades para definir a experiência de seu concierge, configurando habilidades como o **Product Advisory**. Responda ao questionário para fornecer as entradas que os consultores da Adobe usarão posteriormente para engenharia de prompt. A Configuração de habilidades tem vários elementos-chave a serem considerados, como:

* **Seletor de habilidades:** você pode escolher entre as habilidades disponíveis, como o Product Advisory, para fazer recomendações de produtos.
* **Questionário:** você preencherá uma série de prompts para fornecer conhecimento sobre o produto, regras de negócios, palavras-chave a serem evitadas e conexões de origem.
* **Visualização:** você tem a opção de fazer ajustes ao vivo e ver como seus ajustes afetam as respostas, com links para a página de visualização.
* **Habilitar Reserva de Reunião:** Você pode habilitar os visitantes a agendar reuniões diretamente com representantes comerciais.

**Fluxo de trabalho**

1. Navegue até o rastreador de progresso na Página inicial e selecione **[!UICONTROL Configurar habilidades]**.
2. Selecione uma habilidade (por exemplo, Aviso do produto).
3. Responda às perguntas de configuração subsequentes. (Exemplos de perguntas incluem: &quot;O que o concierge deve saber sobre os produtos?&quot;, &quot;Quais regras de negócios devem ser seguidas?&quot;, &quot;Quais palavras-chave devem ser evitadas&quot;)
4. Conecte fontes de conhecimento relevantes.
5. Habilitar recursos adicionais (reserva de reunião).
6. Enviar para processamento.

### Expressão da marca {#brand-expression}

Você pode usar a interface da Expressão da marca para personalizar a personalidade e o estilo das respostas do seu concierge. Você pode acessar a Expressão da marca nos estágios de configuração ou na barra lateral de visualização para alterações em andamento.

Com o Brand Expression, você pode usar controles deslizantes para personalizar as configurações de voz e tom do concierge. Você pode selecionar entre opções como &quot;Amigável&quot;, &quot;Profissional&quot; e &quot;Energético&quot;. Além disso, você pode configurar os comprimentos de resposta à sua vontade. Você pode definir o concierge para retornar saídas curtas, médias ou longas, dependendo da visão da sua marca.

**Fluxo de trabalho**

1. Na Página inicial, selecione **[!UICONTROL Expressão da marca]**.
2. Em seguida, configure a voz, o tom e a duração de resposta preferencial da sua marca.
3. Selecione **[!UICONTROL Salvar]** para garantir que as alterações sejam refletidas em respostas futuras.

### Pré-visualização e teste {#preview-and-test}

Teste seu concierge antes de iniciá-lo para clientes que usam os modos Visualização e Visualização do testador.

>[!BEGINTABS]

>[!TAB Modo de visualização]

Use o modo de Visualização para simular conversas enquanto faz ajustes em tempo real.

1. Após a configuração, volte para a Página inicial e selecione **[!UICONTROL Visualizar]**.
2. Use a interface de chat para inserir sua query (por exemplo, &quot;Recomende um laptop abaixo de US$ 1000).
3. Revise as respostas do concierge.
4. Use o painel direito para ajustar as configurações de expressão da marca.
5. Selecione **[!UICONTROL Compartilhar]** para gerar um link para os comentários da equipe.

>[!TAB Modo de exibição de testador]

Use a visualização Testador para coletar feedback estruturado sobre o desempenho da portaria e simular a experiência do usuário final.

1. Na visualização, selecione **[!UICONTROL Modo de Exibição de Testador]**.
2. Use a view Testador para simular conversas com usuários finais.
3. Use o mecanismo de aumento e diminuição para classificar cada resposta recebida.
4. Formulário de feedback completo para miniaturas:
   **Cobertura de resposta:** Ela solucionou a intenção?
   **Tom da marca:** Alinhado com a personalidade?
   **Qualidade da resposta:** Clara e estruturada?
   **Recursos de resposta:** acompanhamento útil?
5. Adicione comentários e observações específicas.
6. Envie feedback para revisão do painel.

>[!ENDTABS]

### Feedback {#feedback}

Após os testes, você pode usar a guia feedback na página inicial para fornecer feedback e revisões detalhadas.

A seção de feedback fornece vários recursos importantes para ajudar você a monitorar e avaliar o desempenho do Brand Concierge. Os seguintes elementos estão disponíveis:

* **Instantâneo de Desempenho:** Exibe cartões com um resumo das métricas principais, incluindo o total de conversas, usuários únicos, tendências de sentimentos e taxa de engajamento.
* **Botão Exibir Relatório:** permite abrir um painel ativado pela Customer Journey Analytics para obter acesso detalhado a análises avançadas e métricas de desempenho.
* **Lista de Comentários:** Apresenta uma tabela de sessões de comentários. Você pode clicar em linhas individuais para exibir a transcrição completa do chat para cada sessão.
* **Painel de Feedback:** Mostra cartões de classificação no lado direito da interface. Passar o mouse sobre esses cartões ou clicar neles destacará as partes relevantes da transcrição do chat para facilitar a referência.

**Fluxo de trabalho**

1. Navegue até a página inicial do Brand Concierge e selecione **[!UICONTROL Feedback]**.
2. Use o instantâneo fornecido para exibir informações sobre tendências de alto nível.
3. Para acessar um deep drive habilitado pelo Customer Journey Analytics, selecione **[!UICONTROL Exibir Relatório]**.
4. Você também pode inspecionar o painel em busca de comentários conectados adicionais.
5. Quando terminar, você poderá exportar os insights para uso posterior e refinar seu fluxo de trabalho.

### Configurações  {#configurations}

A guia *[!UICONTROL Configurações]* é uma exibição de resumo somente leitura que você pode usar para revisar a configuração completa da concierge. Isso espelha diretamente a Página inicial após a conclusão da configuração inicial e fornece resumos de seus detalhes, fontes de conhecimento, habilidades e expressão de marca configurada. Você pode usar esse recurso como referência antes de visualizar ou compartilhar sua concierge.

## O que você pode fazer com o Brand Concierge

### Recursos do cliente

O Brand Concierge oferece uma interface conversacional que permite aos clientes encontrar produtos, comparar opções e obter respostas usando linguagem natural. Com recomendações personalizadas, comparações avançadas de produtos e a capacidade de escalonar para um agente ativo, os clientes desfrutam de uma experiência contínua e intuitiva. A interação é flexível — os clientes podem usar texto, voz ou imagens — e cada resposta é baseada na documentação confiável de sua marca e no contexto do cliente.

* Faça perguntas em linguagem natural e receba recomendações personalizadas.
* Comparar produtos lado a lado com exibições visuais.
* Obtenha respostas da documentação da sua marca.
* Alterne para um agente ativo com histórico completo da conversa.

### Recursos empresariais

O Brand Concierge capacita as empresas com recursos avançados de IA conversacional para o engajamento do cliente. Ele ajuda as marcas a impulsionar a conversão, orientando os clientes para os produtos certos, reduz os custos de suporte por meio de respostas instantâneas e precisas, e garante a voz e a conformidade consistentes da marca. Com análises robustas, entrega contínua de IA para humanos e profundas integrações da Adobe, a Brand Concierge otimiza a experiência do cliente e o desempenho da empresa.

* Oriente os clientes para os produtos certos a fim de aumentar a conversão.
* Reduza os custos de suporte com respostas instantâneas e precisas.
* Controle os requisitos de voz, tom e conformidade da marca.
* Acompanhe o desempenho com o painel do Customer Journey Analytics.
* Habilite transmissão contínua de IA para humanos, incluindo agendamento de reuniões.
* Integre com o Adobe Experience Platform e o Experience Manager.

## Casos de uso

A Brand Concierge oferece suporte a casos de uso de B2C e B2B em vários setores.

| Setor | Casos de uso |
|---|---|
| Varejo e comércio eletrônico | Os clientes podem descobrir produtos e receber recomendações personalizadas. O Brand Concierge fornece orientação sobre dimensionamento e ajuste, ajuda os usuários a encontrar presentes adequados e corresponde a estilos ou preferências com base na entrada do cliente. |
| Vendas B2B | A Brand Concierge orienta os clientes por meio de avaliações de produtos, oferece comparações detalhadas de recursos e preços, auxilia na programação de reuniões de vendas e fornece recomendações específicas do setor personalizadas para clientes empresariais. |
| Suporte ao cliente | Os usuários podem receber respostas instantâneas diretamente da base de conhecimento. A Brand Concierge fornece informações sobre políticas e procedimentos, ajuda a solucionar problemas e fornece atualizações sobre o status e o rastreamento do pedido. |
| Viagens e hospitalidade | Os clientes recebem recomendações de destino personalizadas, assistência com itinerários de planejamento, suporte durante todo o processo de reserva e respostas a perguntas de política de viagem. |
| Serviços financeiros | A Brand Concierge oferece comparações de produtos para ajudar os clientes a escolher as soluções financeiras certas, fornece informações de conta, fornece orientação de reconhecimento de conformidade e permite a programação de reuniões com consultores financeiros. |

## Perguntas frequentes

Leia esta seção para obter respostas a perguntas frequentes sobre o Brand Concierge.

### Geral

#### Qual é a diferença entre o Brand Concierge e os chatbots?

O Brand Concierge se diferencia dos chatbots tradicionais por aproveitar a IA gerativa treinada especificamente no conteúdo e nos dados do cliente de sua organização, em vez de depender de respostas com script ou resultados genéricos da Web. Isso permite que o assistente forneça respostas personalizadas com base no comportamento individual do cliente, integre-se profundamente às ferramentas e aos dados da Adobe, aprenda continuamente com cada interação e interprete com precisão a intenção do cliente, além da correspondência básica de palavras-chave.

#### Posso usar o Brand Concierge para B2C e B2B?

Sim. Os casos de uso incluem:

* **B2C:** descoberta de produtos, assistência a compras, suporte ao cliente e recomendações personalizadas.
* **B2B:** Avaliações guiadas, comparações de recursos, agendamento de reuniões, roteamento de representantes de vendas, agendamento de consultas.

#### Quais setores podem usar o Brand Concierge?

O Brand Concierge pode ser usado em diversos setores, inclusive varejo e comércio eletrônico, viagens e hospitalidade, serviços financeiros, saúde (com controles de conformidade), mídia e entretenimento, e tecnologia e software. Basicamente, qualquer setor que ajude os clientes a encontrar informações e tomar decisões pode se beneficiar com a implementação do Brand Concierge.

### Dados e privacidade

#### Os dados do cliente estão seguros?

Sim. A Brand Concierge garante a segurança dos dados do cliente aderindo à conformidade com o GDPR e a CCPA, processando dados na infraestrutura segura da Adobe, fornecendo controle sobre o uso de dados e protegendo as conversas por meio de criptografia e registro de auditoria.

Todas as conversas ocorrem em suas propriedades, não em servidores de terceiros.

#### Quais fontes de dados posso conectar?

Você pode conectar os seguintes tipos de fontes de dados ao Brand Concierge:

| Tipo de Source de dados | Origens/Detalhes Disponíveis |
|------------------|---------------------------|
| **Produto e conteúdo** | Catálogos de produtos<br>Sistemas de inventário<br>Bases de conhecimento e documentação<br>Conteúdo de site via upload de URL CSV<br>Conteúdo do Adobe Experience Manager<br>Dados do Adobe Commerce |
| **Dados do cliente** | Perfis do Adobe Experience Platform<br>Dados de comportamento do Adobe Analytics<br>Atributos de clientes próprios<br>APIs de terceiros (configurado) |
| **Formato de arquivo CSV** | Uma coluna contendo URLs de sites<br>O Brand Concierge rastreia URLs e extrai conteúdo automaticamente<br>Processando atualizações de status em tempo real<br>Vários arquivos CSV podem ser carregados para diferentes áreas de conteúdo |

Todos os dados seguem suas regras de governança.

#### Os clientes podem recusar a personalização?

Sim. Os clientes que recusarem recebem respostas úteis sem personalização comportamental. Você configura o tratamento de recusa para corresponder às suas políticas de privacidade.

### Configuração e controle

#### Como controlar a voz da marca?

Você pode controlar a voz da marca diretamente na interface do usuário configurando elementos como tom (formal a casual), idioma (simples a técnico) e personalidade (por exemplo, útil, entusiasmado ou profissional). Além disso, você pode definir padrões de resposta usando modelos e exemplos, e estabelecer medidas de proteção para aplicar regras de conformidade e limites. Comece com os prompts de referência da Adobe e personalize essas configurações para refletir a identidade exclusiva de sua marca.

#### O que acontece quando o Brand Concierge não pode responder uma pergunta?

Você pode configurar comportamentos de fallback para determinar como o Brand Concierge responde quando não consegue responder uma pergunta. As opções incluem exibir uma mensagem elegante &quot;Não posso ajudar com isso&quot;, sugerir perguntas alternativas, vincular a recursos de autoatendimento ou encaminhar automaticamente a consulta a um agente humano. Escolha o que funciona melhor para sua marca.

#### Posso personalizar o design visual?

Sim. Personalizar todos os elementos visuais, incluindo:

* Cores e marcas
* Fontes e tipografia
* Estilos de botão
* Posicionamento do widget
* Layouts de cartão
* Formatação de resposta

Os SDKs fornecem componentes padrão e opções de personalização completas.

#### Quanto tempo leva a configuração?

A duração da configuração pode depender do seu tipo de implementação. Uma implementação básica que inclui um catálogo de produtos existente, conteúdo de perguntas frequentes padrão e configurações padrão pode levar de 3 a 5 dias para ser configurada. Por outro lado, implementações avançadas com integrações personalizadas, personalização abrangente, fluxos de trabalho complexos e regras de conformidade personalizadas podem levar de 2 a 4 semanas para serem concluídas.

#### Como funcionam a pré-visualização e o teste?

O Brand Concierge inclui ferramentas de teste integradas:

| Ferramenta de teste | Recursos |
|--------------|----------|
| **Modo de visualização** | Simular conversas com o cliente<br>Ajustar configurações em tempo real<br>Ver alterações instantaneamente<br>Compartilhar links de visualização com a sua equipe |
| **Modo de Exibição de Testador** | Classifique as respostas com miniaturas para cima/para baixo<br>Forneça feedback estruturado em 4 categorias<br>Adicione comentários detalhados<br>Rastreie feedback no painel |

Todos os testes acontecem antes da implantação para os clientes.

#### Os clientes podem agendar reuniões com nossa equipe?

Sim, os clientes podem agendar reuniões com sua equipe usando a habilidade Reserva de Reunião. Para ativar esse recurso, ative a habilidade na Configuração de habilidades, defina intenções de ativação (como &quot;falar com as vendas&quot;), conecte seu calendário ou sistema de agendamento e defina sua disponibilidade e tipos de reunião. Após a configuração, os clientes podem solicitar reuniões durante conversas, e o Brand Concierge facilitará o processo de agendamento sem exigir que saiam do bate-papo.

#### Quem gerencia a engenharia de prompts?

Os consultores da Adobe lidam com a engenharia de prompts em segundo plano:

1. Você responde às perguntas de configuração na página Habilidades.
2. Forneça conhecimento sobre o produto, regras de negócios e evite palavras-chave.
3. Envie suas entradas.
4. Os consultores da Adobe usam suas respostas para elaborar prompts otimizados.
5. As alterações são refletidas automaticamente no seu concierge.

Isso garante que seu concierge use padrões de prompt de IA de práticas recomendadas, mantendo os requisitos específicos da sua marca.

### Desempenho e análise

#### Como medir o sucesso?

É possível medir o sucesso usando o painel do Brand Concierge. Use o painel para rastrear métricas como:

| Métrica | O que rastreia |
|--------|----------------|
| **Engajamento** | Volume de conversa, duração da sessão |
| **Satisfação** | Pontuações de sentimento, classificações de feedback |
| **Conversão** | Taxas de compra para os serviços assistidos vs. não assistidos |
| **Tópicos** | Perguntas e solicitações mais comuns |
| **Transferência** | Taxas de escalonamento e motivos |
| **Desempenho** | Precisão da resposta, tempo de resolução |

Também é possível integrar o com o Adobe Analytics para fazer uma análise mais profunda.

#### O que devo fazer se o sentimento cair?

Se você notar uma queda no sentimento, investigue as causas subjacentes revisando consultas com falha recentes, verificando lacunas de conteúdo, analisando feedback negativo, testando o tom apropriado e verificando quaisquer problemas técnicos. Depois que as causas raiz forem identificadas, resolva-as imediatamente e continue a monitorar melhorias.

### Integração e suporte técnico

#### Preciso de outros produtos da Adobe?

Não, mas elas melhoram o desempenho:

| Opção de integração | Recursos |
|-------------------|--------------|
| **Independente** | Funciona com seu catálogo de produtos e conteúdo |
| **Com Adobe Experience Platform** | Perfis de clientes unificados<br>Personalização avançada<br>Consistência entre canais |
| **Com Adobe Commerce** | Estoque em tempo real<br>Histórico de pedidos<br>Integração com o carrinho |
| **Com Adobe Experience Manager** | Gerenciamento de conteúdo<br>Atualizações dinâmicas<br>Suporte a vários sites |

#### E se meu site não estiver no Adobe?

O Brand Concierge funciona com qualquer plataforma. O JavaScript SDK é integrado a qualquer site, e os SDKs móveis funcionam com qualquer back-end de aplicativo.

#### Como funciona a transferência do agente?

Quando a entrega do agente é acionada, a Brand Concierge transfere o histórico completo da conversa, o perfil e a ID do cliente, a intenção identificada, os detalhes dos produtos discutidos e todas as tentativas de resolução para o agente. Isso garante que os agentes tenham um contexto completo e possam continuar a conversa perfeitamente, sem exigir que os clientes repitam as informações.

#### Posso oferecer suporte a vários idiomas?

Sim. Configure o suporte de idioma por assistente com base na sua base de clientes. O Brand Concierge detecta o idioma do cliente e responde de acordo.
