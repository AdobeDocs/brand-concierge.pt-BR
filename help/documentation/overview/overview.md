---
title: Visão geral do Brand Concierge
description: Saiba o que é o Brand Concierge, como seus principais componentes se encaixam e o glossário de termos principais que você encontrará na interface do Composer.
source-git-commit: 60835c7971d86341194d773f9cf487c4cb6f171a
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 1%

---

# Visão geral do Brand Concierge

O Brand Concierge é uma plataforma eficiente que permite que empresas e marcas iniciem experiências de conversação personalizadas em suas superfícies voltadas para o cliente: sites, aplicativos móveis e outras propriedades digitais. Cada conversa está fundamentada no conteúdo e nas medidas de proteção da própria marca, e as integrações permitem que os insights dessas conversas fluam para o restante do ecossistema da marca, como o Marketo Engage.

## Componentes principais

Uma implantação do Brand Concierge tem duas partes principais:

| Peça | O que é |
|---|---|
| **Experiência do visitante** | A superfície voltada para a marca, como um site ou aplicativo móvel, em que os visitantes se envolvem com o porteiro e obtêm respostas em tempo real. |
| **Compositor** | A interface do profissional usada para projetar experiências de concierge e gerenciar concierges, integrações, configurações, avaliações, implantação e análises. |

## Módulos do compositor

No Composer, os principais módulos são:

- [Gerenciamento de usuários e de acesso](../user-and-access-management/add-a-user-to-the-org.md)
- [Criação e gerenciamento da fonte de conhecimento](../knowledge-sources/knowledge-sources.md), compartilhados entre concierges
- [Gerenciamento de concierge](../concierge-management/concierge-management.md): integrações, habilidades, instruções de concierge, tom e voz, estilo visual e componentes de chat
- [Avaliação](../evaluation/evaluation.md)
- [Implantação](../deployment/deployment.md)
- [Lista de verificação de ativação](../go-live-checklist/go-live-checklist.md)
- [Analytics](../analytics/analytics.md)

## Como as partes se conectam

Uma fonte de conhecimento (conteúdo) é consultada por uma integração (conexão), chamada por uma habilidade (comportamento), tudo envolvido em uma concierge (a experiência geral) com a qual os visitantes interagem.

## Glossário

Esses termos aparecem na interface do Composer.

| Termo | Definição |
|---|---|
| **Atendimento** | A própria experiência de bate-papo com IA: uma por marca, site ou caso de uso. Uma conta pode ter vários. |
| **Compositor** | A interface usada para criar e gerenciar concierges, diferente do que os visitantes do site veem. |
| **Fonte de conhecimento** | O conteúdo que um concierge pode usar ao responder perguntas, como páginas de site ou uma lista de produtos. Sem ele, o porteiro não tem nada para responder. |
| **Integração** | Uma conexão com um sistema que pode recuperar informações, como conteúdo de site ou um catálogo de produtos ativo. |
| **Habilidade** | Um recurso específico que o porteiro pode executar, como responder a perguntas gerais, comparar produtos ou marcar uma reunião. Uma habilidade usa uma ou mais integrações para executar sua função. |
| **Medidas de proteção** | Regras que definem o que o porteiro não deve fazer ou discutir, como concorrentes ou aconselhamento jurídico. |
| **Avaliação** | Um teste estruturado que consiste em perguntas de amostra emparelhadas com as respostas esperadas, usado para avaliar o desempenho da concierge. |
| **ID da sequência de dados** | Um identificador técnico que especifica para onde os dados de atividade do visitante são enviados em sistemas Adobe. Ele é fornecido pela equipe de TI ou de análise. |
| **Sandbox** | Um espaço de trabalho isolado em uma organização. Uma organização pode ter mais de um; cada um pode conter vários concierges. |
| **Organização IMS** | Termo da Adobe para a conta geral de uma organização. |
| **MCP** (por exemplo, Commerce MCP) | Um conector gerenciado pela Adobe para um sistema específico, como um catálogo de produtos ao vivo, configurado usando códigos ou chaves fornecidos pela TI ou pela equipe de comércio. |
| **CJA (Customer Journey Analytics)** | produto de análise da Adobe. O Brand Concierge provisiona automaticamente um painel inicial aqui sem nenhuma configuração adicional necessária. |

>[!NOTE]
>
>Normalmente, os profissionais de marketing podem ignorar completamente o [Gerenciamento de usuários e acessos](../user-and-access-management/add-a-user-to-the-org.md) (alguém na TI o conclui uma vez) e começar em [Fontes de conhecimento](../knowledge-sources/knowledge-sources.md). Retorne ao gerenciamento de usuários e acesso somente ao configurar novos colegas de equipe.
