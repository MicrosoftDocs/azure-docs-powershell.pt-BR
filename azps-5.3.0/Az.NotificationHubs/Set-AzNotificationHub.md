---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272587"
---
# Set-AzNotificationHub

## Sinopse
Define valores de propriedade para um hub de notificação.

## SYNTAX

### InputFileParameterSet
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzNotificationHub** modifica os valores de propriedade de um hub de notificação.
Você pode modificar um valor de propriedade de Hub de notificação de duas maneiras.
Para um, você pode criar uma instância do objeto **NotificationHubAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que o novo hub possua.
Isso pode ser feito por meio do .NET Framework.
Em seguida, você pode copiar esses valores de propriedade para o seu hub por meio do parâmetro *NotificationHubObj* .
Você também pode criar um arquivo JSON (JavaScript Object Notation) que contenha os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .
Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte: {  
    "Nome": "ContosoNotificationHub",  
    "Local": "Oeste EUA",  
} Quando usado em conjunto com o cmdlet **set-AzNotificationHub** , o exemplo JSON anterior define o valor de localização de um hub de notificação chamado ContosoNotificationHub para Oeste EUA.

## EXEMPLOS

### Exemplo 1: modificar os valores de propriedade de um hub de notificação
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

Esse comando modifica os valores de propriedade para um hub de notificação encontrado no namespace ContosoNamespace e os atribui à ContosoNotificationsGroup do grupo de recursos.
Os valores de propriedade, bem como o nome do hub a ser modificado, não são especificados no comando.
Em vez disso, essas informações estão contidas no arquivo de entrada C:\Configuration\Hubs.js.

### Exemplo 2

Define valores de propriedade para um hub de notificação. (gerado automaticamente)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

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

### -Force
Não peça confirmação.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
Especifica o caminho para um arquivo JSON que contém informações de configuração para o Hub de notificação.

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

### -NotificationHubObj
Especifica o objeto **NotificationHubAttributes** que contém as informações de configuração para o Hub que esse cmdlet modifica.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)


