---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112366"
---
# <span data-ttu-id="0e63f-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="0e63f-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="0e63f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e63f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e63f-103">Exclui a fonte de eventos com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="0e63f-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="0e63f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e63f-104">SYNTAX</span></span>

### <span data-ttu-id="0e63f-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e63f-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0e63f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e63f-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e63f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e63f-107">DESCRIPTION</span></span>
<span data-ttu-id="0e63f-108">Exclui a fonte de eventos com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente</span><span class="sxs-lookup"><span data-stu-id="0e63f-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="0e63f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e63f-109">EXAMPLES</span></span>

### <span data-ttu-id="0e63f-110">Exemplo 1: remover uma fonte de evento especificada por nome</span><span class="sxs-lookup"><span data-stu-id="0e63f-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="0e63f-111">Isso remove uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="0e63f-111">This removes a specific event source.</span></span>

### <span data-ttu-id="0e63f-112">Exemplo 2: Remover uma fonte de evento especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="0e63f-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="0e63f-113">Isso remove uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="0e63f-113">This removes a specific event source.</span></span>

## <span data-ttu-id="0e63f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e63f-114">PARAMETERS</span></span>

### <span data-ttu-id="0e63f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e63f-115">-DefaultProfile</span></span>
<span data-ttu-id="0e63f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e63f-117">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="0e63f-117">-EnvironmentName</span></span>
<span data-ttu-id="0e63f-118">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="0e63f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0e63f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e63f-119">-InputObject</span></span>
<span data-ttu-id="0e63f-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0e63f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e63f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e63f-121">-Name</span></span>
<span data-ttu-id="0e63f-122">O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="0e63f-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="0e63f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e63f-123">-PassThru</span></span>
<span data-ttu-id="0e63f-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="0e63f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0e63f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e63f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e63f-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0e63f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e63f-127">-SubscriptionId</span></span>
<span data-ttu-id="0e63f-128">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63f-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0e63f-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0e63f-129">-Confirm</span></span>
<span data-ttu-id="0e63f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e63f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e63f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e63f-131">-WhatIf</span></span>
<span data-ttu-id="0e63f-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0e63f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e63f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e63f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e63f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e63f-134">CommonParameters</span></span>
<span data-ttu-id="0e63f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e63f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e63f-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e63f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e63f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e63f-137">INPUTS</span></span>

### <span data-ttu-id="0e63f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0e63f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0e63f-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e63f-139">OUTPUTS</span></span>

### <span data-ttu-id="0e63f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e63f-140">System.Boolean</span></span>

## <span data-ttu-id="0e63f-141">Notas</span><span class="sxs-lookup"><span data-stu-id="0e63f-141">NOTES</span></span>

<span data-ttu-id="0e63f-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="0e63f-142">ALIASES</span></span>

<span data-ttu-id="0e63f-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0e63f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e63f-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0e63f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e63f-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e63f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e63f-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0e63f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e63f-147">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="0e63f-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0e63f-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="0e63f-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0e63f-149">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="0e63f-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0e63f-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0e63f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e63f-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="0e63f-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0e63f-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63f-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0e63f-153">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e63f-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0e63f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e63f-154">RELATED LINKS</span></span>

