---
title: Gerenciar um concierge
description: Saiba como criar uma Brand Concierge a partir de um site, configurar suas integrações, habilidades, instruções, tom e estilo visual e testá-la antes da implantação.
toc: true
source-git-commit: fc22eb8e724437483e5d87283f46fb629a4e507c
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 0%

---


# Gerenciar um concierge

Um concierge é criado a partir de um site da marca e pode ser refinado com integrações, habilidades, instruções, configurações de tom e voz, estilos visuais e componentes de bate-papo. Use a visualização para testar as alterações antes de implantar deliberadamente o concierge para os visitantes.

## Visão geral

| Item | Detalhes |
|---|---|
| Usuário primário | Profissional de marketing que usa a configuração de autoatendimento |
| Suporte adicional | As integrações Commerce e B2B podem exigir códigos, chaves ou configuração de uma equipe de TI, comércio ou vendas |
| Tempo típico | Cerca de 5 minutos para criar um concierge de linha de base; é necessário um tempo contínuo para refinamento e teste |
| Implantação | Separado da criação; a criação de um concierge não o torna visível para os visitantes do site |

>[!NOTE]
>
>Uma sandbox pode conter vários concierges. Cada concierge tem sua própria configuração e as concierge podem ser excluídas da lista de concierge.

## Criar um concierge

Criar um concierge a partir de um único URL do site é o ponto de partida recomendado para um usuário pela primeira vez. O sistema cria uma linha de base de trabalho sem exigir configuração manual.

1. Insira a URL do site da marca e selecione **Criar**.

1. Revise a expressão de marca gerada. O sistema analisa o tom do site e propõe atributos como formalidade, calor, jovialidade e energia. Ajuste os valores conforme necessário e selecione **Continuar**.

1. Revise o perfil de marca gerado. O perfil pode incluir a meta da marca, os produtos e serviços, o público-alvo, os valores da marca, os principais diferenciais e os casos de uso comuns. Edite o perfil conforme necessário e selecione **Continuar**.

1. Revise as instruções de início, as medidas de proteção e as sugestões geradas. Por exemplo, as medidas de proteção podem excluir tópicos legais, tópicos de conformidade ou discussões de concorrentes, enquanto as sugestões podem fornecer ideias de prompt de acompanhamento. Edite o conteúdo conforme necessário e selecione **Salvar**.

1. Aguarde o sistema aplicar a configuração de linha de base. O sistema também cria um estilo visual padrão usando cores e fontes desenhadas no site e ativa habilidades e integrações de linha de base, como uma habilidade geral de pergunta e resposta conectada ao conteúdo do site.

1. Testar o concierge na visualização. As visualizações para desktop e dispositivos móveis estão disponíveis. Selecione **Novo** para reiniciar uma conversa de teste.

>[!IMPORTANT]
>
>Criar um concierge não o torna visível para os visitantes. A implantação é uma etapa separada e deliberada. Você pode revisar a configuração a qualquer momento antes da implantação.

## Entender o que é configurado automaticamente

Os seguintes itens são configurados automaticamente quando você cria um concierge:

| Item | Configuração |
|---|---|
| Conteúdo da knowledge base | Criado a partir das páginas principais do site por meio de um rastreo em segundo plano que é iniciado automaticamente |
| Integração da Pesquisa na knowledge base | Aponta automaticamente para o conteúdo rastreado |
| Habilidade do Site Advisory | Ativo por padrão, para que o porteiro possa responder a perguntas gerais imediatamente |

## Entender habilidades e integrações

O Composer, a interface usada para criar e configurar uma concierge, usa dois conceitos relacionados:

- **Integração:** uma conexão com uma fonte de dados, como conteúdo de site ou um catálogo de produtos em tempo real. Uma integração recupera informações, mas não toma decisões por si só.
- **Habilidade:** um comportamento que determina o que o porteiro faz, quando o faz e quais integrações ele pode usar.

Uma integração pode atender a várias habilidades, e uma habilidade pode usar várias integrações. Por exemplo, uma única conexão de catálogo de produtos pode dar suporte a vários casos de uso relacionados a produtos sem ser recriada para cada habilidade.

## Configurar integrações

Selecione **Procurar Integrações** para exibir o catálogo de integração disponível.

| Integração | Finalidade | Notas |
|---|---|---|
| Pesquisa na knowledge base | Pesquisa o conteúdo do site | Configurado automaticamente quando o concierge é criado |
| Pesquisa com IA de conteúdo | Pesquisa conteúdo do AEM Sites | Relevante para clientes do AEM Sites as a Cloud Service |
| Catálogo de produtos | Exibe cartões de produto ou links de uma lista de produtos carregada | Destinado a catálogos menores que não sejam de comércio |
| COMMERCE MCP | Conecta-se a um catálogo Adobe Commerce em tempo real para pesquisa de produtos, detalhes de produtos e comparações | Não habilitado por padrão; requer códigos ou chaves do comércio ou da equipe de TI |
| Reserva de Reunião | Permite aos visitantes reservar uma reunião com um representante de vendas | Recurso B2B |
| Bate-papo ao vivo | Conecta visitantes com um representante de vendas ao vivo | Recurso B2B |

### Ativar e configurar uma integração

1. Abra o bloco de integração e selecione **Editar**.

1. Para a **Pesquisa na Base de Dados de Conhecimento**, selecione a fonte de conhecimento a ser pesquisada. Você pode renomear a conexão, por exemplo `Website content`.

1. Para o **Commerce MCP**, insira os seguintes valores fornecidos pelo Adobe Commerce ou pela equipe de TI e conecte:
   - ID do ambiente
   - Código do site
   - Armazenar código
   - Código de exibição da loja
   - Chave de API

1. Selecione **Salvar**. A integração é mostrada como conectada e pode ser visualizada, editada ou removida.

É possível adicionar mais de uma instância da mesma integração, como instâncias que apontam para diferentes fontes de conhecimento. Uma habilidade pode ser configurada para usar uma instância de integração específica.

### Informações de integração que exigem confirmação

Os seguintes detalhes não foram estabelecidos no material de origem e devem ser confirmados antes da publicação como documentação do produto:

- A URL de produção completa para entrar no `experienceplatform.adobe.com`.
- Se um concierge tem um limite no número de instâncias de integração.
- O roteiro e o processo para integrações personalizadas ou próprias, que foram mencionados como planejados, mas não detalhados.

## Configurar habilidades

As habilidades determinam o que um porteiro pode fazer pelos visitantes. Selecione **Procurar Habilidades** para exibir o catálogo de habilidades disponível.

| Habilidade | Finalidade | Integração ou configuração necessária |
|---|---|---|
| Aviso do site | Responde perguntas gerais sobre a marca, incluindo perguntas frequentes, políticas, preços, instruções e tópicos de suporte | Conteúdo do site; ativo por padrão |
| Descoberta do catálogo Adobe Commerce | Pesquisa, pesquisa, filtra e recupera detalhes sobre produtos de um catálogo em tempo real | Integração do Commerce MCP |
| Comparação de produtos do Adobe Commerce | Fornece uma comparação lado a lado de produtos nomeados | Integração do Commerce MCP |
| Reservar Reunião com Vendas | Sugere e facilita a marcação de uma reunião | Integração de reserva de reunião |
| Bate-papo ao vivo com o setor de vendas | Sugere e facilita uma entrega de bate-papo ao vivo | Integração com o bate-papo ao vivo |

### Ativar e configurar uma habilidade

1. Abra o bloco de habilidades e selecione **Modificar**.

1. Defina o nome, a descrição e as intenções da habilidade. Intenções são as frases ou os tópicos que devem disparar a habilidade, como `pricing` ou `compare products`. É possível adicionar várias intenções.

1. Se a habilidade exigir uma integração, anexe a integração necessária. Por exemplo, uma habilidade comercial exige Commerce MCP. Como alternativa, selecione **Usar recomendado** para permitir que o Composer selecione automaticamente uma integração apropriada.

1. Revise e edite as instruções iniciais da habilidade, conforme necessário.

1. Selecione **Salvar** e teste a alteração na visualização ao vivo.

>[!TIP]
>
>Se duas habilidades puderem responder à mesma pergunta, o roteamento poderá se tornar inconsistente. Mantenha acionadores de habilidades distintos e específicos em vez de usar intenções sobrepostas.

### Informações de habilidades personalizadas que exigem confirmação

O material de origem menciona um recurso planejado para criar habilidades totalmente personalizadas, mas não fornece um roteiro ou processo. Confirme as etapas de disponibilidade e criação antes de documentar esse recurso como compatível.

## Adicionar instruções de concierge

Use o campo de instruções do concierge para manter as respostas alinhadas às diretrizes da marca. As instruções podem definir:

- Uso da marca comercial
- Estrutura de resposta
- Tópicos a serem evitados

Digite as instruções diretamente no campo de texto. Quando você salva as instruções, o concierge atualiza automaticamente seu comportamento. Teste o resultado imediatamente na pré-visualização ao vivo.

A mesma área também inclui o seguinte conteúdo editável:

- **Medidas de proteção:** comportamentos ou tópicos que o concierge deve evitar.
- **Sugestões:** Acompanhe as ideias do prompt que podem ser mostradas após uma resposta.

## Configurar tom e voz

As configurações de tom e voz controlam o comprimento da resposta e os atributos de tom, incluindo:

- Formal ou casual
- Quente ou neutro
- Brincalhão ou sério

As seleções são salvas automaticamente. Teste o resultado na pré-visualização ao vivo depois de fazer as alterações.

## Configurar o estilo visual

As configurações de estilo visual controlam a aparência do concierge, incluindo, mas não limitado a:

- Cores
- Fontes
- Texto da mensagem de boas-vindas
- Texto do aviso legal
- Cores do cartão

Edite as configurações na interface do usuário e use a pré-visualização ao vivo para revisar as alterações. Selecione **Salvar** para tornar as alterações permanentes.

>[!NOTE]
>
>O material de origem afirma que uma aparência totalmente personalizada pode ser possível além das opções disponíveis na interface do usuário, por meio de um script de implantação separado. O procedimento do script de implantação não foi incluído e deve ser documentado separadamente após ser confirmado.

## Configurar componentes do chat

Os componentes de Chat controlam os elementos individuais que os visitantes veem na janela de chat. Selecione um componente na interface para abrir as configurações em um painel lateral.

| Componente | O que ele controla |
|---|---|
| Bolha de bate-papo | A aparência das mensagens do visitante e das mensagens de concierge |
| Iniciar aviso ou avisar pílulas | Perguntas de abertura sugeridas, especialmente as mostradas em dispositivos móveis |
| Sugestões de acompanhamento | Próximas perguntas sugeridas após uma resposta |
| Barra de entrada | A caixa de mensagem que os visitantes usam para inserir uma pergunta |
| Citações | Se e como as referências de origem aparecem em uma resposta |
| Feedback | O controle de classificação de miniatura ou miniatura mostrado após cada resposta |
| Cartão do produto | O layout e o estilo dos cartões de produto, incluindo cores e botões |

## Configurar recursos B2B

A Reserva de Reunião e o Bate-papo ao Vivo permitem que os visitantes agendem reuniões com os representantes de vendas ou iniciem um bate-papo ao vivo com um representante. Esses recursos são fornecidos por um produto complementar chamado Sales Qualifier.

### Funções e responsabilidades

- **Profissional de marketing:** Configura a habilidade e a integração no Brand Concierge.
- **Representante de vendas:** conecta seu próprio calendário e configura a disponibilidade.

### Configurar a Reserva da Reunião ou o Bate-papo ao Vivo

1. Em **Procurar Integrações**, abra a **Reserva de Reunião** ou o **Chat ao Vivo**. Por padrão, todos na organização estão disponíveis como um possível membro da equipe; nenhuma etapa separada é necessária para adicionar membros da equipe nesse estágio.

1. Faça com que cada representante de vendas entre no `experienceplatform.adobe.com`, abra o **Sales Qualifier** e vá para as **Configurações de Perfil**.

1. Faça com que cada representante conecte um calendário, como o Outlook. Como opção, o Microsoft Teams pode ser incluído. O representante também pode definir o assunto do convite da reunião e o texto do email.

1. Configure a disponibilidade. A disponibilidade é retirada do calendário por padrão e pode ser ainda limitada por:
   - Duração da reunião
   - Tempo de buffer entre reuniões
   - Aviso mínimo obrigatório
   - Janelas de tempo específicas disponíveis

1. Configure a disponibilidade do Live Chat separadamente, usando um processo semelhante.

1. Na Brand Concierge, abra **Membros Gerenciados** e confirme se os representantes são mostrados como disponíveis.

1. Ative a integração do **Reserva de Reunião** e/ou do **Chat ao Vivo**.

1. Vá para **Procurar Habilidades** e selecione **Reservar Reunião com Vendas** e/ou **Bate-papo ao Vivo com Vendas**. Defina os acionadores, anexe a integração correspondente e salve a habilidade.

1. Selecione **Simular** para testar a experiência completa. Insira uma pergunta de exemplo e confirme se ela é direcionada para o fluxo correto de habilidades e engajamento.

### Comportamento após a implantação

Quando os recursos estiverem ativos:

- Os bate-papos ao vivo recebidos aparecem para representantes disponíveis em tempo real.
- As reuniões marcadas aparecem em uma exibição de reuniões.
- Um Relatório de Desempenho de Reunião está disponível no Analytics.
- Envolvimentos de reunião e chat são enviados para a Marketo como atividades, junto com dados de atividade existentes.

### Informações B2B que exigem confirmação

O material de origem identifica os seguintes itens como não resolvidos:

- O Live Chat não tem seu próprio painel de análise; isso foi descrito como uma lacuna de produto em andamento, em vez de uma lacuna de documentação.
- O caminho de entrada `experienceplatform.adobe.com` exato para o Sales Qualifier.
- Se a Reserva de Reunião e o Bate-papo ao Vivo exigem licenças ou direitos separados.

## Compartilhar um link de visualização

Um link de visualização compartilhável permite que as partes interessadas revisem e interajam com uma concierge sem acesso ao Composer e sem implantar a concierge em um site ativo.

1. Na tela de visualização do concierge, gere um link de visualização compartilhável.

1. Compartilhe o link com revisores.

1. Os revisores podem interagir com a concierge por meio do link sem fazer logon no Composer.

### Informações do link de visualização que exigem confirmação

Confirme os detalhes a seguir antes de publicar esse procedimento como um fluxo de trabalho completo do produto:

- O local e rótulo exatos da ação de compartilhamento na interface do usuário.
- Se os links de visualização expiram ou podem ser revogados.
- Se o uso do link de visualização é rastreado separadamente do live analytics.

## Testar antes da implantação

Use a experiência de visualização ou simulação após cada alteração significativa de configuração. No mínimo, verifique o seguinte:

- O concierge responde a perguntas gerais do conteúdo do site desejado.
- Cada habilidade responde somente aos acionadores desejados.
- As integrações necessárias estão conectadas e apontam para a fonte de dados correta.
- As pesquisas e comparações de produtos usam a instância do MCP ou do Catálogo de produtos do Commerce pretendida.
- Reserva de reunião e rota de bate-papo ao vivo para os representantes pretendidos.
- Tom, voz, instruções, medidas de proteção e sugestões produzem as respostas esperadas.
- Estilos visuais e componentes de bate-papo são exibidos corretamente em visualizações móveis e de desktop.
- As partes interessadas podem revisar a experiência por meio do link de visualização compartilhável, se usado.
