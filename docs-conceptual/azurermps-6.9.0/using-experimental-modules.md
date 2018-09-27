---
title: Usando módulos experimentais do Azure PowerShell
description: Entenda a filosofia e o uso dos módulos experimentais do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: cb1c49682ea1bfd5fa43baafe4cb0f7fc0c46020
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178928"
---
# <a name="use-experimental-azure-powershell-modules"></a>Usar módulos experimentais do Azure PowerShell

Com ênfase nas ferramentas do desenvolvedor (especialmente as CLIs) no Azure, a equipe do Azure PowerShell está experimentando várias melhorias na experiência do Azure PowerShell.

## <a name="experimentation-methodology"></a>Metodologia de experimentação

Para facilitar a experimentação, estamos criando novos módulos do Azure PowerShell que implementam a funcionalidade existente do SDK do Azure de formas novas e mais fáceis de usar. Na maioria dos casos, os cmdlets espelham exatamente os cmdlets existentes. No entanto, os cmdlets experimentais fornecem uma notação abreviada e valores padrão mais inteligentes que facilitam criar e gerenciar os recursos do Azure.

Esses módulos podem ser instalados lado a lado com os módulos existentes do Azure PowerShell. Os nomes do cmdlet foram reduzidos para fornecer nomes mais curtos e evitar conflitos de nomenclatura com os cmdlets existentes e não experimentais.

Os módulos experimentais usam a seguinte convenção de nomenclatura: `AzureRM.*.Experiments`. Essa convenção de nomenclatura é semelhante à nomenclatura dos módulos de Visualização: `AzureRM.*.Preview`. Os módulos de Visualização são diferentes dos módulos experimentais. Os módulos de Visualização implementam a nova funcionalidade de serviços do Azure, só disponível como uma oferta de Visualização. Os módulos de Visualização substituem os módulos existentes do Azure PowerShell e usam os mesmos nomes do cmdlet e do parâmetro.

## <a name="how-to-install-an-experimental-module"></a>Como instalar um módulo experimental

Os módulos experimentais são publicados na Galeria do PowerShell como módulos existentes do Azure PowerShell. Para ver uma lista de módulos experimentais, execute o seguinte comando:

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

Para instalar o módulo experimental, use os seguintes comandos de uma sessão do PowerShell com privilégios elevados:

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Documentação e suporte

A documentação está incluída no pacote de instalação e é acessada usando o cmdlet `Get-Help`. Nenhuma documentação oficial é publicada para os módulos experimentais.

Incentivamos você a testar esses módulos. Seus comentários nos permitam aumentar a utilização e responder às suas necessidades. No entanto, sendo experimentais, o suporte para esses módulos é limitado. As perguntas ou problemas podem ser enviados criando um [caso](https://github.com/Azure/azure-powershell/issues) no repositório do GitHub.

## <a name="experiments-and-areas-of-improvement"></a>Experimentos e áreas de aprimoramento

Esses aperfeiçoamentos foram selecionados com base nos principais diferenciais dos produtos concorrentes. Por exemplo,a CLI do Azure 2.0 fez questão de basear os comandos nos _cenários_, em vez da _área de superfície de API_.
A CLI do Azure 2.0 usa vários padrões inteligentes que facilitam os cenários de "introdução" para os usuários finais.

### <a name="core-improvements"></a>Principais melhorias

As principais melhorias são consideradas de "bom senso" e pouca experimentação é necessária para continuar a implementar essas atualizações.

- Cmdlets baseados em cenário - **Todos*- os cmdlets devem ser criados com base em cenários, não no serviço REST do Azure.

- Menor nomes - isso inclui os nomes dos cmdlets (por exemplo, `New-AzureRmVM` => `New-AzVm`) e os nomes dos parâmetros (por exemplo, `-ResourceGroupName` => `-Rg`). Use aliases para ter compatibilidade com os cmdlets "antigos". Forneça conjuntos de parâmetros _compatíveis com as versões anteriores_.

- Padrões Inteligente - criam padrões inteligentes preencher as informações "obrigatórias". Por exemplo: 
  - Grupo de recursos
  - Local padrão
  - Recursos dependentes

### <a name="experimental-improvements"></a>Melhorias experimentais

As melhorias experimentais apresentam uma alteração significativa que a equipe deseja validar via experimentação.

- Tipos simples - criam cenários que devem ficar longe dos tipos complexos e objetos de configuração. Simplifique a configuração para um ou dois parâmetros.

- "Criação Inteligente" - todos que criam cenários que implementam a "Criação Inteligente" _não_ teriam parâmetros obrigatórios: todas as informações necessárias seriam escolhidas pelo Azure PowerShell de forma dogmática.

- Parâmetros cinzas - em muitos casos, alguns parâmetros podem ser "cinza" ou semiopcionais. Se o parâmetro não for especificado, será perguntado ao usuário se este deseja o parâmetro gerado para ele. Também faz sentido que os parâmetros cinzas deduzam um valor com base no contexto, com a autorização do usuário.
  Por exemplo, talvez faça sentido que o parâmetro cinza sugira o valor usado mais recentemente.

- `-Auto`Argumento - o argumento `-Auto` forneceria uma maneira de "aceitação" para que os usuários _tenham como padrão tudo_, mantendo a integridade dos parâmetros necessários no caminho principal.

### <a name="feature-specific-switches"></a>Argumentos específicos do recurso

Por exemplo, o cenário de "Criar aplicativo Web" pode ter um argumento `-Git` ou `-AddRemote` que adicionaria automaticamente um "azure" remoto a um repositório git existente.

- Padrões configuráveis - Os usuários devem ser capazes de definir padrões para parâmetros comuns como `-ResourceGroupName` e `-Location`.

- Padrões de tamanho - o recurso "tamanhos" pode confundir os usuários, pois muitos Provedores de Recursos usam nomes diferentes (por exemplo, "Standard\_DS1\_v2" ou "S1"). No entanto, a maioria dos usuários se importa mais com o custo. Portanto, faz sentido definir tamanhos “universais” com base em um agendamento de preços. Os usuários podem escolher um tamanho específico ou deixar que o Azure PowerShell escolher a _melhor opção_ com base no recurso do orçamento.

- Formato da saída - o Azure PowerShell atualmente retorna `PSObject`s e há pouca saída do console. O Azure PowerShell pode precisar exibir algumas informações para o usuário sobre os “padrões inteligentes” usados.
