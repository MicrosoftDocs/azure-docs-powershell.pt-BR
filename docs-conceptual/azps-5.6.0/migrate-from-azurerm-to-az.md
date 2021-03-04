---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Conheça as etapas e as ferramentas para migrar os scripts do Azure PowerShell do AzureRM para o novo módulo Az PowerShell.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872230"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrar o Azure PowerShell do AzureRM para o Az

Todas as versões do módulo AzureRM PowerShell estão desatualizadas. Agora, o [módulo Az PowerShell](install-az-ps.md) é o módulo do PowerShell recomendado para interagir com o Azure.

## <a name="why-a-new-module"></a>Por que um novo módulo?

A maior e mais importante alteração é que o [PowerShell](/powershell/scripting/overview), baseado na biblioteca .NET Standard, tem sido um produto multiplataforma desde que foi introduzido.

Como a linguagem do PowerShell, estamos comprometidos em oferecer o suporte do Azure em todas as plataformas. Nosso compromisso significava que os módulos do Azure PowerShell precisavam ser atualizados para usar o .NET Standard e ser compatíveis com o PowerShell Core. Em vez de modificar o módulo AzureRM existente e introduzir alterações complexas para adicionar esse suporte, o módulo Az foi criado.

A criação de um módulo também permitiu que nossos engenheiros tornassem consistentes o design e a nomeação de cmdlets e módulos. Todos os módulos agora começam com o prefixo `Az.` e todos os cmdlets usam a convenção de nomenclatura `Verb-AzNoun`. Anteriormente, os nomes dos cmdlets eram mais longos e inconsistentes.

O número de módulos também foi reduzido: Alguns módulos que funcionavam com os mesmos serviços foram combinados. Os cmdlets do plano de gerenciamento e do plano de dados agora estão contidos em módulo único. Para aqueles que gerenciam dependências e importações manualmente, essa consolidação simplifica muito as coisas.

Ao fazer essas alterações importantes, a equipe se comprometeu em tornar o uso do Azure com cmdlets do PowerShell mais fácil do que nunca e em mais plataformas do que era possível anteriormente.

## <a name="upgrading-to-az-powershell"></a>Atualizando para o Az PowerShell

Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente no Az. Para facilitar a transição, foi desenvolvido o [kit de ferramentas de migração do AzureRM para o Az](https://github.com/Azure/azure-powershell-migration). Nenhuma migração para um novo conjunto de comandos é conveniente, mas este artigo ajudará você a começar a realizar a transição para o módulo Az do PowerShell. Para saber mais sobre o módulo Az do PowerShell, confira [Introdução do novo módulo Az do Azure PowerShell](new-azureps-module-az.md).

Os novos nomes de cmdlets foram projetados para serem fáceis de aprender. Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`. Por exemplo, o cmdlet antigo `New-AzureRMVm` tornou-se `New-AzVm`.
Contudo, a migração é mais do que apenas se familiarizar com os novos nomes de cmdlets. Há módulos e parâmetros renomeados, além de outras alterações importantes.

Para ver a lista completa de alterações da falha entre o AzureRM e o Az, confira as [alterações completas do AzureRM para o Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verifique se os scripts existentes funcionam com a última versão do AzureRM

Antes de executar qualquer etapa de migração, verifique quais versões do AzureRM estão instaladas em seu sistema.
Esse procedimento permite que você verifique se os scripts já estão em execução na última versão e se você sabe quais versões do AzureRM precisam ser desinstaladas.

Para verificar qual versão do AzureRM você instalou, execute o seguinte exemplo:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

A **última** versão disponível do AzureRM é a **6.13.1**. Se você não tiver essa versão instalada, os scripts existentes poderão precisar de modificação adicional para funcionar com o módulo Az, além do escopo descrito neste artigo e na [lista de alterações da falha](migrate-az-1.0.0.md).

Se os scripts não funcionarem com o AzureRM 6.13.1, atualize-os de acordo com o [guia de migração do AzureRM 5.x para o 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Se você usar uma versão anterior do módulo AzureRM, haverá guias de migração disponíveis para cada versão principal.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Opção 1 (recomendada): Migrar automaticamente os scripts do PowerShell

Essa opção recomendada minimiza o esforço necessário para migrar scripts do AzureRM para o Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Instalar o kit de ferramentas de migração do AzureRM para o Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Converter scripts automaticamente

Com o kit de ferramentas de migração do AzureRM para o Az, você poderá gerar um plano para determinar quais alterações serão executadas nos scripts antes de fazer qualquer modificação neles e antes de instalar o módulo Az do PowerShell.

O início rápido [Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) orienta você ao longo do processo inteiro de atualização automática dos scripts do PowerShell do AzureRM para o módulo Az do PowerShell.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Opção 2: Usar o modo de compatibilidade com o cmdlet Enable-AzureRmAlias

O módulo Az tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você atualiza para a nova sintaxe. O cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) habilita um modo de compatibilidade por meio de aliases. Esse modo permite que você use scripts existentes com o mínimo de modificações, ao passo que trabalha no sentido de uma migração completa para o Az. Por padrão, `Enable-AzureRmAlias` habilita apenas aliases de compatibilidade para a sessão atual do PowerShell. Use seu parâmetro `Scope` para persistir os aliases de compatibilidade entre as sessões do PowerShell. Para obter mais informações, confira a [documentação de referência de Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Embora os nomes dos cmdlets sejam convertidos em alias, ainda poderá haver parâmetros novos (ou renomeados) ou valores retornados alterados para os cmdlets do Az. Não espere que a habilitação de aliases cuide da migração para você. Confira a [lista completa de alterações da falha](migrate-az-1.0.0.md) para descobrir quando seus scripts podem exigir atualizações.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Opção 3: Migrar os scripts do Visual Studio Code com a extensão do Azure PowerShell

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Instalar a extensão do Azure PowerShell para Visual Studio Code

Instalar a [extensão do Azure PowerShell para VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>Converter scripts manualmente

1. Carregar o script do AzureRM no VSCode
2. Iniciar a migração abrindo a paleta de comandos `Ctrl+Shift+P` e selecionar `Migrate Azure PowerShell script`
3. Selecionar versão de origem `AzureRM`
4. Siga as ações recomendadas para cada comando ou parâmetro sublinhado.

## <a name="next-steps"></a>Próximas etapas

* [Desinstalar o AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [Instale o Azure PowerShell](install-az-ps.md)
