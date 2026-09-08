---
description: Notas de versão atuais do Adobe Brand Concierge.
title: Notas de versão atuais
feature: Release Information
source-git-commit: 35ce8a7b460e97336246293ad5e53ee83ead5108
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Informações da versão atual {#current-release-notes}

O Adobe Brand Concierge segue um modelo de entrega contínua, permitindo que o Adobe forneça novos recursos, melhorias e correções de forma contínua.

Todos os recursos estão disponíveis para o público em geral, a menos que indicado de outra forma.

## Agosto de 2026 {#august-2026}

* **Composer 2.0**: a criação de concierge foi reprojetada em torno de uma única URL de site. O Composer elabora automaticamente um ponto de partida alinhado à marca, incluindo expressão da marca, perfil da marca, instruções, medidas de proteção, uma fonte de conhecimento e uma habilidade de linha de base, pronto para revisar e entrar em funcionamento em minutos sem a necessidade de configuração manual para começar.

* **Estrutura de Habilidades e Integrações**: os concierges são criados a partir de um catálogo de autoatendimento de habilidades e integrações, detectáveis e configuráveis por meio da opção Procurar Habilidades e Procurar Integrações. Isso inclui recursos novos e lançados anteriormente, como o Site Advisory, o Product Advisory e o Commerce Catalog Discovery and Comparation.

* **Personalização de Estilo Visual e Componente de Chat**: personalize as cores, as fontes, a mensagem de boas-vindas e os componentes individuais do chat de uma sala de espera, incluindo bolhas de chat, sugestões de prompt, citações, controles de feedback e cartões de produto de uma sala de espera, com as alterações visualizadas ao vivo.

* **Vários concierges por sandbox**: crie e gerencie vários concierges em uma única sandbox, cada um com configuração independente.

* **Eventos do lado do cliente e funções de retorno de chamada**: registre um único retorno de chamada para observar eventos do ciclo de vida do cliente Web, interações do usuário, respostas, comentários e erros em tempo real, para usar no envio de dados de envolvimento para a Adobe Analytics, a Google Analytics ou outros sistemas de terceiros.

* **Suporte para Atendimento Multilíngue (Disponibilidade Limitada)**: implante um concierge em idiomas adicionais, além do inglês, com suporte validado para espanhol e francês. Cada idioma de destino é executado como seu próprio concierge na mesma sandbox e é roteado automaticamente por idioma de solicitação.

* **Implantação: Datastream e Configuração de Superfície**: configure uma sequência de dados para rastrear a participação do visitante e defina regras de superfície para controlar em quais páginas e domínios o concierge aparece, usando a correspondência de domínio e caminho (qualquer, começa com, termina com ou corresponde exata).

## Junho de 2026 {#june-2026}

* **Integração do Marketo**: as conversas com visitantes, incluindo a captura de leads no chat, fluem automaticamente para o Marketo Engage como dados de atividade nativos, disponíveis para uso em campanhas inteligentes de acionador e em lote.

## Abril de 2026 {#april-2026}

* **Integração do Brand Concierge com o Real-Time CDP (Disponibilidade Limitada)**: melhore a qualidade e a relevância das respostas de conversação incorporando o contexto do Real-Time CDP, como atributos de usuário, sinais comportamentais e interações anteriores, para alinhar melhor as respostas com a intenção do usuário.

* **Aprimoramento do Ajuste de Autoatendimento**: o Brand Concierge Composer avalia automaticamente o desempenho da conversa e atualiza as configurações de prompt para melhorar a qualidade da resposta. Essas otimizações são aplicadas continuamente com base em resultados de avaliação automatizada, reduzindo a necessidade de ajuste manual.

* **Recomendação de produto sensível ao contexto**: a Brand Concierge fornece recomendações de produto com base na intenção de usuário inferida, aproveitando dados estruturados do catálogo de produtos e a capacidade de integrar-se à pesquisa de produtos e aos sistemas de registro de recomendação para melhorar a relevância e a precisão. Os cartões de produto são apresentados quando apropriado, oferecendo suporte a recomendações de vários produtos e alinhando-se à intenção de detecção ou compra.

* **Comparação lado a lado**: habilite a comparação lado a lado de vários produtos na conversa por meio de uma exibição de tabela estruturada, destacando os principais atributos, recursos e diferenças. A comparação é gerada dinamicamente com base na intenção do usuário e em produtos selecionados, apoiando uma avaliação e tomada de decisão mais informadas.

* **Agente de Suporte (Solução de Problemas e Instruções)**: habilite o suporte guiado na conversa, ajudando os usuários a solucionar problemas e concluir tarefas de instrução, por meio da assistência sensível ao contexto. O agente adapta as respostas com base na entrada do usuário para impulsionar uma resolução eficiente do problema sem a necessidade de escalonamento.

## Março de 2026 {#march-2026}

* **Configuração do Site Advisor AEM no Composer**: a configuração do Site Advisor AEM no Composer permite que os clientes da AEM configurem facilmente a assimilação da fonte de conhecimento diretamente no Composer, com o conteúdo do site da AEM como a fonte de conhecimento principal. Isso reduz o atrito de integração, garantindo respostas precisas, compatíveis e previsíveis com base no conteúdo AEM do próprio cliente.

* **Assimilação completa de site**: a Assimilação completa de site permite que os clientes assimilem automaticamente todo o site usando um único mapa de site, eliminando a necessidade de carregamentos manuais de URL. Isso garante uma cobertura de conteúdo completa e atualizada com integração escalável e de baixo esforço e atualização contínua do conteúdo.

* **Criação automatizada de prompts (disponibilidade limitada)**: a Criação automatizada de prompts permite que os clientes criem uma experiência de Brand Concierge de alta qualidade por meio de um fluxo simples de autoatendimento. O Brand Concierge gera automaticamente solicitações de concierge a partir de entradas mínimas do usuário sem expor ou exigir engenharia de solicitação. Os usuários não técnicos podem obter rapidamente um serviço de concierge que funcione e tenha a qualidade validada por meio da validação guiada do perfil da marca e da configuração orientada por IA.

* **BYOA - Agente do Firefly em Adobe.com Brand Concierge**: a geração de imagens do Firefly agora está integrada ao Adobe.com Brand Concierge, permitindo que os usuários criem, baixem e continuem editando imagens ou moodboards no Firefly. Este é o nosso primeiro lançamento da integração &quot;Traga seu próprio agente&quot;, permitindo que agentes do cliente e de terceiros façam parte da Brand Concierge por meio da Agent Orchestrator.

## Fevereiro de 2026 {#february-2026}

* **Geração automatizada do conjunto de dados de avaliação**: gere automaticamente conjuntos de dados de avaliação de alta qualidade para avaliações funcionais, fora do escopo e de proteção. O conjunto de dados de avaliação é fundamentado diretamente na base de conhecimento da marca, garantindo testes confiáveis e de alta confiança.

* **Avaliação Automatizada e Loop de Qualidade Baseado em LLM**: valide o desempenho do Concierge com um clique usando a pontuação baseada em LLM nas dimensões de qualidade, incluindo correção, assistência e adesão à marca. Isso fornece avaliações de qualidade objetivas e reproduzíveis que dão aos clientes confiança antes de cada lançamento.

* **Automação para tarefas de criação e inicialização do Concierge (Interface do desenvolvedor)**: é um recurso interno voltado para o desenvolvedor que permite que as equipes girem e iniciem uma experiência do Concierge rapidamente, com opções para gerenciar a sandbox e a configuração do Concierge, a configuração de estilo/interface do usuário e o ajuste de prompt. Isso acelera o tempo de ativação e capacita as equipes a criar instâncias personalizadas e de alta qualidade do Concierge em escala.

* **Aprimoramento do Knowledge Source: Carregamento/Atualização Incremental de URL e Suporte a Tipo de Arquivo Adicional**: o recurso de gerenciamento incremental de URL permite que os clientes atualizem facilmente (adicionar/excluir/atualizar) somente as páginas que foram alteradas, sem reprocessar toda a fonte de conhecimento. Isso reduz o tempo de atualização e diminui a sobrecarga operacional. Além disso, o Brand Concierge agora é compatível com o upload de arquivos PDF/DOCX.

* **Suporte a esquema de produto personalizado**: o recurso de suporte a esquema personalizado permite que os clientes carreguem e gerenciem catálogos de produtos que seguem sua própria estrutura de dados em vez de um formato fixo. Isso permite a validação adequada, o mapeamento de campos e a geração precisa de cartões de produtos entre marcas com diferentes modelos de catálogos.

* **SDK móvel**: o Brand Concierge Mobile SDK (para aplicativos móveis) permite que as marcas incorporem o Brand Concierge diretamente em seus aplicativos móveis, suportando interações de texto, voz e imagem. Ele fornece interface pronta para uso e integração de back-end para que os consumidores possam acessar facilmente o Brand Concierge no aplicativo da marca.
