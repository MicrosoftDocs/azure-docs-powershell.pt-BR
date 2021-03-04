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
# Módulo Az.Support
## Descrição
Os tópicos desta seção documentam os cmdlets do Azure PowerShell para criar e gerenciar tíquetes de suporte do Azure na estrutura do Gerenciador de Recursos do Azure (ARM). Os cmdlets existem no namespace Microsoft.Azure.Commands.Support

## Az.Support Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Obtém a lista atual dos serviços do Azure para os quais o suporte está disponível. Cada serviço do Azure tem seu próprio conjunto de categorias chamada classificação de problemas. Obter a lista atual de classificação de problemas para um serviço usando Get-AzSupportProblemClassification. Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Obtém a lista atual de classificação de problemas para um serviço do Azure. Você pode usar o GUID de classificação de problemas e serviço para criar um novo tíquete de suporte usando New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Cmdlet auxiliar para criar um objeto de perfil de contato de suporte. Você pode usar esse objeto para New-AzSupportTicket cmdlet.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Cria um novo tíquete de suporte do Azure. Essa operação é modelada no comportamento [](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)da página de solicitação de suporte novo do Azure .

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Obtém a lista de tíquetes de suporte. Você pode obter detalhes completos do tíquete de suporte pelo nome do tíquete ou filtrar os tíquetes de suporte *por Status* ou *CreatedDate*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Atualize a gravidade, o status ou os detalhes de contato do cliente de um tíquete de suporte.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Obtém comunicações para um tíquete de suporte. Você também pode filtrar as comunicações de tíquete de *suporte por CreatedDate* ou *CommunicationType*. 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Adiciona uma nova comunicação do cliente a um tíquete de suporte do Azure. 



