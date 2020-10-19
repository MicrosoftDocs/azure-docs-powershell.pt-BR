---
title: Migrar os scripts do Azure PowerShell do AzureRM para o Az
description: Saiba mais sobre as etapas e as ferramentas para a migração de scripts do módulo AzureRM para o novo módulo Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021084"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrar o Azure PowerShell do AzureRM para o Az

Todas as versões do módulo AzureRM PowerShell estão desatualizadas, mas o suporte continua. Agora, o [módulo Az PowerShell](install-az-ps.md) é o módulo do PowerShell recomendado para interagir com o Azure.

Os scripts gravados para os cmdlets do AzureRM não funcionarão automaticamente com o novo módulo. Para facilitar a transição, foi desenvolvido o [kit de ferramentas de migração do AzureRM para o Az](https://github.com/Azure/azure-powershell-migration). Nenhuma migração para um novo conjunto de comandos é conveniente, mas este artigo ajudará você a começar a realizar a transição para o módulo Az do PowerShell. Para saber mais sobre o módulo Az do PowerShell, confira [Introdução do novo módulo Az do Azure PowerShell](new-azureps-module-az.md).

Para ver a lista completa de alterações da falha entre o AzureRM e o Az, confira as [alterações completas do AzureRM para o Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verifique se os scripts existentes funcionam com a última versão do AzureRM

Antes de executar qualquer etapa de migração, verifique quais versões do AzureRM estão instaladas em seu sistema.
Esse procedimento permite que você verifique se os scripts já estão em execução na última versão e se você sabe quais versões do AzureRM precisam ser desinstaladas.

Para verificar qual versão do AzureRM você instalou, execute o seguinte exemplo:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

A **última** versão disponível do AzureRM é a **6.13.1**. Se você não tiver essa versão instalada, os scripts existentes poderão precisar de modificação adicional para funcionar com o módulo Az, além do que foi descrito neste artigo e na [lista de alterações da falha](migrate-az-1.0.0.md).

Se os scripts não funcionarem com o AzureRM 6.13.1, atualize-os de acordo com o [guia de migração do AzureRM 5.x para o 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Se você usar uma versão anterior do módulo AzureRM, haverá guias de migração disponíveis para cada versão principal.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Instalar o kit de ferramentas de migração do AzureRM para o Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Migrar automaticamente os scripts do PowerShell

Com o kit de ferramentas de migração do AzureRM para o Az, você poderá gerar um plano para determinar quais alterações serão executadas nos scripts antes de fazer qualquer modificação neles e antes de instalar o módulo Az do PowerShell.

O início rápido [Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) orienta você ao longo do processo inteiro de atualização automática dos scripts do PowerShell do AzureRM para o módulo Az do PowerShell.

## <a name="next-steps"></a>Próximas etapas

[Instalar o Azure PowerShell](install-az-ps.md)
[Desinstalar o AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
