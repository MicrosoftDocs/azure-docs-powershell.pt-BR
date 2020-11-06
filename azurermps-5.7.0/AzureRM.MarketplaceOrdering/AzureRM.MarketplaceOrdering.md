---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: 198de5436453caf633288e23f804085319a30f73
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425576"
---
# <span data-ttu-id="a15d6-101">Módulo AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a15d6-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="a15d6-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="a15d6-102">Description</span></span>
<span data-ttu-id="a15d6-103">Os tópicos desta seção documentam os cmdlets do PowerShell do Azure para o MarketplaceOrdering do Azure na estrutura ARM (Azure Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="a15d6-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="a15d6-104">Os cmdlets existem no namespace Microsoft. Azure. Commands. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="a15d6-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="a15d6-105">Esses cmdlets permitem que os usuários do Azure aceitem os termos legais para um Marketplace oferecendo mais implantação programática para essas soluções.</span><span class="sxs-lookup"><span data-stu-id="a15d6-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="a15d6-106">Os usuários também podem rejeitar o conjunto de termos legais já aceitos.</span><span class="sxs-lookup"><span data-stu-id="a15d6-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="a15d6-107">Cmdlets AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a15d6-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="a15d6-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a15d6-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="a15d6-109">Obtenha os termos do contrato para um determinado ID de fornecedor (fornecedor), ID da oferta (produto) e ID do plano (nome).</span><span class="sxs-lookup"><span data-stu-id="a15d6-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a15d6-110">O objeto terms que é retornado por esse comando deve ser passado para Set-AzureRmMarketplaceTerms para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="a15d6-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="a15d6-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a15d6-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="a15d6-112">Aceitar ou rejeitar termos para um determinado ID de fornecedor (fornecedor), ID de oferta (produto) e ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="a15d6-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a15d6-113">Use Get-AzureRmMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="a15d6-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

