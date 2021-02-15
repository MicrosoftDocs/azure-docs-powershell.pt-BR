---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111869"
---
# Remove-AzFunctionAppPlan

## Sinopse
Exclui um plano de aplicativo de função.

## Sintaxe

### ByName (Default)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
Exclui um plano de aplicativo de função.

## Exemplos

### Exemplo 1: Obter um plano de aplicativo de função por nome e excluí-lo.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Esse comando obtém um plano de aplicativo de função por nome e o exclui.

### Exemplo 2: Excluir um plano de aplicativo de função por nome.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Esse comando exclui um plano de aplicativo de função por nome.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Forçar
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

### -Nome
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
Retorna verdadeiro quando o comando é bem-sucedido.

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

### System.Boolean

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

