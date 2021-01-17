---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433311"
---
# Get-AzDeviceSecurityGroup

## Sinopse
Obter grupo de segurança de dispositivo (segurança de Hub IoT)

## SYNTAX

### ResourceIdScope (padrão)
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdLevelResource
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzDeviceSecurityGroup retorna um grupo de segurança de dispositivo definido na solução de segurança IOT

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

Obter o grupo de segurança do dispositivo "mysecurity Group" no Hub IoT com ID reasource "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"

### Exemplo 2
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

Obter a lista de grupos de segurança de dispositivos no Hub IoT com ID de reasource "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -HubResourceId
ID do recurso de segurança no qual você deseja invocar o comando.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do recurso.

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup

## INFORMA

## LINKS RELACIONADOS
