---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117692"
---
# <span data-ttu-id="1cb9e-101">Módulo AZ. Managedservices</span><span class="sxs-lookup"><span data-stu-id="1cb9e-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="1cb9e-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="1cb9e-102">Description</span></span>
<span data-ttu-id="1cb9e-103">Esse recurso é usado por clientes dos provedores de serviços gerenciados (MSPs).</span><span class="sxs-lookup"><span data-stu-id="1cb9e-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="1cb9e-104">Os clientes dão ao MSP a capacidade de gerenciar a assinatura ou o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="1cb9e-105">Além de conceder acesso, o cliente também pode remover o acesso ou exibir o acesso existente.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="1cb9e-106">O MSPs pode ver a lista de clientes que lhes conceder acesso a assinaturas.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="1cb9e-107">Há dois objetos envolvidos nesse processo: uma definição de registro que identifica o MSP e as definições de função concedidas aos usuários do MSP.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="1cb9e-108">Opcionalmente, o MSP pode definir esse objeto usando um Marketplace de serviços gerenciados oferecendo atribuições de acesso que associam uma assinatura com a definição.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="1cb9e-109">Cmdlets AZ. Managedservices</span><span class="sxs-lookup"><span data-stu-id="1cb9e-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="1cb9e-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb9e-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="1cb9e-111">Obtém uma atribuição de Registro específica ou uma lista de atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="1cb9e-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb9e-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="1cb9e-113">Obtém uma definição de Registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="1cb9e-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb9e-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="1cb9e-115">Cria ou atualiza uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="1cb9e-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb9e-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="1cb9e-117">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="1cb9e-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb9e-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="1cb9e-119">Remove uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="1cb9e-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb9e-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="1cb9e-121">Remove uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="1cb9e-121">Removes a registration definition.</span></span>
