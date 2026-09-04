---
title: Documentação do produto
description: Saiba como configurar e usar os principais recursos do Brand Concierge.
role: User,Admin
level: Beginner
TQID: https://experienceleague.adobe.com/Ob3NAKyD929Ije-Y7UPO1hMfDYDi-UJ0gINpGlxiYGM
product_v2:
  - id: b6ee73fe-bdc6-47d9-99a2-80194514dd40
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: 2047
ht-degree: 1%

---

# Ajuda do Brand Concierge

Saiba como configurar e usar os principais recursos do Brand Concierge. Encontre respostas para perguntas comuns sobre configuração, integração de dados, privacidade, personalização, medição de desempenho e requisitos técnicos.

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

Você pode acessar o Brand Concierge no painel da Adobe Experience Cloud. Em um nível superior, você executa estas tarefas:

1. [Criar um concierge](#homepage) a partir da URL de um site. Uma fonte de conhecimento inicial, expressão de marca e habilidade da linha de base são geradas automaticamente.
1. [Revise e refine as fontes de conhecimento](#knowledge-sources) conforme necessário.
1. [Configure habilidades adicionais](#skills-configuration) além da habilidade da linha de base.
1. [Ajuste sua Expressão de marca](#brand-expression) se os padrões gerados precisarem de alterações.

Para assistir a um tutorial em vídeo, consulte [Criar sua primeira concierge](../getting-started/create-first-concierge.md)

As seções a seguir descrevem cada tarefa e as opções da interface em detalhes.

## Criar um concierge {#homepage}

Criar um concierge a partir de um único URL do site é o ponto de partida recomendado para um usuário pela primeira vez. A Página inicial do Brand Concierge lê o site e cria uma linha de base de trabalho automaticamente: nenhuma configuração manual é necessária para começar.

Conforme a configuração é concluída, um resumo da configuração fornece uma visualização abrangente dos detalhes, organizada com guias para facilitar ajustes e refinamentos contínuos. A Página inicial também apresenta uma seção inspiradora com vídeos e demonstrações de recursos de concierge, como recomendações de produtos e acesso rápido à documentação do Experience League para obter insights técnicos mais aprofundados.

**Elementos-chave**

* **Criação com um clique**: insira uma URL de site para gerar automaticamente uma expressão de marca inicial, um perfil de marca, instruções, medidas de proteção, uma fonte de conhecimento e uma habilidade de linha de base.
* **Revisão guiada**: cada elemento gerado é apresentado para revisão antes de ser salvo, portanto, nada fica ativo sem uma chance de ajustá-lo primeiro.
* **Seção Inspiradora**: vídeos e demonstrações que mostram recursos de concierge (por exemplo, recomendações de produtos).
* **Links de documentação**: acesso rápido aos recursos do Experience League para obter insights técnicos mais profundos.
* **Resumo da Configuração**: exibição pós-configuração de todos os detalhes, com guias para refinamento.

**Para criar uma concierge**

1. Insira a URL do site da marca e selecione **[!UICONTROL Criar]**.
1. Revise a expressão da marca gerada (como formalidade, calor, jovialidade e energia) e ajuste conforme necessário.
1. Analise o perfil de marca gerado, incluindo metas, produtos e serviços, público-alvo e diferenciais, e ajuste conforme necessário.
1. Revise as instruções, as medidas de proteção e as sugestões geradas e ajuste conforme necessário.
1. Selecione **[!UICONTROL Salvar]**. O concierge está pronto para testar na visualização.

Para obter detalhes completos sobre este fluxo, incluindo o que é configurado automaticamente, consulte [Gerenciar uma concierge](./concierge-management/concierge-management.md).

>[!TIP]
>
>O Brand Concierge salva seu progresso automaticamente. Uma configuração incompleta pode limitar a funcionalidade, mas não bloqueará as tentativas de visualização.

### Fontes de conhecimento {#knowledge-sources}

As [!UICONTROL Fontes de Conhecimento] ajudam você a gerenciar as fontes de dados que alimentam as respostas do seu concierge. Uma fonte de conhecimento inicial é criada automaticamente quando você cria um concierge a partir do URL de um site; use essa área para revisá-la ou adicionar mais. [!UICONTROL Fontes de Conhecimento] tem vários elementos-chave a serem considerados, como:

* **Lista do Source:** Exibe todos os itens carregados, como arquivos CSV com links de site, e indica seu status como processado ou pendente.
* **Interface de Carregamento:** permite que você arraste e solte ou procure arquivos CSV que contenham URLs, que o sistema rastreará por extrair conhecimento.
* **Opções de Conexão:** permite que você vincule fontes de conhecimento específicas a habilidades relevantes para uso mais direcionado.

**Para adicionar uma fonte de conhecimento**

1. Na Página inicial, clique em **[!UICONTROL Fontes de conhecimento]**.

1. Nomeie a fonte de conhecimento.

1. Clique em **[!UICONTROL Adicionar]** para carregar um arquivo CSV.

   Certifique-se de que inclua uma coluna para URLs de site.

1. Aguarde alguns momentos para o processamento.

   Essa etapa é resolvida rapidamente como atualizações de status em tempo real.

1. Depois de adicionado, retorne à Página inicial.

   Nesse ponto, você deve ver a nova fonte adicionada à Página inicial.

   Use a Página inicial para editar ou excluir suas fontes de conhecimento, conforme necessário. Você também pode reconectar uma fonte de conhecimento se ocorrerem alterações.

Para obter o conjunto completo de tipos de fonte de conhecimento e etapas de solução de problemas, consulte [Criar e gerenciar fontes de conhecimento para o Brand Concierge](./knowledge-sources/knowledge-sources.md).

### Configurar habilidades {#skills-configuration}

As habilidades determinam o que um concierge pode fazer pelos visitantes, como o **Product Advisory** para recomendações de produtos ou o **Site Advisory** para perguntas gerais sobre marcas. Selecione **[!UICONTROL Procurar Habilidades]** para exibir o catálogo de habilidades disponível e ativar as habilidades necessárias para a concierge.

* **Catálogo de habilidades:** escolha entre as habilidades disponíveis, como o Site Advisory, o Product Advisory e as habilidades que oferecem suporte à reserva da reunião ou ao chat ao vivo com um representante de vendas.
* **Configuração:** Para cada habilidade, defina seu nome, descrição e as intenções (frases ou tópicos de gatilho) que devem chamá-la.
* **Integrações:** anexe a integração que uma habilidade precisa para fazer seu trabalho, ou selecione **[!UICONTROL Usar recomendado]** para que o Composer selecione uma automaticamente.
* **Visualização:** teste as alterações imediatamente na visualização ao vivo.

**Para configurar habilidades**

1. Na concierge, selecione **[!UICONTROL Procurar habilidades]**.
1. Selecione uma habilidade para ativar (por exemplo, Aviso de produto).
1. Defina o nome, a descrição e as intenções da habilidade.
1. Anexe a integração necessária ou selecione **[!UICONTROL Usar recomendado]**.
1. Selecione **[!UICONTROL Salvar]** e teste a alteração na visualização ao vivo.

Para ver o catálogo completo de habilidades e integração, consulte a [Estrutura de habilidades e integrações](./skills-and-integrations.md).

### Expressão da marca {#brand-expression}

A expressão da marca controla a personalidade e o estilo das respostas do seu porteiro. Ele é redigido automaticamente quando você cria um concierge, e você pode acessá-lo posteriormente a partir das configurações de Tom e voz do concierge para alterações contínuas.

A expressão da marca é definida usando atributos como formalidade, calor, jovialidade e energia, em vez de um único estilo nomeado. Você também pode configurar a duração da resposta (curta, média ou longa) para corresponder à preferência da sua marca.

**Para personalizar sua expressão de marca**

1. Na concierge, abra **[!UICONTROL Tom e Voz]**.
2. Ajuste a formalidade, o calor, a jovialidade, a energia e a duração preferida da resposta.
3. Selecione **[!UICONTROL Salvar]** para garantir que as alterações sejam refletidas em respostas futuras.

### Visualizar e testar {#preview-and-test}

Teste seu concierge antes de iniciá-lo para clientes que usam os modos Visualização e Visualização do testador.

>[!BEGINTABS]

>[!TAB Modo de visualização]

Use o modo de Visualização para simular conversas enquanto faz ajustes em tempo real.

1. Após a configuração, navegue de volta para a Página inicial e clique em **[!UICONTROL Visualizar]**.
1. Use a interface de chat para inserir sua consulta (por exemplo, _Recomendamos um laptop abaixo de US$ 1000_).
1. Revise as respostas do concierge.
1. Use o painel direito para ajustar as configurações de expressão da marca.
1. Clique em **[!UICONTROL Compartilhar]** para gerar um link para os comentários da equipe.

>[!TAB Modo de exibição de testador]

Use a visualização Testador para coletar feedback estruturado sobre o desempenho da portaria e simular a experiência do usuário final.

1. Na visualização, clique em **[!UICONTROL Exibição do testador]**.
1. Use a view Testador para simular conversas com usuários finais.
1. Use o mecanismo de aumento e diminuição para classificar cada resposta recebida.
1. Formulário de feedback completo para miniaturas:
   **Cobertura de resposta:** Ela solucionou a intenção?
   **Tom da marca:** Alinhado com a personalidade?
   **Qualidade da resposta:** Clara e estruturada?
   **Recursos de resposta:** acompanhamento útil?
1. Adicione comentários e observações específicas.
1. Envie feedback para revisão do painel.

>[!ENDTABS]

### Feedback {#feedback}

Após os testes, você pode usar a guia feedback na página inicial para fornecer feedback e revisões detalhadas.

A seção de feedback fornece vários recursos importantes para ajudar você a monitorar e avaliar o desempenho do Brand Concierge. Os seguintes elementos estão disponíveis:

* **Instantâneo de Desempenho:** Exibe cartões com um resumo das métricas principais, incluindo o total de conversas, usuários únicos, tendências de sentimento e taxa de participação.
* **Botão Exibir Relatório:** permite abrir um painel ativado pela Customer Journey Analytics para obter acesso detalhado a análises avançadas e métricas de desempenho.
* **Lista de Comentários:** Apresenta uma tabela de sessões de comentários. Você pode clicar em linhas individuais para exibir a transcrição completa do chat para cada sessão.
* **Painel de Feedback:** Mostra cartões de classificação no lado direito da interface. Passar o mouse sobre esses cartões ou clicar neles destacará as partes relevantes da transcrição do chat para facilitar a referência.

**Para enviar comentários**

1. Navegue até a página inicial do Brand Concierge e selecione **[!UICONTROL Feedback]**.
1. Use o instantâneo fornecido para exibir informações sobre tendências de alto nível.
1. Para acessar um deep drive habilitado pelo Customer Journey Analytics, selecione **[!UICONTROL Exibir Relatório]**.
1. Você também pode inspecionar o painel em busca de comentários conectados adicionais.
1. Quando terminar, você poderá exportar os insights para uso posterior e refinar seu fluxo de trabalho.

### Configurações {#configurations}

A guia _[!UICONTROL Configurações]_ é uma exibição de resumo somente leitura que você pode usar para revisar a configuração completa da concierge. Isso espelha diretamente a Página inicial após a conclusão da configuração inicial e fornece resumos de seus detalhes, fontes de conhecimento, habilidades e expressão de marca configurada. Você pode usar esse recurso como referência antes de visualizar ou compartilhar sua concierge.

## O que você pode fazer com o Brand Concierge

Saiba mais sobre os recursos do cliente, os recursos comerciais e os casos de uso do Brand Concierge.

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

## Divulgação da IA de conversa {#disclosure}

Para fornecer uma experiência transparente e confiável, os usuários do Adobe Brand Concierge são responsáveis por adicionar uma breve divulgação em sua experiência de conversa. Essa divulgação ajuda os usuários finais a entender como a conversa funciona e como suas informações podem ser usadas.

**O que a divulgação deve cobrir**

Sua divulgação da conversa deve comunicar claramente três coisas aos usuários finais.

1. _A conversa usa IA gerativa_

   Informe aos usuários que as respostas são geradas pela IA para que eles entendam que estão interagindo com um sistema automatizado.

1. _As conversas podem ser revisadas para melhorar a experiência_

   Os usuários devem ser informados de que você (o cliente) e seus provedores de serviço podem acessar as conversas para ajudar a personalizar as respostas e melhorar a qualidade e o desempenho da conversa.

1. _Usar a IA de conversação significa concordar com esse uso_

Esclareça que, ao continuar usando a IA conversacional, os usuários estão concordando com esse processamento de seus dados de conversa.

**Exemplo (somente para fins de referência)**

`"This conversational AI uses generative AI to help respond to you. Conversations may be recorded by [customer] and/or our service provider and used to help operate and improve services, make your interactions with us better, and provide a more personalized experience. By continuing to conversational AI you agree to this processing of data."`

Você pode adaptar o texto de acordo com a voz da sua marca e a experiência do usuário, desde que os pontos principais acima sejam comunicados claramente.

**Por que isso é importante**

Ser inovador sobre como a IA conversacional funciona ajuda a definir as expectativas certas para os usuários e cria confiança em experiências alimentadas por IA.
