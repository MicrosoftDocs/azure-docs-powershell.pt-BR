---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433674"
---
# Get-AzIotCentralApp

## Sinopse
Obtém Propriedades para um ou vários aplicativos centrais do IoT.

## SYNTAX

### ListIotCentralAppsParameterSet (padrão)
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

## DESCRITIVO
Obtém os metadados de um aplicativo Central de IoT específico ou todos os aplicativos em um grupo de recursos ou assinatura, dependendo do conjunto de parâmetros. 

## EXEMPLOS

### Exemplo 1 obter aplicativo da central de IoT específico.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Obtém os metadados do aplicativo da central de IoT especificado.

Exemplo de saída:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Nome do IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: {[chave, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

### Exemplo 2 obter aplicativos centrais do IoT na assinatura.
```powershell
PS C:\> Get-AzIotCentralApp
```

Obtém os metadados de todos os aplicativos centrais da IoT na assinatura atual.

Exemplo de saída:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Nome do IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: {[chave, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. Nome do IoTCentral/IoTApps/MyAppResourceName2: MyAppResourceName2 tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: {[chave, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado 2 subdomínio: MyAppSubdomain2 modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2

### Exemplo 3 obter aplicativos da central de IoT no grupo de recursos.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Obtém os metadados de todos os aplicativos centrais do IoT no grupo de recursos fornecido.

Exemplo de saída:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Nome do IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: {[chave, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado subdomínio: MyAppSubdomain modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Nome do IoTCentral/IoTApps/MyAppResourceName2: MyAppResourceName2 tipo: Microsoft. IoTCentral/IoTApps Location: marca westus: {[chave, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: meu nome de exibição personalizado 2 subdomínio: MyAppSubdomain2 modelo: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

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

### -Nome
Nome do recurso de aplicativo da central do IOT.

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
Nome do grupo de recursos.

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
ID do recurso de aplicativo do IOT central.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp

## INFORMA

## LINKS RELACIONADOS
