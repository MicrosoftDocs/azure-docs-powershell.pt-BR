---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429211"
---
# Get-AzureRmNotificationHubsNamespace

## Sinopse
Obtém informações sobre um namespace do hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
**O cmdlet Get-AzureRmNotificationHubsNamespace** Obtém informações sobre namespaces do hub de notificação.
Esse cmdlet oferece a opção de obter informações para todos os namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um namespace específico.

Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace de Hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.
Um único namespace pode alojar vários hubs, o que significa que você pode só precisar de um namespace em sua organização.
No entanto, você também pode ter vários namespaces para organizar melhor seus hubs, ou para dar a pessoas específicas permissão para gerenciar um subconjunto de hubs selecionado.

O cmdlet **Get-AzureRmNotificationHubsNamespace** retorna informações básicas sobre o próprio namespace.
Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.

## EXEMPLOS

### Exemplo 1: obter informações para todos os namespaces do hub de notificação
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

Esse comando retorna informações para todos os namespaces do hub de notificação.

### Exemplo 2: obter informações para um único namespace Hub de notificação
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Esse comando obtém informações para um único namespace Hub de notificação: ContosoNamespace.

### Exemplo 3: obter informações para todos os hubs de notificação atribuídos a um namespace específico
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações para todos os namespaces do hub de notificação atribuídos à ContosoNotificationsGroup do grupo de recursos.

## OS

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes]

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


