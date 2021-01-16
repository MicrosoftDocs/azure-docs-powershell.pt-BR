---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258752"
---
# Get-AzNotificationHubsNamespace

## Sinopse
Obtém informações sobre um namespace do hub de notificação.

## SYNTAX

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
**O cmdlet Get-AzNotificationHubsNamespace** Obtém informações sobre namespaces do hub de notificação.
Esse cmdlet oferece a opção de obter informações para todos os namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um namespace específico.
Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace de Hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.
Um único namespace pode alojar vários hubs, o que significa que você pode só precisar de um namespace em sua organização.
No entanto, você também pode ter vários namespaces para organizar melhor seus hubs, ou para dar a pessoas específicas permissão para gerenciar um subconjunto de hubs selecionado.
O cmdlet **Get-AzNotificationHubsNamespace** retorna informações básicas sobre o próprio namespace.
Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzNotificationHubsNamespaceAuthorizationRules.

## EXEMPLOS

### Exemplo 1: obter informações para todos os namespaces do hub de notificação
```
PS C:\>Get-AzNotificationHubsNamespace
```

Esse comando retorna informações para todos os namespaces do hub de notificação.

### Exemplo 2: obter informações para um único namespace Hub de notificação
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Esse comando obtém informações para um único namespace Hub de notificação: ContosoNamespace.

### Exemplo 3: obter informações para todos os hubs de notificação atribuídos a um namespace específico
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações para todos os namespaces do hub de notificação atribuídos à ContosoNotificationsGroup do grupo de recursos.

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
Especifica um nome exclusivo para o namespace.
Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.

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

### -Resource
Especifica o grupo de recursos ao qual o namespace está atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


