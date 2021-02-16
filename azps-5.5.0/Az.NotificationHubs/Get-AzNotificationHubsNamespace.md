---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118243"
---
# Get-AzNotificationHubsNamespace

## Sinopse
Obtém informações sobre um namespace do hub de notificação.

## Sintaxe

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
**O cmdlet Get-AzNotificationHubsNamespace** obtém informações sobre namespaces do hub de notificação.
Este cmdlet fornece a opção de obter informações para todos os seus namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um espaço de nome específico.
Os namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace do hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.
Um único namespace pode ter vários hubs, o que significa que talvez você só precise de um namespace em sua organização.
No entanto, você também pode ter vários namespaces para organizar melhor seus hubs ou para dar permissão a indivíduos específicos para gerenciar um subconjunto de hubs selecionado.
O **cmdlet Get-AzNotificationHubsNamespace retorna** informações básicas sobre o próprio namespace.
Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzNotificationHubsNamespaceAuthorizationRules.

## Exemplos

### Exemplo 1: Obter informações para todos os namespaces do hub de notificação
```
PS C:\>Get-AzNotificationHubsNamespace
```

Esse comando retorna informações para todos os namespaces do hub de notificação.

### Exemplo 2: Obter informações para um único espaço de nome do hub de notificação
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Este comando obtém informações para um único namespace de hub de notificação: ContosoNamespace.

### Exemplo 3: Obter informações para todos os hubs de notificação atribuídos a um espaço de nome específico
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações para todos os namespaces do hub de notificação atribuídos ao grupo de recursos ContosoNotificationsGroup.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Especifica um nome exclusivo para o namespace.
Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Especifica o grupo de recursos ao qual o namespace é atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## Notas

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


