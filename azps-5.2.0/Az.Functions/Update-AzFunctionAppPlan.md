---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260252"
---
# Update-AzFunctionAppPlan

## Sinopse
Atualiza um plano do serviço de aplicativo função.

## SYNTAX

### ByName (padrão)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Atualiza um plano do serviço de aplicativo função.

## EXEMPLOS

### Exemplo 1: atualizar um plano de serviço de aplicativo para EP2 SKU com vinte funcionários máximos.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Esse comando atualiza um plano do serviço de aplicativo para EP2 SKU com vinte trabalhadores máximos.

## OS

### -AsJob
Executar o comando como um trabalho.

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

### -DefaultProfile


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

### -InputObject
Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
O número máximo de trabalhadores para o plano do serviço de aplicativo.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
O número mínimo de trabalhadores para o plano do serviço de aplicativo.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do plano do serviço de aplicativo.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Executar o comando de forma assíncrona.

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

### -ResourceGroupName
Nome do grupo de recursos ao qual o recurso pertence.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
A SKU do plano.
As entradas válidas são: EP1, EP2, EP3

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura do Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Marcas de recurso.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <IAppServicePlan> : 
  - `Location <String>`: Local do recurso.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas do recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.
  - `[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores vence.
  - `[HostingEnvironmentProfileId <String>]`: ID do recurso do ambiente do serviço de aplicativo.
  - `[HyperV <Boolean?>]`: Se o plano do serviço de aplicativo contêiner Hyper-V <code>true</code> , <code>false</code> caso contrário.
  - `[IsSpot <Boolean?>]`: Se <code>true</code> , esse plano do serviço de aplicativo possui instâncias especiais.
  - `[IsXenon <Boolean?>]`: Obsoleto: se o plano do serviço de aplicativo contêiner do Hyper-V <code>true</code> , <code>false</code> caso contrário.
  - `[MaximumElasticWorkerCount <Int32?>]`: Número máximo do total de trabalhadores permitidos para este plano do serviço de aplicativo ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo poderão ser dimensionados independentemente.         Se <code>false</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo serão dimensionados para todas as instâncias do plano.
  - `[Reserved <Boolean?>]`: Se for o plano do serviço de aplicativo Linux <code>true</code> , <code>false</code> caso contrário.
  - `[SkuCapability <ICapability[]>]`: Recursos do SKU, por exemplo, o Gerenciador de tráfego está habilitado?
    - `[Name <String>]`: Nome do recurso de SKU.
    - `[Reason <String>]`: Motivo da funcionalidade de SKU.
    - `[Value <String>]`: Valor da funcionalidade de SKU.
  - `[SkuCapacityDefault <Int32?>]`: Número padrão de trabalhadores para esta SKU do plano do serviço de aplicativo.
  - `[SkuCapacityMaximum <Int32?>]`: Número máximo de trabalhadores para esta SKU do plano do serviço de aplicativo.
  - `[SkuCapacityMinimum <Int32?>]`: Número mínimo de trabalhadores para esta SKU do plano do serviço de aplicativo.
  - `[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano do serviço de aplicativo.
  - `[SkuFamily <String>]`: Código da família do SKU do recurso.
  - `[SkuLocation <String[]>]`: Locais da SKU.
  - `[SkuName <String>]`: Nome do SKU do recurso.
  - `[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.
  - `[SkuTier <String>]`: Camada de serviço do SKU do recurso.
  - `[SpotExpirationTime <DateTime?>]`: O tempo em que o farm de servidores vence. Válido somente se for um farm de servidores Spot.
  - `[TargetWorkerCount <Int32?>]`: Dimensionando a contagem de trabalhadores.
  - `[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do valor do trabalhador.
  - `[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano do serviço de aplicativo.

## LINKS RELACIONADOS

