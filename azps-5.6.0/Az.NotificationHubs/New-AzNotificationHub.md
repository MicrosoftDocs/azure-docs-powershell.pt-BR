---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885297"
---
# New-AzNotificationHub

## SYNOPSIS
Cria um hub de notificação.

## SINTAXE

### InputFileParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzNotificationHub** cria um hub de notificação.
Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.
Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.
O cmdlet **New-AzNotificationHub** fornece duas maneiras de criar um novo hub de notificação.
Você pode criar uma instância do **objeto NotificationHubAttributes** e configurar esse objeto.
Em seguida, você pode copiar esses valores de propriedade para seu novo hub por meio do *parâmetro NotificationHubObj.*
Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores usando o parâmetro *InputFile.*
Quando usado em conjunto com o cmdlet **New-AzNotificationHub,** o exemplo JSON anterior cria um hub de notificação chamado ContosoNotificationHub localizado no datacenter do Oeste dos EUA.

## EXEMPLOS

### Exemplo 1: Criar um hub de notificação
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Este comando cria um hub de notificação no namespace ContosoNamespace.
O novo hub será atribuído ao ContosoNotificationsGroup.
Você não precisa especificar um nome ou qualquer outra informação de configuração para o hub; essas informações serão retiradas do arquivo de entrada C:\Configurations\InternalHub.json.

## PARÂMETROS

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

### -InputFile
Especifica o caminho para um arquivo JSON que contém valores de configuração para o novo hub de notificação.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace ao qual o hub de notificação será atribuído.
Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.
Os hubs de notificação devem ser atribuídos a um namespace existente.
O cmdlet **New-AzNotificationHub** não pode criar um novo namespace.

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

### -NotificationHubObj
Especifica o **objeto NotificationHubAttributes** que contém informações de configuração para o novo hub.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Especifica o grupo de recursos ao qual o hub de notificação será atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.
Você deve usar um grupo de recursos existente.
O cmdlet **New-AzNotificationHub** não pode criar um novo grupo de recursos.

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## NOTES

## LINKS RELACIONADOS

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


