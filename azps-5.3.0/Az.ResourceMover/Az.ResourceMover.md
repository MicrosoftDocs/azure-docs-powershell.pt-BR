---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271562"
---
# <span data-ttu-id="96372-101">Módulo AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="96372-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="96372-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="96372-102">Description</span></span>
<span data-ttu-id="96372-103">Microsoft Azure PowerShell: cmdlets do ResourceMover</span><span class="sxs-lookup"><span data-stu-id="96372-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="96372-104">Cmdlets AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="96372-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="96372-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="96372-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="96372-106">Cria ou atualiza um recurso de movimentação na coleção move.</span><span class="sxs-lookup"><span data-stu-id="96372-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="96372-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="96372-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="96372-108">Obtém a coleção mover.</span><span class="sxs-lookup"><span data-stu-id="96372-108">Gets the move collection.</span></span>

### [<span data-ttu-id="96372-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="96372-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="96372-110">Obtém o recurso mover.</span><span class="sxs-lookup"><span data-stu-id="96372-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="96372-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="96372-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="96372-112">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="96372-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="96372-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="96372-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="96372-114">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="96372-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="96372-115">A operação de confirmação é disparada no moveResources em movestate ' CommitPending ' ou ' CommitFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="96372-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="96372-116">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="96372-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="96372-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="96372-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="96372-118">Descarta o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="96372-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="96372-119">A operação de descarte é disparada no moveResources em movestate ' CommitPending ' ou ' DiscardFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="96372-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="96372-120">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="96372-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="96372-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="96372-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="96372-122">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="96372-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="96372-123">A operação de movimentação é disparada depois que o moveResources está em movestate ' MovePending ' ou ' MoveFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="96372-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="96372-124">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="96372-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="96372-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="96372-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="96372-126">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="96372-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="96372-127">A operação de preparação está em moveResources que estão em movestate ' PreparePending ' ou ' PrepareFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="96372-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="96372-128">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="96372-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="96372-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="96372-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="96372-130">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="96372-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="96372-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="96372-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="96372-132">Exclui uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="96372-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="96372-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="96372-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="96372-134">Exclui um recurso de movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="96372-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="96372-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="96372-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="96372-136">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="96372-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

