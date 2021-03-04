---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 260cf95d04d6a923acbdeaa91a412aa0046d9ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885312"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Obtém informações sobre as regras de autorização associadas a um hub de notificação.

## SINTAXE

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzNotificationHubAuthorizationRule** obtém informações sobre as regras de autorização da Assinatura de Acesso Compartilhado (SAS) associadas a um hub de notificação.
O cmdlet retorna informações sobre todas as regras associadas a um hub ou, incluindo o parâmetro *AuthorizationRule,* obtém informações sobre uma regra específica.
As regras de autorização gerenciam o acesso aos hubs de notificação.
Uma regra de autorização criará links, como URI, com base em diferentes níveis de permissão.
Os clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.
Por exemplo, um cliente com a permissão Ouvir será direcionado para o URI para essa permissão.
O cmdlet **Get-AzNotificationHubAuthorizationRule** só obtém informações sobre as regras de autorização associadas a um hub de notificação.
Para obter informações sobre o hub em si, use Get-AzNotificationHub.

## EXEMPLOS

### Exemplo 1: obter informações para todas as regras de autorização atribuídas a um hub de notificação
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Este comando obtém informações de todas as regras de autorização atribuídas ao hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.
Você deve especificar o namespace no qual o hub está localizado, bem como o grupo de recursos ao qual o hub foi atribuído.

### Exemplo 2: obter informações sobre regras de autorização atribuídas a um hub de notificação
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Este comando obtém informações de todas as regras de autorização atribuídas ao hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.
O comando usa o *parâmetro AuthorizationRule* para limitar os dados retornados a uma única regra de autorização chamada ListenRule.

## PARÂMETROS

### -AuthorizationRule
Especifica o nome de uma regra de autenticação SAS.
Essas regras determinam o tipo de acesso que os usuários têm ao hub de notificação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace ao qual o hub de notificação é atribuído.
Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Especifica o hub de notificação que este cmdlet atribui regras de autorização.
Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Especifica o grupo de recursos ao qual o hub de notificação é atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplificar o gerenciamento de inventário e a administração do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTES

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


