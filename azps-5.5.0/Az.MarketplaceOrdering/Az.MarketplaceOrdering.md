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
# <span data-ttu-id="762a4-101">Módulo Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="762a4-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="762a4-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="762a4-102">Description</span></span>
<span data-ttu-id="762a4-103">Os tópicos neste documento de seção são cmdlets do Azure PowerShell para Azure MarketplaceOrdering na estrutura do Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="762a4-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="762a4-104">Os cmdlets existem no namespace Microsoft.Azure.Commands.MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="762a4-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="762a4-105">Esses cmdlets permitem que os usuários do azure aceitem os termos legais para um marketplace, permitindo ainda mais a implantação programática para essas soluções.</span><span class="sxs-lookup"><span data-stu-id="762a4-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="762a4-106">Os usuários também podem rejeitar o conjunto de termos legais já aceitos.</span><span class="sxs-lookup"><span data-stu-id="762a4-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="762a4-107">Az.MarketplaceOrdering Cmdlets</span><span class="sxs-lookup"><span data-stu-id="762a4-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="762a4-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="762a4-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="762a4-109">Obter os termos do contrato para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome).</span><span class="sxs-lookup"><span data-stu-id="762a4-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="762a4-110">O objeto de termos que é retornado por este comando deve ser passado para Set-AzMarketplaceTerms aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="762a4-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="762a4-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="762a4-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="762a4-112">Aceitar ou rejeitar termos para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome).</span><span class="sxs-lookup"><span data-stu-id="762a4-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="762a4-113">Use o Get-AzMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="762a4-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

