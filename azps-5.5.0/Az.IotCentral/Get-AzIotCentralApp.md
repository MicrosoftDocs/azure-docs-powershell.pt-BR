---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117615"
---
# Get-AzIotCentralApp

## Sinopse
Obtém propriedades para um ou vários Aplicativos Centrais de IoT.

## Sintaxe

### ListIotCentralAppsParameterSet (Padrão)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
Obtém os metadados de um Aplicativo Central de IoT específico ou todos os aplicativos em um Grupo de Recursos ou Assinatura, dependendo do Conjunto de Parâmetros. 

## Exemplos

### Exemplo 1 Obter Aplicativo Central de IoT específico.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Obtém os metadados do Aplicativo Central de IoT especificado.

Exemplo de saída:

ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

### Exemplo 2 Obter Aplicativos Centrais de IoT em Assinatura.
```powershell
PS C:\> Get-AzIotCentralApp
```

Obtém os metadados de todos os Aplicativos Centrais de IoT na Assinatura atual.

Exemplo de saída:

ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag: {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Meu subdomínio Nome de Exibição Personalizado 2 : Meu Modelo MyAppSubdomain2 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2

### Exemplo 3 Obter Aplicativos Centrais de IoT no Grupo de Recursos.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Obtém os metadados de todos os Aplicativos Centrais de IoT no Grupo de Recursos fornecido.

Exemplo de saída:

ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain iotc-default@1.0.0 Template : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location: westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Meu subdomínio Nome de Exibição Personalizado 2 : Meu Modelo MyAppSubdomain2 : iotc-default@1.0.0 SubscriptionId : XXXXXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Nome
Nome do Recurso de Aplicativo Central de Iot.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do Grupo de Recursos.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Iot Central Application Resource Id.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## Notas

## LINKS RELACIONADOS
