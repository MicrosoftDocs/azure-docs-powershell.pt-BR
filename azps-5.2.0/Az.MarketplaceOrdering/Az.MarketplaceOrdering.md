---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257691"
---
# <span data-ttu-id="e3291-101">Módulo AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e3291-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="e3291-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="e3291-102">Description</span></span>
<span data-ttu-id="e3291-103">Os tópicos desta seção documentam os cmdlets do PowerShell do Azure para o MarketplaceOrdering do Azure na estrutura ARM (Azure Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="e3291-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="e3291-104">Os cmdlets existem no namespace Microsoft. Azure. Commands. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="e3291-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="e3291-105">Esses cmdlets permitem que os usuários do Azure aceitem os termos legais para um Marketplace oferecendo mais implantação programática para essas soluções.</span><span class="sxs-lookup"><span data-stu-id="e3291-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="e3291-106">Os usuários também podem rejeitar o conjunto de termos legais já aceitos.</span><span class="sxs-lookup"><span data-stu-id="e3291-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="e3291-107">Cmdlets AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e3291-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="e3291-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="e3291-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="e3291-109">Obtenha os termos do contrato para um determinado ID de fornecedor (fornecedor), ID da oferta (produto) e ID do plano (nome).</span><span class="sxs-lookup"><span data-stu-id="e3291-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="e3291-110">O objeto terms que é retornado por esse comando deve ser passado para Set-AzMarketplaceTerms para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="e3291-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="e3291-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="e3291-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="e3291-112">Aceitar ou rejeitar termos para um determinado ID de fornecedor (fornecedor), ID de oferta (produto) e ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="e3291-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="e3291-113">Use Get-AzMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="e3291-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

