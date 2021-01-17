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
# Módulo de suporte AZ
## Descritivo
Os tópicos desta seção documentam os cmdlets do Azure PowerShell para criar e gerenciar os tíquetes de suporte do Azure na estrutura ARM (Azure Resource Manager). Os cmdlets existem no namespace Microsoft. Azure. Commands. support

## Cmdlets AZ. support
### [Get-AzSupportService](Get-AzSupportService.md)
Obtém a lista atual de serviços do Azure para as quais há suporte disponível. Cada serviço do Azure tem seu próprio conjunto de categorias chamado classificação de problemas. Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification. Você pode usar o GUID de classificação de serviço e problema para criar um novo tíquete de suporte usando New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Obtém a lista atual de classificação de problemas para um serviço do Azure. Você pode usar o GUID de classificação de serviço e problema para criar um novo tíquete de suporte usando New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet de ajuda para criar um objeto de perfil de contato de suporte. Você pode usar esse objeto para New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Cria um novo tíquete de suporte do Azure. Esta operação tem o modelo do comportamento da [nova página de solicitação de suporte](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)do Azure.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Obtém a lista de tíquetes de suporte. Você pode obter detalhes de tíquete de suporte completo por nome do bilhete ou filtrar as permissões de suporte por *status* ou *CreatedDate*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Atualize a gravidade, o status ou os detalhes de contato do cliente do tíquete de suporte.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Obtém comunicações para um tíquete de suporte. Você também pode filtrar comunicações de tíquete de suporte por *CreatedDate* ou *communicationtype*. 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Adiciona uma nova comunicação de cliente a um tíquete de suporte do Azure. 



