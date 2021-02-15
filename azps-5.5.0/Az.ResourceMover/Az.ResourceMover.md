---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118771"
---
# Módulo Az.ResourceMover
## Descrição
Microsoft Azure PowerShell: cmdlets ResourceMover

## Az.ResourceMover Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Cria ou atualiza um Recurso de Movimentação no conjunto de movimentações.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Obtém a coleção de movimentações.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Obtém o Recurso de Movimentação.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Obtém uma lista de dependências não resolvidas.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Confirma o conjunto de recursos incluídos no corpo da solicitação.
A operação de confirmação é disparada no moveResources no moveState "CommitPending" ou "CommitFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para Committed.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Descarta o conjunto de recursos incluído no corpo da solicitação.
A operação de descarte é disparada no moveResources no moveState "CommitPending" ou "DiscardFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para Mover Pendente.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Move o conjunto de recursos incluídos no corpo da solicitação.
A operação de movimentação é disparada depois que o moveResources está no moveState "MovePending" ou "MoveFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para CommitPending.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.
A operação de preparação está no moveResources que estão no moveState "PreparePending" ou "PrepareFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para Mover Pendente.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Cria ou atualiza uma coleção de movimentações.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Exclui uma coleção de movimentações.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Exclui um Recurso de Movimentação da coleção de movimentações.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Calcula, resolve e valida as dependências das moveResources na coleção de movimentações.

