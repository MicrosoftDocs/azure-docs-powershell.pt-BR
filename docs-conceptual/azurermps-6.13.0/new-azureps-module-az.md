---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828103"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Apresentação do novo módulo Az do Azure PowerShell

A partir de novembro de 2018, o módulo `Az` do Azure PowerShell estará disponível para visualização pública completa.
O Az oferece comandos menores, maior estabilidade e dá suporte ao Windows, macOS e Linux. O Az também oferece paridade de recursos e um caminho de migração fácil do AzureRM.

O Az usa a biblioteca .NET Standard, ou seja, ele é executado no PowerShell 5.x e no PowerShell 6.x.
Uma vez que o PowerShell 6.x pode ser executado no Linux, macOS e Windows, significa que o Az está disponível para todas as plataformas.
O .NET Standard permite unificar a base de código do Azure PowerShell com impacto mínimo para os usuários.

O Az é um novo módulo, portanto, a versão foi redefinida. A primeira versão estável será a 1.0. No entanto, o módulo terá paridade de recursos com o AzureRm a partir de novembro de 2018.

## <a name="upgrade-to-az"></a>Atualizar para o Az

É recomendável que os usuários atualizem para o novo módulo `Az`. Para fazer isso:

* [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-azurerm-ps)
* [Instalar o módulo Az do Azure PowerShell](/powershell/azure/install-az-ps)
* Habilitar o modo de compatibilidade para o AzureRM com `Enable-AzureRMAlias` enquanto você se familiariza com o novo conjunto de comandos.

## <a name="migrate-existing-scripts-to-az"></a>Migrar os scripts existentes para o Az

Atualizações importantes podem ser inconvenientes. No entanto, o módulo `Az` tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você trabalha nas atualizações da nova sintaxe. Use o cmdlet `Enable-AzureRmAlias` para habilitar o modo de compatibilidade do `AzureRM`. Esse cmdlet define os nomes de cmdlets `AzureRM` como aliases para os novos nomes de cmdlets `Az`.

Os novos nomes de cmdlets foram projetados para serem fáceis de aprender. Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`. Por exemplo, o comando antigo `New-AzureRmVm` tornou-se `New-AzVm`.

Para obter uma descrição completa do processo de migração, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>O futuro do suporte do AzureRM

O módulo `AzureRM` existente deixará de receber novos cmdlets ou recursos quando o `Az` versão 1.0 for lançado em dezembro de 2018. No entanto, o `AzureRM` ainda será oficialmente mantido e terá correções de bugs. Para se manter atualizado com os recursos e serviços do Azure mais recentes, você deve alternar para o módulo `Az`.