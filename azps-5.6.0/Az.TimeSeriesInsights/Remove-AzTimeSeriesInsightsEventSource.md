---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 9dcce9640500b1fa1aeebea8f5f3169e0a527b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890503"
---
# <span data-ttu-id="c12e4-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="c12e4-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="c12e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c12e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c12e4-103">Exclui a fonte de eventos com o nome especificado na assinatura especificada, grupo de recursos e ambiente</span><span class="sxs-lookup"><span data-stu-id="c12e4-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="c12e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c12e4-104">SYNTAX</span></span>

### <span data-ttu-id="c12e4-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c12e4-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c12e4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c12e4-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c12e4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c12e4-107">DESCRIPTION</span></span>
<span data-ttu-id="c12e4-108">Exclui a fonte de eventos com o nome especificado na assinatura especificada, grupo de recursos e ambiente</span><span class="sxs-lookup"><span data-stu-id="c12e4-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="c12e4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c12e4-109">EXAMPLES</span></span>

### <span data-ttu-id="c12e4-110">Exemplo 1: Remover uma fonte de eventos especificada pelo nome</span><span class="sxs-lookup"><span data-stu-id="c12e4-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="c12e4-111">Isso remove uma fonte de eventos específica.</span><span class="sxs-lookup"><span data-stu-id="c12e4-111">This removes a specific event source.</span></span>

### <span data-ttu-id="c12e4-112">Exemplo 2: Remover uma fonte de eventos especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="c12e4-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="c12e4-113">Isso remove uma fonte de eventos específica.</span><span class="sxs-lookup"><span data-stu-id="c12e4-113">This removes a specific event source.</span></span>

## <span data-ttu-id="c12e4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c12e4-114">PARAMETERS</span></span>

### <span data-ttu-id="c12e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12e4-115">-DefaultProfile</span></span>
<span data-ttu-id="c12e4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c12e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c12e4-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c12e4-117">-EnvironmentName</span></span>
<span data-ttu-id="c12e4-118">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c12e4-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c12e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c12e4-119">-InputObject</span></span>
<span data-ttu-id="c12e4-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c12e4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c12e4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c12e4-121">-Name</span></span>
<span data-ttu-id="c12e4-122">O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c12e4-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c12e4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c12e4-123">-PassThru</span></span>
<span data-ttu-id="c12e4-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c12e4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c12e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c12e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="c12e4-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c12e4-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c12e4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c12e4-127">-SubscriptionId</span></span>
<span data-ttu-id="c12e4-128">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c12e4-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c12e4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c12e4-129">-Confirm</span></span>
<span data-ttu-id="c12e4-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c12e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12e4-131">-WhatIf</span></span>
<span data-ttu-id="c12e4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c12e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c12e4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c12e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12e4-134">CommonParameters</span></span>
<span data-ttu-id="c12e4-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12e4-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c12e4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12e4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c12e4-137">INPUTS</span></span>

### <span data-ttu-id="c12e4-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="c12e4-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="c12e4-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c12e4-139">OUTPUTS</span></span>

### <span data-ttu-id="c12e4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c12e4-140">System.Boolean</span></span>

## <span data-ttu-id="c12e4-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="c12e4-141">NOTES</span></span>

<span data-ttu-id="c12e4-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c12e4-142">ALIASES</span></span>

<span data-ttu-id="c12e4-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="c12e4-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c12e4-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c12e4-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c12e4-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c12e4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c12e4-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="c12e4-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c12e4-147">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="c12e4-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="c12e4-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="c12e4-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="c12e4-149">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c12e4-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="c12e4-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c12e4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c12e4-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="c12e4-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="c12e4-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c12e4-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="c12e4-153">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c12e4-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c12e4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c12e4-154">RELATED LINKS</span></span>

