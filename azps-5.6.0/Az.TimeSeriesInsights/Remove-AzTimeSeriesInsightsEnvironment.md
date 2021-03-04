---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886808"
---
# <span data-ttu-id="25e77-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="25e77-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="25e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e77-102">SYNOPSIS</span></span>
<span data-ttu-id="25e77-103">Exclui o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="25e77-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="25e77-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="25e77-104">SYNTAX</span></span>

### <span data-ttu-id="25e77-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25e77-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25e77-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25e77-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25e77-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="25e77-107">DESCRIPTION</span></span>
<span data-ttu-id="25e77-108">Exclui o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="25e77-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="25e77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25e77-109">EXAMPLES</span></span>

### <span data-ttu-id="25e77-110">Exemplo 1: Remover um ambiente de insights de série de tempo pelo nome</span><span class="sxs-lookup"><span data-stu-id="25e77-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="25e77-111">Este comando remove um ambiente de insights de séries de tempo.</span><span class="sxs-lookup"><span data-stu-id="25e77-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="25e77-112">Exemplo 2: Remover um ambiente de insights de série de tempo por objeto</span><span class="sxs-lookup"><span data-stu-id="25e77-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="25e77-113">Este comando remove um ambiente de insights de séries de tempo.</span><span class="sxs-lookup"><span data-stu-id="25e77-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="25e77-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="25e77-114">PARAMETERS</span></span>

### <span data-ttu-id="25e77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e77-115">-DefaultProfile</span></span>
<span data-ttu-id="25e77-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25e77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e77-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e77-117">-InputObject</span></span>
<span data-ttu-id="25e77-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="25e77-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25e77-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25e77-119">-Name</span></span>
<span data-ttu-id="25e77-120">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="25e77-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e77-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e77-121">-PassThru</span></span>
<span data-ttu-id="25e77-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="25e77-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25e77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e77-123">-ResourceGroupName</span></span>
<span data-ttu-id="25e77-124">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="25e77-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="25e77-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25e77-125">-SubscriptionId</span></span>
<span data-ttu-id="25e77-126">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="25e77-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="25e77-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e77-127">-Confirm</span></span>
<span data-ttu-id="25e77-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e77-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e77-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e77-129">-WhatIf</span></span>
<span data-ttu-id="25e77-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25e77-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e77-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25e77-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e77-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e77-132">CommonParameters</span></span>
<span data-ttu-id="25e77-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e77-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e77-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25e77-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e77-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25e77-135">INPUTS</span></span>

### <span data-ttu-id="25e77-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="25e77-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="25e77-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="25e77-137">OUTPUTS</span></span>

### <span data-ttu-id="25e77-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25e77-138">System.Boolean</span></span>

## <span data-ttu-id="25e77-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="25e77-139">NOTES</span></span>

<span data-ttu-id="25e77-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25e77-140">ALIASES</span></span>

<span data-ttu-id="25e77-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="25e77-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25e77-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="25e77-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25e77-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25e77-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25e77-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="25e77-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25e77-145">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="25e77-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="25e77-146">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="25e77-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="25e77-147">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="25e77-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="25e77-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="25e77-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25e77-149">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="25e77-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="25e77-150">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="25e77-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="25e77-151">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="25e77-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="25e77-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25e77-152">RELATED LINKS</span></span>

