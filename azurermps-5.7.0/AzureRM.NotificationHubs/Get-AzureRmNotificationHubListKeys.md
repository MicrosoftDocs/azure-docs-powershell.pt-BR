---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 49bb03e903d465b372bc00118e15369f158661e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430386"
---
# Get-AzureRmNotificationHubListKeys

## Sinopse
Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmNotificationHubListKeys** retorna as cadeias de conexão primária e secundária de uma regra de autorização de assinatura de acesso compartilhado (SAS) do hub de notificação.

Regras de autorização gerenciem os direitos de usuário ao Hub.
Cada regra inclui uma cadeia de conexão principal e secundária.
Essas cadeias de conexão (URIs) executam o seguinte:

- Aponte os usuários para um recurso.
- Inclua um token contendo parâmetros de consulta.

Um desses parâmetros, a assinatura, é usado para autenticar o usuário e fornecer o nível de acesso especificado.

## EXEMPLOS

### Exemplo 1: obter as cadeias de conexão primária e secundária para uma regra de autorização
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Esse comando obtém as cadeias de conexão primária e secundária para a regra de autorização ListenRule, uma regra atribuída ao Hub de notificação ContosoInternalHub.
O comando deve incluir o namespace Hub e o grupo de recursos.

## OS

### -AuthorizationRule
Especifica o nome de uma regra de autenticação de assinatura de acesso compartilhado (SAS).
Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Especifica o Hub de notificação para o qual esse cmdlet atribui uma regra de autorização.
Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resource
Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)


