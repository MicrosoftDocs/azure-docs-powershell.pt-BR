---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111783"
---
# Módulo Az.MarketplaceOrdering
## Descrição
Os tópicos neste documento de seção são cmdlets do Azure PowerShell para Azure MarketplaceOrdering na estrutura do Gerenciador de Recursos do Azure (ARM). Os cmdlets existem no namespace Microsoft.Azure.Commands.MarketplaceOrdering. Esses cmdlets permitem que os usuários do azure aceitem os termos legais para um marketplace, permitindo ainda mais a implantação programática para essas soluções. Os usuários também podem rejeitar o conjunto de termos legais já aceitos.

## Az.MarketplaceOrdering Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Obter os termos do contrato para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome). O objeto de termos que é retornado por este comando deve ser passado para Set-AzMarketplaceTerms aceitar os termos legais.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Aceitar ou rejeitar termos para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome). Use o Get-AzMarketplaceTerms para obter os termos do contrato.

