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
# Módulo Az.ResourceMover
## Descrição
Microsoft Azure PowerShell: cmdlets ResourceMover

## Az.ResourceMover Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Cria ou atualiza um Recurso move na coleção move.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Obtém a coleção move.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Obtém o Recurso de Movimentação.

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
Lista dos recursos de movimentação para os quais um recurso arm é necessário.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Obtém uma lista de dependências não resolvidas.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
Remove o conjunto de recursos de movimentação incluídos no corpo da solicitação da coleção move.
A orquestração é feita por serviço.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Confirma o conjunto de recursos incluídos no corpo da solicitação.
A operação de confirmação é disparada no moveResources no moveState 'CommitPending' ou 'CommitFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para Committed.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Descarta o conjunto de recursos incluídos no corpo da solicitação.
A operação de descarte é disparada no moveResources no moveState 'CommitPending' ou 'DiscardFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para MovePending.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Move o conjunto de recursos incluídos no corpo da solicitação.
A operação de movimentação é disparada depois que moveResources estão no moveState 'MovePending' ou 'MoveFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para CommitPending.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.
A operação de preparação está no moveResources que estão no moveState 'PreparePending' ou 'PrepareFailed', em uma conclusão bem-sucedida, moveResource moveState fazer uma transição para MovePending.
Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Cria ou atualiza uma coleção de movimentação.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Exclui uma coleção move.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Exclui um Recurso de Movimentação da coleção move.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Calcula, resolve e valida as dependências do moveResources na coleção move.

