---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 6fc2cfd47d9b03fc02d935245d1ec87d6831d173
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944507"
---
# Get-AzNotificationHub

## Sinopse
Obtém informações sobre seus hubs de notificação.

## SYNTAX

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzNotificationHub** Obtém informações sobre os hubs de notificação em um namespace especificado e atribuídos a um grupo de recursos especificado.
Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.
Você também pode usar o parâmetro *NotificationHub* para limitar os dados retornados às informações sobre um hub de notificação específico.
Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.
Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.
Este cmdlet somente Obtém informações sobre o próprio Hub.
Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre as regras de autorização de um Hub, cadeias de conexão e credenciais do serviço de notificação de plataforma.

## EXEMPLOS

### Exemplo 1: obter informações para todos os hubs de notificação em um namespace específico
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos à ContosoNotificationsGroup do grupo de recursos.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
Especifica o namespace ao qual o Hub de notificações está atribuído.
Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.

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
Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.

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

### -Resource
Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzNotificationHubAuthorizationRules](./Get-AzNotificationHubAuthorizationRules.md)

[Get-AzNotificationHubListKeys](./Get-AzNotificationHubListKeys.md)

[Get-AzNotificationHubPNSCredentials](./Get-AzNotificationHubPNSCredentials.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


