---
title: Implantar uma concierge
description: Saiba como implantar uma Brand Concierge configurando uma sequência de dados, instalando o script de implantação, definindo regras de superfície e verificando a implantação.
hide: true
source-git-commit: da4b30fa292b911987aebec378af420b293ea594
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---


# Implantar uma concierge

A implantação disponibiliza um concierge para visitantes reais do site. O profissional de marketing define as configurações de implantação, enquanto a equipe de TI ou de análise fornece a ID da sequência de dados e a equipe do site instala o script de implantação no site.

A implantação geralmente é uma configuração curta e única para cada site. Planeje aproximadamente 15 minutos por parte do profissional de marketing, além do tempo necessário para a equipe de instalação do script no site.

>[!IMPORTANT]
>
>Envolva a equipe de TI ou de análise e a equipe do site antecipadamente. A participação é necessária para fornecer a ID da sequência de dados e instalar o script, de modo que a implantação não deve ser tratada como a etapa final da implementação.

## Antes de começar

- Coordene com a equipe de TI ou de análise para obter uma ID de fluxo de dados.
- Identifique a equipe responsável pelo site ou gerenciador de tags. Este artigo se refere a esse grupo como a equipe do site.
- Decida se o concierge deve aparecer como um componente nas páginas existentes ou como uma página completa e dedicada.
- Identifique os domínios e caminhos de página em que o concierge deve aparecer.

## Configurar o fluxo de dados

Uma sequência de dados é o destino dos dados de atividade gerados pelas interações do visitante com o concierge. Exemplos dessas interações incluem cliques, envios de formulários, reuniões reservadas e bate-papos ao vivo. A sequência de dados permite que essa atividade seja visualizada no Analytics posteriormente.

Não é necessário criar um fluxo de dados como parte desse procedimento. Você só precisa da ID dela.

### Obter a ID do fluxo de dados

Solicite a ID da sequência de dados à equipe de TI ou de análise. A ID pode ser encontrada no Adobe Experience Platform em **Coleção de dados** > **Fluxos de dados**.

### Adicionar a configuração da sequência de dados

1. Tenha a ID da sequência de dados pronta.
1. Na seção de implantação do Brand Concierge, selecione **Adicionar configuração**.
1. Cole a ID do fluxo de dados.
1. Salve a configuração.
1. Depois que a configuração for salva, selecione a opção de instalação apropriada:
   - **Instalação de componente:** use um trecho que a equipe do site coloca em um local específico do site.
   - **Instalação de página inteira:** use uma página completa e pronta para hospedar para uma página de aterrissagem de concierge dedicada.
1. Forneça o script ou a página selecionada à equipe do site.
1. Faça com que a equipe do site instale o script diretamente no código da página ou por meio de um gerenciador de tags.

>[!NOTE]
>
>Normalmente, a instalação é feita pela equipe do site, de modo semelhante à adição de uma tag de análise ou de ferramenta de bate-papo.

## Configurar a superfície

Depois que o script é instalado, a configuração de superfície controla as páginas em que a concierge aparece. Por exemplo, você pode configurar o concierge para aparecer nas páginas de produtos, mas não em uma página de carreiras.

### Adicionar um domínio e regras de página

1. Adicione um domínio, como `blog.example.com`.
1. Escolha como os caminhos no domínio devem corresponder. Os padrões de correspondência disponíveis incluem:
   - Qualquer página sob o domínio.
   - Caminhos que começam com um valor especificado.
   - Caminhos que terminam com um valor especificado.
   - Um caminho exato corresponde.
1. Combine várias regras para definir uma cobertura de página mais precisa.
1. Salve a configuração da superfície.

## Verificar a implantação

Depois que a equipe do site instalar o script e salvar as regras de superfície, verifique se:

- O script está presente nas páginas do site pretendido.
- O concierge aparece somente nas páginas cobertas pelas regras configuradas.
- O concierge não aparece nas páginas excluídas.
- As interações do visitante geram dados de atividade para o fluxo de dados configurado.

>[!TIP]
>
>Teste uma página incluída e uma página excluída. Isso confirma que as regras de superfície estão funcionando como pretendido antes que o concierge seja disponibilizado amplamente.
