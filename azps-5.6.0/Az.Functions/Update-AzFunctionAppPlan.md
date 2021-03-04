---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886766"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Atualiza um plano de serviço de aplicativo de função.

## SINTAXE

### ByName (Padrão)
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

## DESCRIPTION
Atualiza um plano de serviço de aplicativo de função.

## EXEMPLOS

### Exemplo 1: atualizar um plano de serviço de aplicativo para sku EP2 com vinte funcionários máximos.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Este comando atualiza um plano de serviço de aplicativo para sku EP2 com vinte funcionários máximos.

## PARÂMETROS

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
Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

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
O número máximo de funcionários para o plano de serviço de aplicativo.

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
O número mínimo de funcionários para o plano de serviço de aplicativo.

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

### -Name
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
Execute o comando de forma assíncrona.

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

### -Sku
O plano sku.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Localização do Recurso.
  - `[Kind <String>]`: Tipo de recurso.
  - `[Tag <IResourceTags>]`: Marcas de recurso.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.
  - `[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores expira.
  - `[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.
  - `[HyperV <Boolean?>]`: Se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for, <code>false</code> caso contrário.
  - `[IsSpot <Boolean?>]`: If <code>true</code> , this App Service Plan owns spot instances.
  - `[IsXenon <Boolean?>]`: Obsoleto: se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for , <code>false</code> caso contrário.
  - `[MaximumElasticWorkerCount <Int32?>]`: Número máximo de funcionários permitidos para este Plano de Serviço de Aplicativo ElasticScaleEnabled
  - `[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo podem ser dimensionados independentemente.         Se <code>false</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo serão dimensionados para todas as instâncias do plano.
  - `[Reserved <Boolean?>]`: Se o plano de serviço do aplicativo <code>true</code> Linux, <code>false</code> caso contrário.
  - `[SkuCapability <ICapability[]>]`: Os recursos do SKU, por exemplo, estão habilitados para o gerenciador de tráfego?
    - `[Name <String>]`: Nome da funcionalidade SKU.
    - `[Reason <String>]`: Motivo da funcionalidade SKU.
    - `[Value <String>]`: Valor da funcionalidade SKU.
  - `[SkuCapacityDefault <Int32?>]`: Número padrão de funcionários para este SKU do plano de Serviço de Aplicativo.
  - `[SkuCapacityMaximum <Int32?>]`: Número máximo de funcionários para este SKU do plano de Serviço de Aplicativo.
  - `[SkuCapacityMinimum <Int32?>]`: Número mínimo de funcionários para este SKU do plano de Serviço de Aplicativo.
  - `[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano de Serviço de Aplicativo.
  - `[SkuFamily <String>]`: Código da família do SKU do recurso.
  - `[SkuLocation <String[]>]`: Locais do SKU.
  - `[SkuName <String>]`: Nome da SKU do recurso.
  - `[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.
  - `[SkuTier <String>]`: Camada de serviço do SKU do recurso.
  - `[SpotExpirationTime <DateTime?>]`: A hora em que o farm de servidores expira. Válido somente se for um farm de servidores spot.
  - `[TargetWorkerCount <Int32?>]`: Escala de contagem de funcionários.
  - `[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do tamanho do trabalho.
  - `[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano de Serviço de Aplicativo.

## LINKS RELACIONADOS

