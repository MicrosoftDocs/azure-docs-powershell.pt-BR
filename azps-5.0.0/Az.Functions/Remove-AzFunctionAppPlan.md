---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115417"
---
# Remove-AzFunctionAppPlan

## Sinopse
Exclui um plano de aplicativo de função.

## SYNTAX

### ByName (padrão)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Exclui um plano de aplicativo de função.

## EXEMPLOS

### Exemplo 1: obter uma função plano do aplicativo por nome e excluí-lo.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Esse comando obtém uma função plano do aplicativo por nome e a exclui.

### Exemplo 2: excluir uma função de plano do aplicativo por nome.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Esse comando exclui um plano de aplicativo de função por nome.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Force
Força o cmdlet a remover o plano de aplicativo da função sem solicitar confirmação.

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

### -Nome
O nome da função do aplicativo.

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

### -PassThru
Retorna true quando o comando é bem-sucedido.

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

### System. Boolean

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

