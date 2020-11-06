---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 57b810c448c739b6346a410284272e26b44d3aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428857"
---
# New-AzureRmNotificationHub

## Sinopse
Cria um hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### InputFileParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmNotificationHub** cria um hub de notificação.
Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.
Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.

O cmdlet **New-AzureRmNotificationHub** fornece duas maneiras de criar um novo hub de notificação.
Você pode criar uma instância do objeto **NotificationHubAttributes** e, em seguida, configurar esse objeto.
Em seguida, você pode copiar esses valores de propriedade para o novo hub por meio do parâmetro *NotificationHubObj* .

Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores usando o parâmetro *InputFile* .

Quando usado em conjunto com o cmdlet **New-AzureRmNotificationHub** , o exemplo JSON anterior cria um hub de notificação chamado ContosoNotificationHub localizado no datacenter dos EUA.

## EXEMPLOS

### Exemplo 1: criar um hub de notificação
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Esse comando cria um hub de notificação no namespace ContosoNamespace.
O novo hub será atribuído ao ContosoNotificationsGroup.
Você não precisa especificar um nome ou outras informações de configuração para o Hub; essas informações serão tiradas do arquivo de entrada C:\Configurations\InternalHub.js.

## OS

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

### -InputFile
Especifica o caminho para um arquivo JSON contendo valores de configuração para o novo hub de notificação.

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace ao qual o Hub de notificações será atribuído.

Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.
Os hubs de notificação devem ser atribuídos a um namespace existente.
O cmdlet **New-AzureRmNotificationHub** não pode criar um novo namespace.

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

### -NotificationHubObj
Especifica o objeto **NotificationHubAttributes** que contém informações de configuração para o novo hub.

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resource
Especifica o grupo de recursos ao qual o Hub de notificações será atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

Você deve usar um grupo de recursos existente.
O cmdlet **New-AzureRmNotificationHub** não pode criar um novo grupo de recursos.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNotificationHub](./Get-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


