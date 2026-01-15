---
title: Perguntas frequentes
description: Obtenha respostas para perguntas frequentes sobre o Adobe Brand Concierge.
role: User,Admin
level: Beginner
source-git-commit: 0f010472e3f49c5d84e9875a33215d56e020bef8
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 1%

---

# Perguntas frequentes

Leia esta seção para obter respostas a perguntas frequentes sobre o Brand Concierge.

## Geral

### Qual é a diferença entre o Brand Concierge e os chatbots?

O Brand Concierge se diferencia dos chatbots tradicionais por aproveitar a IA gerativa treinada especificamente no conteúdo e nos dados do cliente de sua organização, em vez de depender de respostas com script ou resultados genéricos da Web. Isso permite que o assistente forneça respostas personalizadas com base no comportamento individual do cliente, integre-se profundamente às ferramentas e aos dados da Adobe, aprenda continuamente com cada interação e interprete com precisão a intenção do cliente, além da correspondência básica de palavras-chave.

### Posso usar o Brand Concierge para B2C e B2B?

Sim. Os casos de uso incluem:

* **B2C:** descoberta de produtos, assistência a compras, suporte ao cliente e recomendações personalizadas.
* **B2B:** Avaliações guiadas, comparações de recursos, agendamento de reuniões, roteamento de representantes de vendas, agendamento de consultas.

### Quais setores podem usar o Brand Concierge?

O Brand Concierge pode ser usado em diversos setores, inclusive varejo e comércio eletrônico, viagens e hospitalidade, serviços financeiros, saúde (com controles de conformidade), mídia e entretenimento, e tecnologia e software. Basicamente, qualquer setor que ajude os clientes a encontrar informações e tomar decisões pode se beneficiar com a implementação do Brand Concierge.

## Dados e privacidade

### Os dados do cliente estão seguros?

Sim. A Brand Concierge garante a segurança dos dados do cliente aderindo à conformidade com o GDPR e a CCPA, processando dados na infraestrutura segura da Adobe, fornecendo controle sobre o uso de dados e protegendo as conversas por meio de criptografia e registro de auditoria.

Todas as conversas ocorrem em suas propriedades, não em servidores de terceiros.

### Quais fontes de dados posso conectar?

Você pode conectar os seguintes tipos de fontes de dados ao Brand Concierge:

| Tipo de Source de dados | Origens/Detalhes Disponíveis |
|------------------|---------------------------|
| **Produto e conteúdo** | Catálogos de produtos<br>Sistemas de inventário<br>Bases de conhecimento e documentação<br>Conteúdo de site via upload de URL CSV<br>Conteúdo do Adobe Experience Manager<br>Dados do Adobe Commerce |
| **Dados do cliente** | Perfis do Adobe Experience Platform<br>Dados de comportamento do Adobe Analytics<br>Atributos de clientes próprios<br>APIs de terceiros (configurado) |
| **Formato de arquivo CSV** | Uma coluna contendo URLs de sites<br>O Brand Concierge rastreia URLs e extrai conteúdo automaticamente<br>Processando atualizações de status em tempo real<br>Vários arquivos CSV podem ser carregados para diferentes áreas de conteúdo |

Todos os dados seguem suas regras de governança.

### Os clientes podem recusar a personalização?

Sim. Os clientes que recusarem recebem respostas úteis sem personalização comportamental. Você configura o tratamento de recusa para corresponder às suas políticas de privacidade.

## Configuração e controle

### Como controlar a voz da marca?

Você pode controlar a voz da marca diretamente na interface do usuário configurando elementos como tom (formal a casual), idioma (simples a técnico) e personalidade (por exemplo, útil, entusiasmado ou profissional). Além disso, você pode definir padrões de resposta usando modelos e exemplos, e estabelecer medidas de proteção para aplicar regras de conformidade e limites. Comece com os prompts de referência da Adobe e personalize essas configurações para refletir a identidade exclusiva de sua marca.

### O que acontece quando o Brand Concierge não pode responder uma pergunta?

Você pode configurar comportamentos de fallback para determinar como o Brand Concierge responde quando não consegue responder uma pergunta. As opções incluem exibir uma mensagem elegante &quot;Não posso ajudar com isso&quot;, sugerir perguntas alternativas, vincular a recursos de autoatendimento ou encaminhar automaticamente a consulta a um agente humano. Escolha o que funciona melhor para sua marca.

### Posso personalizar o design visual?

Sim. Personalizar todos os elementos visuais, incluindo:

* Cores e marcas
* Fontes e tipografia
* Estilos de botão
* Posicionamento do widget
* Layouts de cartão
* Formatação de resposta

Os SDKs fornecem componentes padrão e opções de personalização completas.

### Quanto tempo leva a configuração?

A duração da configuração pode depender do seu tipo de implementação. Uma implementação básica que inclui um catálogo de produtos existente, conteúdo de perguntas frequentes padrão e configurações padrão pode levar de 3 a 5 dias para ser configurada. Por outro lado, implementações avançadas com integrações personalizadas, personalização abrangente, fluxos de trabalho complexos e regras de conformidade personalizadas podem levar de 2 a 4 semanas para serem concluídas.

### Como funcionam a pré-visualização e o teste?

O Brand Concierge inclui ferramentas de teste integradas:

| Ferramenta de teste | Recursos |
|--------------|----------|
| **Modo de visualização** | Simular conversas com o cliente<br>Ajustar configurações em tempo real<br>Ver alterações instantaneamente<br>Compartilhar links de visualização com a sua equipe |
| **Modo de Exibição de Testador** | Classifique as respostas com miniaturas para cima/para baixo<br>Forneça feedback estruturado em 4 categorias<br>Adicione comentários detalhados<br>Rastreie feedback no painel |

Todos os testes acontecem antes da implantação para os clientes.

### Os clientes podem agendar reuniões com nossa equipe?

Sim, os clientes podem agendar reuniões com sua equipe usando a habilidade Reserva de Reunião. Para ativar esse recurso, ative a habilidade na Configuração de habilidades, defina intenções de ativação (como &quot;falar com as vendas&quot;), conecte seu calendário ou sistema de agendamento e defina sua disponibilidade e tipos de reunião. Após a configuração, os clientes podem solicitar reuniões durante conversas, e o Brand Concierge facilitará o processo de agendamento sem exigir que saiam do bate-papo.

### Quem gerencia a engenharia de prompts?

Os consultores da Adobe lidam com a engenharia de prompts em segundo plano:

1. Você responde às perguntas de configuração na página Habilidades.
1. Forneça conhecimento sobre o produto, regras de negócios e evite palavras-chave.
1. Envie suas entradas.
1. Os consultores da Adobe usam suas respostas para elaborar prompts otimizados.
1. As alterações são refletidas automaticamente no seu concierge.

Isso garante que seu concierge use padrões de prompt de IA de práticas recomendadas, mantendo os requisitos específicos da sua marca.

## Desempenho e análise

### Como medir o sucesso?

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

### O que devo fazer se o sentimento cair?

Se você notar uma queda no sentimento, investigue as causas subjacentes revisando consultas com falha recentes, verificando lacunas de conteúdo, analisando feedback negativo, testando o tom apropriado e verificando quaisquer problemas técnicos. Depois que as causas raiz forem identificadas, resolva-as imediatamente e continue a monitorar melhorias.

## Integração e suporte técnico

### Preciso de outros produtos da Adobe?

Não, mas elas melhoram o desempenho:

| Opção de integração | Recursos |
|-------------------|--------------|
| **Independente** | Funciona com seu catálogo de produtos e conteúdo |
| **Com Adobe Experience Platform** | Perfis de clientes unificados<br>Personalização avançada<br>Consistência entre canais |
| **Com Adobe Commerce** | Estoque em tempo real<br>Histórico de pedidos<br>Integração com o carrinho |
| **Com Adobe Experience Manager** | Gerenciamento de conteúdo<br>Atualizações dinâmicas<br>Suporte a vários sites |

### E se meu site não estiver no Adobe?

O Brand Concierge funciona com qualquer plataforma. O JavaScript SDK é integrado a qualquer site, e os SDKs móveis funcionam com qualquer back-end de aplicativo.

### Como funciona a transferência do agente?

Quando a entrega do agente é acionada, a Brand Concierge transfere o histórico completo da conversa, o perfil e a ID do cliente, a intenção identificada, os detalhes dos produtos discutidos e todas as tentativas de resolução para o agente. Isso garante que os agentes tenham um contexto completo e possam continuar a conversa perfeitamente, sem exigir que os clientes repitam as informações.

### Posso oferecer suporte a vários idiomas?

Sim. Configure o suporte de idioma por assistente com base na sua base de clientes. O Brand Concierge detecta o idioma do cliente e responde de acordo.
