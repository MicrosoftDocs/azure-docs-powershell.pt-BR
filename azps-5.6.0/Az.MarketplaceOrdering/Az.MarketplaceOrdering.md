---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890388"
---
# Módulo Az.MarketplaceOrdering
## Descrição
Os tópicos desta seção documentam os cmdlets do Azure PowerShell para o Azure MarketplaceOrdering na estrutura do Gerenciador de Recursos do Azure (ARM). Os cmdlets existem no namespace Microsoft.Azure.Commands.MarketplaceOrdering. Esses cmdlets permitem que os usuários do azure aceitem os termos legais para um marketplace oferecendo ainda mais a implantação programática para essas soluções. Os usuários também podem rejeitar o conjunto de termos legais já aceitos.

## Az.MarketplaceOrdering Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Obter os termos de contrato para um determinado publisher id(Publisher), id(Product) e plan id(Name). O objeto terms retornado por este comando deve ser passado para Set-AzMarketplaceTerms aceitar os termos legais.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Aceitar ou rejeitar termos para um determinado publisher id(Publisher), id(Product) e plan id(Name). Use o Get-AzMarketplaceTerms para obter os termos do contrato.

