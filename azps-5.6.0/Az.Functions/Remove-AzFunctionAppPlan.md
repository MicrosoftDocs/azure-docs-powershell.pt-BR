---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890841"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
Exclui um plano de aplicativo de função.

## SINTAXE

### ByName (Padrão)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Exclui um plano de aplicativo de função.

## EXEMPLOS

### Exemplo 1: Obter um plano de aplicativo de função pelo nome e excluí-lo.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Esse comando obtém um plano de aplicativo de função por nome e o exclui.

### Exemplo 2: Excluir um plano de aplicativo de função por nome.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Este comando exclui um plano de aplicativo de função por nome.

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

### -Force
Força o cmdlet a remover o plano do aplicativo de função sem solicitar confirmação.

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

### -Name
O nome do aplicativo de função.

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

### System.Boolean

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

