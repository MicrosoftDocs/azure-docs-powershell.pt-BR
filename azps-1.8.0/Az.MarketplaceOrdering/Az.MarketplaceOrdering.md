---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93595378"
---
# Módulo AZ. MarketplaceOrdering
## Descritivo
Os tópicos desta seção documentam os cmdlets do PowerShell do Azure para o MarketplaceOrdering do Azure na estrutura ARM (Azure Resource Manager). Os cmdlets existem no namespace Microsoft. Azure. Commands. MarketplaceOrdering. Esses cmdlets permitem que os usuários do Azure aceitem os termos legais para um Marketplace oferecendo mais implantação programática para essas soluções. Os usuários também podem rejeitar o conjunto de termos legais já aceitos.

## Cmdlets AZ. MarketplaceOrdering
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Obtenha os termos do contrato para um determinado ID de fornecedor (fornecedor), ID da oferta (produto) e ID do plano (nome). O objeto terms que é retornado por esse comando deve ser passado para Set-AzMarketplaceTerms para aceitar os termos legais.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Aceitar ou rejeitar termos para um determinado ID de fornecedor (fornecedor), ID de oferta (produto) e ID de plano (nome). Use Get-AzMarketplaceTerms para obter os termos do contrato.

