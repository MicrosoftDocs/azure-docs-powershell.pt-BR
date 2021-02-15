---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118862"
---
# <span data-ttu-id="e5eea-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="e5eea-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="e5eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5eea-102">SYNOPSIS</span></span>
<span data-ttu-id="e5eea-103">Exclui o conjunto de dados de referência com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="e5eea-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e5eea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5eea-104">SYNTAX</span></span>

### <span data-ttu-id="e5eea-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5eea-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5eea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5eea-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5eea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5eea-107">DESCRIPTION</span></span>
<span data-ttu-id="e5eea-108">Exclui o conjunto de dados de referência com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="e5eea-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e5eea-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5eea-109">EXAMPLES</span></span>

### <span data-ttu-id="e5eea-110">Exemplo 1: remover um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="e5eea-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="e5eea-111">Esse comando remove um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="e5eea-112">Exemplo 2: Remover um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="e5eea-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="e5eea-113">Esse comando remove um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="e5eea-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5eea-114">PARAMETERS</span></span>

### <span data-ttu-id="e5eea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5eea-115">-DefaultProfile</span></span>
<span data-ttu-id="e5eea-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5eea-117">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="e5eea-117">-EnvironmentName</span></span>
<span data-ttu-id="e5eea-118">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5eea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5eea-119">-InputObject</span></span>
<span data-ttu-id="e5eea-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e5eea-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5eea-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5eea-121">-Name</span></span>
<span data-ttu-id="e5eea-122">O nome do conjunto de dados de referência insights de série de tempo associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5eea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5eea-123">-PassThru</span></span>
<span data-ttu-id="e5eea-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e5eea-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e5eea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5eea-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5eea-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eea-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5eea-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5eea-127">-SubscriptionId</span></span>
<span data-ttu-id="e5eea-128">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eea-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5eea-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e5eea-129">-Confirm</span></span>
<span data-ttu-id="e5eea-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5eea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5eea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5eea-131">-WhatIf</span></span>
<span data-ttu-id="e5eea-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5eea-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5eea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5eea-134">CommonParameters</span></span>
<span data-ttu-id="e5eea-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5eea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5eea-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5eea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5eea-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5eea-137">INPUTS</span></span>

### <span data-ttu-id="e5eea-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e5eea-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e5eea-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5eea-139">OUTPUTS</span></span>

### <span data-ttu-id="e5eea-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5eea-140">System.Boolean</span></span>

## <span data-ttu-id="e5eea-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e5eea-141">NOTES</span></span>

<span data-ttu-id="e5eea-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="e5eea-142">ALIASES</span></span>

<span data-ttu-id="e5eea-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="e5eea-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5eea-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e5eea-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5eea-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5eea-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5eea-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="e5eea-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5eea-147">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="e5eea-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e5eea-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="e5eea-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e5eea-149">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e5eea-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e5eea-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="e5eea-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5eea-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e5eea-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e5eea-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eea-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e5eea-153">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5eea-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e5eea-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5eea-154">RELATED LINKS</span></span>

