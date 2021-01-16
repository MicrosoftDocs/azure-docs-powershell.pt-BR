---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259201"
---
# <span data-ttu-id="14f44-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="14f44-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="14f44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14f44-102">SYNOPSIS</span></span>
<span data-ttu-id="14f44-103">Exclui a fonte de evento com o nome especificado na assinatura especificada, grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="14f44-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="14f44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14f44-104">SYNTAX</span></span>

### <span data-ttu-id="14f44-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="14f44-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14f44-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14f44-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14f44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14f44-107">DESCRIPTION</span></span>
<span data-ttu-id="14f44-108">Exclui a fonte de evento com o nome especificado na assinatura especificada, grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="14f44-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="14f44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14f44-109">EXAMPLES</span></span>

### <span data-ttu-id="14f44-110">Exemplo 1: remover uma fonte de evento especificada por nome</span><span class="sxs-lookup"><span data-stu-id="14f44-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="14f44-111">Isso remove uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="14f44-111">This removes a specific event source.</span></span>

### <span data-ttu-id="14f44-112">Exemplo 2: remover uma fonte de evento especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="14f44-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="14f44-113">Isso remove uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="14f44-113">This removes a specific event source.</span></span>

## <span data-ttu-id="14f44-114">OS</span><span class="sxs-lookup"><span data-stu-id="14f44-114">PARAMETERS</span></span>

### <span data-ttu-id="14f44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f44-115">-DefaultProfile</span></span>
<span data-ttu-id="14f44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14f44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f44-117">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="14f44-117">-EnvironmentName</span></span>
<span data-ttu-id="14f44-118">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="14f44-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="14f44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14f44-119">-InputObject</span></span>
<span data-ttu-id="14f44-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="14f44-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14f44-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="14f44-121">-Name</span></span>
<span data-ttu-id="14f44-122">O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="14f44-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="14f44-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14f44-123">-PassThru</span></span>
<span data-ttu-id="14f44-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="14f44-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14f44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f44-125">-ResourceGroupName</span></span>
<span data-ttu-id="14f44-126">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14f44-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="14f44-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14f44-127">-SubscriptionId</span></span>
<span data-ttu-id="14f44-128">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="14f44-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="14f44-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14f44-129">-Confirm</span></span>
<span data-ttu-id="14f44-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14f44-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f44-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f44-131">-WhatIf</span></span>
<span data-ttu-id="14f44-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14f44-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f44-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14f44-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f44-134">CommonParameters</span></span>
<span data-ttu-id="14f44-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f44-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14f44-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f44-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14f44-137">INPUTS</span></span>

### <span data-ttu-id="14f44-138">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="14f44-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="14f44-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14f44-139">OUTPUTS</span></span>

### <span data-ttu-id="14f44-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14f44-140">System.Boolean</span></span>

## <span data-ttu-id="14f44-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14f44-141">NOTES</span></span>

<span data-ttu-id="14f44-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="14f44-142">ALIASES</span></span>

<span data-ttu-id="14f44-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="14f44-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14f44-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="14f44-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14f44-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14f44-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14f44-146">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="14f44-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14f44-147">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="14f44-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="14f44-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="14f44-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="14f44-149">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="14f44-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="14f44-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="14f44-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14f44-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="14f44-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="14f44-152">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="14f44-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="14f44-153">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="14f44-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="14f44-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14f44-154">RELATED LINKS</span></span>

