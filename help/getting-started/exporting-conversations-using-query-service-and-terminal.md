---
title: Exportar conversas usando o serviço de consulta e o terminal
description: Saiba como exportar conversas do Brand Concierge para CSV usando o Serviço de consulta e o Terminal da Experience Platform, com orientação sobre credenciais e dados pessoais.
topic: Development
role: Developer
level: Experienced
doc-type: Tutorial
duration: 260
last-substantial-update: 2026-10-15
jira: KT-22874
source-git-commit: 04c844e16a8fb13e54dfcbb29c776896674532b9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%
---
# Exportar conversas usando o serviço de consulta e o terminal

Saiba como salvar e exportar conversas do Adobe Brand Concierge usando o Serviço de consulta e o Terminal da Adobe Experience Platform. Este vídeo mostra como localizar nomes de tabela de conjunto de dados, configurar o cliente de linha de comando PostgreSQL e exportar dados de conversação de um intervalo de datas para um arquivo CSV.

## Para quem é este vídeo?

* Desenvolvedores que precisam exportar dados de conversação do Brand Concierge usando ferramentas de linha de comando

## Conteúdo de vídeo

* Localizar conjuntos de dados de conversa no Experience Platform e copiar seus nomes de tabela
* Instale o cliente PostgreSQL com o Homebrew e configure seu caminho de linha de comando
* Copie o comando de conexão PSQL da guia Credenciais do Serviço de Consulta
* Selecione um conjunto de dados e um intervalo de datas e exporte os resultados da consulta para um arquivo CSV local
* Verifique os resultados exportados e atualize as credenciais expiradas quando necessário

>[!VIDEO](https://video.tv.adobe.com/v/3504647?captions=por_br)

```bash
psql "sslmode=require host=... password=..." --csv -o ~/brand-concierge-conversation-export/oct-1-2026-till-today-responses.csv -c "SELECT * FROM cja_brand_concierge_responses_dataset_b4c15126_bd9b_4d52_8151_26 WHERE timestamp >= TIMESTAMP '2026-10-01 00:00:00' AND timestamp <= NOW() ORDER BY timestamp ASC LIMIT 1000"
```

>[!IMPORTANT]
>
> O comando de conexão PSQL contém uma senha ativa. Não o compartilhe nem cole em chats, agentes de IA ou emails. Se a autenticação falhar após a senha expirar, copie um novo comando da guia Credenciais do serviço de consulta.

>[!NOTE]
>
> As conversas exportadas podem conter informações de identificação pessoal (PII). Siga a política de tratamento de dados de sua organização ao armazenar arquivos CSV.

Para obter a documentação, consulte a [ajuda do Brand Concierge](../documentation/overview.md).

## Tutoriais relacionados

* [Exportar conversas usando o Adobe CX Enterprise Coworker](exporting-conversations-using-adobe-cx-enterprise-coworker.md)
