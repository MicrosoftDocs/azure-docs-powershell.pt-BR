---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427637"
---
# <span data-ttu-id="3c9d5-101">Módulo de suporte AZ</span><span class="sxs-lookup"><span data-stu-id="3c9d5-101">Az.Support Module</span></span>
## <span data-ttu-id="3c9d5-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="3c9d5-102">Description</span></span>
<span data-ttu-id="3c9d5-103">Os tópicos desta seção documentam os cmdlets do Azure PowerShell para criar e gerenciar os tíquetes de suporte do Azure na estrutura ARM (Azure Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="3c9d5-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="3c9d5-104">Os cmdlets existem no namespace Microsoft. Azure. Commands. support</span><span class="sxs-lookup"><span data-stu-id="3c9d5-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="3c9d5-105">Cmdlets AZ. support</span><span class="sxs-lookup"><span data-stu-id="3c9d5-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="3c9d5-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="3c9d5-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="3c9d5-107">Obtém a lista atual de serviços do Azure para as quais há suporte disponível.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="3c9d5-108">Cada serviço do Azure tem seu próprio conjunto de categorias chamado classificação de problemas.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="3c9d5-109">Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="3c9d5-110">Você pode usar o GUID de classificação de serviço e problema para criar um novo tíquete de suporte usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="3c9d5-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="3c9d5-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="3c9d5-112">Obtém a lista atual de classificação de problemas para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="3c9d5-113">Você pode usar o GUID de classificação de serviço e problema para criar um novo tíquete de suporte usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="3c9d5-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="3c9d5-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="3c9d5-115">Cmdlet de ajuda para criar um objeto de perfil de contato de suporte.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="3c9d5-116">Você pode usar esse objeto para New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="3c9d5-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3c9d5-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="3c9d5-118">Cria um novo tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="3c9d5-119">Esta operação tem o modelo do comportamento da [nova página de solicitação de suporte](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="3c9d5-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3c9d5-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="3c9d5-121">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-121">Gets the list of support tickets.</span></span> <span data-ttu-id="3c9d5-122">Você pode obter detalhes de tíquete de suporte completo por nome do bilhete ou filtrar as permissões de suporte por *status* ou *CreatedDate*.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="3c9d5-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3c9d5-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="3c9d5-124">Atualize a gravidade, o status ou os detalhes de contato do cliente do tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="3c9d5-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="3c9d5-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="3c9d5-126">Obtém comunicações para um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="3c9d5-127">Você também pode filtrar comunicações de tíquete de suporte por *CreatedDate* ou *communicationtype*.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="3c9d5-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="3c9d5-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="3c9d5-129">Adiciona uma nova comunicação de cliente a um tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9d5-129">Adds a new customer communication to an Azure support ticket.</span></span> 



