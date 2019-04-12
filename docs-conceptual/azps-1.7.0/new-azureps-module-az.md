---
title: Apresentação do módulo do Azure PowerShell
description: Apresentação do novo módulo Az do Azure PowerShell, a substituição pelo módulo AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363949"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Apresentação do novo módulo Az do Azure PowerShell

A partir de dezembro de 2018, o módulo Az do Azure PowerShell foi lançado e é agora o módulo do PowerShell utilizado para interagir com o Azure. O Az oferece comandos menores, maior estabilidade e dá suporte à plataforma cruzada. O Az também oferece paridade de recursos e um caminho de migração fácil do AzureRM.

O Az usa a biblioteca .NET Standard, ou seja, ele é executado no PowerShell 5 e no PowerShell 6.
Como o PowerShell 6 pode ser executado no Linux, macOS e Windows, o Azure PowerShell agora está disponível para todas as plataformas.
O .NET Standard permite unificar a base de código do Azure PowerShell com impacto mínimo para os usuários.

O Az é um novo módulo, portanto, a versão foi redefinida para 1.0.0.

## <a name="upgrade-to-az"></a>Atualizar para o Az

É recomendável que todos os usuários atualizem para o novo módulo Az. Para fazer isso:

* __RECOMENDÁVEL__: [Desinstalar o módulo AzureRM do Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Instalar o módulo Az do Azure PowerShell](/powershell/azure/install-az-ps)
* Habilitar o modo de compatibilidade para adicionar aliases para cmdlets AzureRM com `Enable-AzureRMAlias` enquanto você se familiariza com o novo conjunto de comandos. Habilite __apenas__ os aliases se você não tiver o AzureRM instalado.

## <a name="migrate-existing-scripts-to-az"></a>Migrar os scripts existentes para o Az

Atualizações importantes podem ser inconvenientes. No entanto, o módulo Az tem um modo de compatibilidade para ajudá-lo a usar os scripts existentes enquanto você trabalha nas atualizações da nova sintaxe. Use o cmdlet `Enable-AzureRmAlias` para habilitar o modo de compatibilidade do AzureRM. Esse cmdlet define os nomes de cmdlets AzureRM como aliases para os novos nomes de cmdlets Az.

Os novos nomes de cmdlets foram projetados para serem fáceis de aprender. Em vez de usar `AzureRm` ou `Azure` nos nomes de cmdlets, use `Az`. Por exemplo, o comando antigo `New-AzureRMVm` tornou-se `New-AzVm`.

Para obter uma descrição completa do processo de migração, confira [Migrar do AzureRM para o Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>O futuro do suporte do AzureRM

O módulo AzureRM existente deixará de receber novos cmdlets ou recursos. No entanto, o AzureRM ainda será oficialmente mantido e terá correções de bugs até dezembro de 2020. Para se manter atualizado com os recursos e serviços do Azure mais recentes, você deve trocar para o módulo Az.
