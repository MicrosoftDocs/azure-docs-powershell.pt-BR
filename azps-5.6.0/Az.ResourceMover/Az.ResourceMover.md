---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891658"
---
# <span data-ttu-id="db97a-101">Módulo Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="db97a-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="db97a-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="db97a-102">Description</span></span>
<span data-ttu-id="db97a-103">Microsoft Azure PowerShell: cmdlets ResourceMover</span><span class="sxs-lookup"><span data-stu-id="db97a-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="db97a-104">Az.ResourceMover Cmdlets</span><span class="sxs-lookup"><span data-stu-id="db97a-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="db97a-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="db97a-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="db97a-106">Cria ou atualiza um Recurso move na coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="db97a-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="db97a-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="db97a-108">Obtém a coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-108">Gets the move collection.</span></span>

### [<span data-ttu-id="db97a-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="db97a-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="db97a-110">Obtém o Recurso de Movimentação.</span><span class="sxs-lookup"><span data-stu-id="db97a-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="db97a-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="db97a-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="db97a-112">Lista dos recursos de movimentação para os quais um recurso arm é necessário.</span><span class="sxs-lookup"><span data-stu-id="db97a-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="db97a-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="db97a-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="db97a-114">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="db97a-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="db97a-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="db97a-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="db97a-116">Remove o conjunto de recursos de movimentação incluídos no corpo da solicitação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="db97a-117">A orquestração é feita por serviço.</span><span class="sxs-lookup"><span data-stu-id="db97a-117">The orchestration is done by service.</span></span>
<span data-ttu-id="db97a-118">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="db97a-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="db97a-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="db97a-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="db97a-120">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="db97a-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="db97a-121">A operação de confirmação é disparada no moveResources no moveState 'CommitPending' ou 'CommitFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="db97a-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="db97a-122">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="db97a-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="db97a-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="db97a-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="db97a-124">Descarta o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="db97a-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="db97a-125">A operação de descarte é disparada no moveResources no moveState 'CommitPending' ou 'DiscardFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="db97a-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="db97a-126">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="db97a-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="db97a-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="db97a-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="db97a-128">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="db97a-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="db97a-129">A operação de movimentação é disparada depois que moveResources estão no moveState 'MovePending' ou 'MoveFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="db97a-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="db97a-130">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="db97a-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="db97a-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="db97a-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="db97a-132">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="db97a-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="db97a-133">A operação de preparação está no moveResources que estão no moveState 'PreparePending' ou 'PrepareFailed', em uma conclusão bem-sucedida, moveResource moveState fazer uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="db97a-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="db97a-134">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="db97a-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="db97a-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="db97a-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="db97a-136">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="db97a-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="db97a-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="db97a-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="db97a-138">Exclui uma coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="db97a-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="db97a-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="db97a-140">Exclui um Recurso de Movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="db97a-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="db97a-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="db97a-142">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="db97a-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

