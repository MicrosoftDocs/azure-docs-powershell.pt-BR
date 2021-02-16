---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113590"
---
# <span data-ttu-id="ca505-101">Módulo Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ca505-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="ca505-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca505-102">Description</span></span>
<span data-ttu-id="ca505-103">Esse recurso é usado pelos clientes de MSPs (Provedores de Serviços Gerenciados).</span><span class="sxs-lookup"><span data-stu-id="ca505-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="ca505-104">Os clientes dão a um MSP a capacidade de gerenciar sua assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca505-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="ca505-105">Além de conceder acesso, o cliente também pode remover o acesso ou exibir o acesso existente.</span><span class="sxs-lookup"><span data-stu-id="ca505-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="ca505-106">Os MSPs podem exibir a lista de clientes que concederam a eles acesso às assinaturas.</span><span class="sxs-lookup"><span data-stu-id="ca505-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="ca505-107">Há dois objetos envolvidos neste processo: uma definição de registro que identifica o MSP e as definições de função concedidas aos usuários do MSP.</span><span class="sxs-lookup"><span data-stu-id="ca505-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="ca505-108">Opcionalmente, o MSP pode definir esse objeto usando um marketplace de Serviços Gerenciados que oferece atribuições do Access que associam uma assinatura à definição.</span><span class="sxs-lookup"><span data-stu-id="ca505-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="ca505-109">Az.ManagedServices Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ca505-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="ca505-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="ca505-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="ca505-111">Obtém uma atribuição de registro específica ou uma lista das atribuições de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="ca505-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ca505-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="ca505-113">Obtém uma definição de registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="ca505-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="ca505-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="ca505-115">Cria ou atualiza uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="ca505-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ca505-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="ca505-117">Cria ou atualiza uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="ca505-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="ca505-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="ca505-119">Remove uma atribuição de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="ca505-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ca505-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="ca505-121">Remove uma definição de registro.</span><span class="sxs-lookup"><span data-stu-id="ca505-121">Removes a registration definition.</span></span>
