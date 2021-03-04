---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888775"
---
# <span data-ttu-id="a3629-101">Módulo Az.Support</span><span class="sxs-lookup"><span data-stu-id="a3629-101">Az.Support Module</span></span>
## <span data-ttu-id="a3629-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3629-102">Description</span></span>
<span data-ttu-id="a3629-103">Os tópicos desta seção documentam os cmdlets do Azure PowerShell para criar e gerenciar tíquetes de suporte do Azure na estrutura do Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="a3629-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="a3629-104">Os cmdlets existem no namespace Microsoft.Azure.Commands.Support</span><span class="sxs-lookup"><span data-stu-id="a3629-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="a3629-105">Az.Support Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a3629-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="a3629-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="a3629-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="a3629-107">Obtém a lista atual dos serviços do Azure para os quais o suporte está disponível.</span><span class="sxs-lookup"><span data-stu-id="a3629-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="a3629-108">Cada serviço do Azure tem seu próprio conjunto de categorias chamada classificação de problemas.</span><span class="sxs-lookup"><span data-stu-id="a3629-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="a3629-109">Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="a3629-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="a3629-110">Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="a3629-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="a3629-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="a3629-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="a3629-112">Obtém a lista atual de classificação de problemas para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3629-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="a3629-113">Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="a3629-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="a3629-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="a3629-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="a3629-115">Cmdlet auxiliar para criar um objeto de perfil de contato de suporte.</span><span class="sxs-lookup"><span data-stu-id="a3629-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="a3629-116">Você pode usar esse objeto para New-AzSupportTicket cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3629-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="a3629-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="a3629-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="a3629-118">Cria um novo tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3629-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="a3629-119">Essa operação é modelada no comportamento [](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)da página de solicitação de suporte novo do Azure .</span><span class="sxs-lookup"><span data-stu-id="a3629-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="a3629-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="a3629-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="a3629-121">Obtém a lista de tíquetes de suporte.</span><span class="sxs-lookup"><span data-stu-id="a3629-121">Gets the list of support tickets.</span></span> <span data-ttu-id="a3629-122">Você pode obter detalhes completos do tíquete de suporte pelo nome do tíquete ou filtrar os tíquetes de suporte *por Status* ou *CreatedDate*.</span><span class="sxs-lookup"><span data-stu-id="a3629-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="a3629-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="a3629-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="a3629-124">Atualize a gravidade, o status ou os detalhes de contato do cliente de um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="a3629-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="a3629-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="a3629-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="a3629-126">Obtém comunicações para um tíquete de suporte.</span><span class="sxs-lookup"><span data-stu-id="a3629-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="a3629-127">Você também pode filtrar as comunicações de tíquete de *suporte por CreatedDate* ou *CommunicationType*.</span><span class="sxs-lookup"><span data-stu-id="a3629-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="a3629-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="a3629-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="a3629-129">Adiciona uma nova comunicação do cliente a um tíquete de suporte do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3629-129">Adds a new customer communication to an Azure support ticket.</span></span> 



