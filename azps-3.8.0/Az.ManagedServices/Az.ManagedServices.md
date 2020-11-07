---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944202"
---
# <span data-ttu-id="7c267-101">Módulo AZ. Managedservices</span><span class="sxs-lookup"><span data-stu-id="7c267-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="7c267-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="7c267-102">Description</span></span>
<span data-ttu-id="7c267-103">Esse recurso é usado por clientes dos provedores de serviços gerenciados (MSPs).</span><span class="sxs-lookup"><span data-stu-id="7c267-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="7c267-104">Os clientes dão ao MSP a capacidade de gerenciar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="7c267-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="7c267-105">Além de conceder acesso, o cliente também pode remover o acesso ou exibir as delegações de acesso existentes.</span><span class="sxs-lookup"><span data-stu-id="7c267-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="7c267-106">O MSPs pode ver a lista de clientes que lhes conceder acesso a assinaturas.</span><span class="sxs-lookup"><span data-stu-id="7c267-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="7c267-107">Há dois objetos envolvidos nesse processo: uma definição de registro que identifica o MSP e as definições de função concedidas ao MSP.</span><span class="sxs-lookup"><span data-stu-id="7c267-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="7c267-108">Opcionalmente, o MSP pode definir esse objeto usando um Marketplace de serviços gerenciados oferecendo atribuições de acesso que associam uma assinatura com a definição.</span><span class="sxs-lookup"><span data-stu-id="7c267-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="7c267-109">Cmdlets AZ. Managedservices</span><span class="sxs-lookup"><span data-stu-id="7c267-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="7c267-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c267-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="7c267-111">Obtém uma lista das tarefas de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="7c267-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c267-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="7c267-113">Obtém uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="7c267-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c267-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="7c267-115">Cria uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="7c267-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c267-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="7c267-117">Cria uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="7c267-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7c267-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="7c267-119">Exclui a atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="7c267-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7c267-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="7c267-121">Exclui a definição de registro.</span><span class="sxs-lookup"><span data-stu-id="7c267-121">Deletes the registration definition.</span></span>

