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
# Módulo Az.Support
## Descrição
Os tópicos neste documento de seção são cmdlets do Azure PowerShell para criar e gerenciar tíquetes de suporte do Azure na estrutura do Gerenciador de Recursos do Azure (ARM). Os cmdlets existem no namespace Microsoft.Azure.Commands.Support

## Az.Support Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Obtém a lista atual de serviços do Azure para os quais o suporte está disponível. Cada serviço do Azure tem seu próprio conjunto de categorias chamada classificação de problemas. Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification. Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando o New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Obtém a lista atual de classificação de problemas para um serviço do Azure. Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando o New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet auxiliar para criar um objeto de perfil de contato de suporte. Você pode usar esse objeto para New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Cria um novo tíquete de suporte do Azure. Esta operação é modelada no comportamento da página de solicitação de suporte do Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Obtém a lista de tíquetes de suporte. Você pode obter detalhes completos do tíquete de suporte por nome de tíquete ou filtrar os tíquetes de suporte *por Status* ou *CreatedDate.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Atualize a gravidade, o status ou os detalhes de contato do cliente de um tíquete de suporte.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Obtém comunicações para um tíquete de suporte. Você também pode filtrar as comunicações de tíquete de suporte *por CreatedDate* ou *CommunicationType.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Adiciona uma nova comunicação do cliente a um tíquete de suporte do Azure. 



