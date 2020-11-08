---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111948"
---
# Módulo AZ. ResourceMover
## Descritivo
Microsoft Azure PowerShell: cmdlets do ResourceMover

## Cmdlets AZ. ResourceMover
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Cria ou atualiza um recurso de movimentação na coleção move.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Obtém a coleção mover.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Obtém o recurso mover.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Obtém uma lista de dependências não resolvidas.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Confirma o conjunto de recursos incluídos no corpo da solicitação.
A operação de confirmação é disparada no moveResources em movestate ' CommitPending ' ou ' CommitFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para Committed.
Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Descarta o conjunto de recursos incluídos no corpo da solicitação.
A operação de descarte é disparada no moveResources em movestate ' CommitPending ' ou ' DiscardFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.
Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Move o conjunto de recursos incluídos no corpo da solicitação.
A operação de movimentação é disparada depois que o moveResources está em movestate ' MovePending ' ou ' MoveFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para CommitPending.
Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.
A operação de preparação está em moveResources que estão em movestate ' PreparePending ' ou ' PrepareFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.
Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Cria ou atualiza uma coleção de movimentação.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Exclui uma coleção de movimentação.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Exclui um recurso de movimentação da coleção move.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Calcula, resolve e valida as dependências do moveResources na coleção move.

