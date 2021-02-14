---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116787"
---
# Update-AzFunctionAppPlan

## Sinopse
Atualiza um plano de serviço de aplicativo de função.

## Sintaxe

### ByName (Default)
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

## Descrição
Atualiza um plano de serviço de aplicativo de função.

## Exemplos

### Exemplo 1: Atualize um plano de serviço de aplicativo para a SKU DE ACORDO2 com vinte trabalhadores máximos.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Este comando atualiza um plano de serviço de aplicativo para a SKU DE ACORDO2 com vinte trabalhadores máximos.

## Parâmetros

### -AsJob
Execute o comando como um trabalho.

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
Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

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
O número máximo de trabalhadores para o plano de serviço de aplicativo.

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
O número mínimo de trabalhadores para o plano de serviço de aplicativo.

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
Nome do plano serviço de aplicativo.

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

### -NoWait
Execute o comando assíncrona.

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
As entradas válidas são: EP1, EP2, TEM3

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
A ID de assinatura do Azure.

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

### -Tag
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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## Saídas

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppServicePlan> 
  - `Location <String>`: Localização do Recurso.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.
  - `[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.
  - `[FreeOfferExpirationTime <DateTime?>]`: o tempo em que a oferta gratuita de farm do servidor expira.
  - `[HostingEnvironmentProfileId <String>]`: ID do recurso do Ambiente de Serviço de Aplicativos.
  - `[HyperV <Boolean?>]`: caso contrário, se o plano de serviço do aplicativo de contêineres Hiper-V <code>true</code> <code>false</code> for.
  - `[IsSpot <Boolean?>]`: Se <code>true</code> , este Plano de Serviço de Aplicativo possui instâncias de local.
  - `[IsXenon <Boolean?>]`: Obsoleto: se o plano de serviço do aplicativo de contêineres Hiper-V, <code>true</code> <code>false</code> caso contrário.
  - `[MaximumElasticWorkerCount <Int32?>]`: número máximo de trabalhadores totais permitidos para este Plano de Serviço de Aplicativo ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativos podem ser dimensionados independentemente.         Se <code>false</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo serão dimensionados para todas as instâncias do plano.
  - `[Reserved <Boolean?>]`: Se o plano de serviço do aplicativo <code>true</code> Linux, <code>false</code> caso contrário.
  - `[SkuCapability <ICapability[]>]`: Os recursos da SKU, por exemplo, estão habilitados no gerenciador de tráfego?
    - `[Name <String>]`: Nome do recurso SKU.
    - `[Reason <String>]`: motivo da capacidade da SKU.
    - `[Value <String>]`: Valor da capacidade de SKU.
  - `[SkuCapacityDefault <Int32?>]`: Número padrão de trabalhadores para esta SKU do plano serviço de aplicativo.
  - `[SkuCapacityMaximum <Int32?>]`: Número máximo de trabalhadores para esta SKU do plano serviço de aplicativo.
  - `[SkuCapacityMinimum <Int32?>]`: Número mínimo de trabalhadores para esta SKU do plano serviço de aplicativo.
  - `[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano de Serviço de Aplicativo.
  - `[SkuFamily <String>]`: Código da família da SKU do recurso.
  - `[SkuLocation <String[]>]`: locais da SKU.
  - `[SkuName <String>]`: Nome da SKU do recurso.
  - `[SkuSize <String>]`: Especificador de tamanho da SKU do recurso.
  - `[SkuTier <String>]`: Nível de serviço da SKU do recurso.
  - `[SpotExpirationTime <DateTime?>]`: o tempo em que o farm do servidor expira. Válido somente se for um farm de servidor local.
  - `[TargetWorkerCount <Int32?>]`: Dimensionando a contagem de trabalhadores.
  - `[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do tamanho do trabalhador.
  - `[WorkerTierName <String>]`: Nível de trabalhador de destino atribuído ao plano serviço de aplicativos.

## LINKS RELACIONADOS

