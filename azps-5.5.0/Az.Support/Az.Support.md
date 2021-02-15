---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112428"
---
# <span data-ttu-id="42ac0-101">Módulo Az.Support</span><span class="sxs-lookup"><span data-stu-id="42ac0-101">Az.Support Module</span></span>
## <span data-ttu-id="42ac0-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="42ac0-102">Description</span></span>
<span data-ttu-id="42ac0-103">Os tópicos neste documento de seção são cmdlets do Azure PowerShell para criar e gerenciar tíquetes de suporte do Azure na estrutura do Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="42ac0-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="42ac0-104">Os cmdlets existem no namespace Microsoft.Azure.Commands.Support</span><span class="sxs-lookup"><span data-stu-id="42ac0-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="42ac0-105">Az.Support Cmdlets</span><span class="sxs-lookup"><span data-stu-id="42ac0-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="42ac0-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="42ac0-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="42ac0-107">Obtém a lista atual de serviços do Azure para os quais o suporte está disponível.</span><span class="sxs-lookup"><span data-stu-id="42ac0-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="42ac0-108">Cada serviço do Azure tem seu próprio conjunto de categorias chamada classificação de problemas.</span><span class="sxs-lookup"><span data-stu-id="42ac0-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="42ac0-109">Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="42ac0-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="42ac0-110">Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando o New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="42ac0-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="42ac0-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="42ac0-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="42ac0-112">Obtém a lista atual de classificação de problemas para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="42ac0-113">Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando o New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="42ac0-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="42ac0-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="42ac0-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="42ac0-115">Cmdlet auxiliar para criar um objeto de perfil de contato de suporte.</span><span class="sxs-lookup"><span data-stu-id="42ac0-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="42ac0-116">Você pode usar esse objeto para New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ac0-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="42ac0-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="42ac0-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="42ac0-118">Cria um novo tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="42ac0-119">Esta operação é modelada no comportamento da página de solicitação de suporte do Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="42ac0-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="42ac0-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="42ac0-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="42ac0-121">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="42ac0-121">Gets the list of support tickets.</span></span> <span data-ttu-id="42ac0-122">Você pode obter detalhes completos do tíquete de suporte por nome de tíquete ou filtrar os tíquetes de suporte *por Status* ou *CreatedDate.*</span><span class="sxs-lookup"><span data-stu-id="42ac0-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="42ac0-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="42ac0-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="42ac0-124">Atualize a gravidade, o status ou os detalhes de contato do cliente de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="42ac0-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="42ac0-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="42ac0-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="42ac0-126">Obtém comunicações para um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="42ac0-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="42ac0-127">Você também pode filtrar as comunicações de tíquete de suporte *por CreatedDate* ou *CommunicationType.*</span><span class="sxs-lookup"><span data-stu-id="42ac0-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="42ac0-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="42ac0-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="42ac0-129">Adiciona uma nova comunicação do cliente a um tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac0-129">Adds a new customer communication to an Azure support ticket.</span></span> 



