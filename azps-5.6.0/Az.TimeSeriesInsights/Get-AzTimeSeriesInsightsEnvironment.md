---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893046"
---
# Get-AzTimeSeriesInsightsEnvironment

## SYNOPSIS
Obtém o ambiente com o nome especificado no grupo de recursos e assinatura especificado.

## SINTAXE

### List1 (Padrão)
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Obter
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Listar
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Obtém o ambiente com o nome especificado no grupo de recursos e assinatura especificado.

## EXEMPLOS

### Exemplo 1: Obter um ambiente de insights de séries de tempo
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

Este comando obtém um ambiente de insights de séries de tempo.

### Exemplo 2: listar todos os ambientes de insights de séries de tempo
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

Este comando lista todos os ambientes de insights de séries de tempo em um grupo de recursos.

### Exemplo 3: Obter um ambiente de insights de série de tempo por objeto
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

Este comando obtém ambientes de insights de séries de tempo.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expand
A configuração $expand=status incluirá o status dos serviços internos do ambiente no serviço Insights da Série de Tempo.

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome de um grupo de Recursos do Azure.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID da Assinatura do Azure.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity
  - `[AccessPolicyName <String>]`: Nome da política de acesso.
  - `[EnvironmentName <String>]`: Nome do ambiente
  - `[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.
  - `[Id <String>]`: Caminho da identidade do recurso
  - `[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.
  - `[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.
  - `[SubscriptionId <String>]`: ID da Assinatura do Azure.

## LINKS RELACIONADOS

