---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400613"
---
# Get-AzNotificationHub

## Sinopse
Obtém informações sobre seus hubs de notificação.

## Sintaxe

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Get-AzNotificationHub** obtém informações sobre os hubs de notificação em um espaço de nome especificado e atribuído a um grupo de recursos especificado.
Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.
Como alternativa, você pode usar o parâmetro *NotificationHub* para limitar os dados retornados a informações sobre um hub de notificação específico.
Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.
Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.
Este cmdlet obtém apenas informações sobre o hub em si.
Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre regras de autorização do hub, cadeias de conexão e credenciais de serviço de notificação de plataforma.

## Exemplos

### Exemplo 1: Obter informações para todos os hubs de notificação em um namespace específico
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos ao grupo de recursos ContosoNotificationsGroup.

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
Especifica o namespace ao qual o hub de notificação está atribuído.
Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.

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
Especifica o nome do hub de notificação que este cmdlet obtém.
Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Especifica o grupo de recursos ao qual o hub de notificação está atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## Notas

## LINKS RELACIONADOS




[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


