---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113149"
---
# <span data-ttu-id="7b644-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="7b644-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="7b644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b644-102">SYNOPSIS</span></span>
<span data-ttu-id="7b644-103">Exclui o ambiente com o nome especificado na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b644-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="7b644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b644-104">SYNTAX</span></span>

### <span data-ttu-id="7b644-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b644-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b644-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7b644-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b644-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b644-107">DESCRIPTION</span></span>
<span data-ttu-id="7b644-108">Exclui o ambiente com o nome especificado na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b644-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="7b644-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b644-109">EXAMPLES</span></span>

### <span data-ttu-id="7b644-110">Exemplo 1: remover um ambiente do insights série de tempo por nome</span><span class="sxs-lookup"><span data-stu-id="7b644-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="7b644-111">Esse comando Remove um ambiente do insights série de tempo.</span><span class="sxs-lookup"><span data-stu-id="7b644-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="7b644-112">Exemplo 2: remover um ambiente do insights série de tempo por objeto</span><span class="sxs-lookup"><span data-stu-id="7b644-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="7b644-113">Esse comando Remove um ambiente do insights série de tempo.</span><span class="sxs-lookup"><span data-stu-id="7b644-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="7b644-114">OS</span><span class="sxs-lookup"><span data-stu-id="7b644-114">PARAMETERS</span></span>

### <span data-ttu-id="7b644-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b644-115">-DefaultProfile</span></span>
<span data-ttu-id="7b644-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b644-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b644-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b644-117">-InputObject</span></span>
<span data-ttu-id="7b644-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7b644-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b644-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b644-119">-Name</span></span>
<span data-ttu-id="7b644-120">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7b644-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7b644-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b644-121">-PassThru</span></span>
<span data-ttu-id="7b644-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7b644-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7b644-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b644-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b644-124">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b644-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7b644-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b644-125">-SubscriptionId</span></span>
<span data-ttu-id="7b644-126">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b644-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7b644-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b644-127">-Confirm</span></span>
<span data-ttu-id="7b644-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b644-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b644-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b644-129">-WhatIf</span></span>
<span data-ttu-id="7b644-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b644-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b644-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b644-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b644-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b644-132">CommonParameters</span></span>
<span data-ttu-id="7b644-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b644-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b644-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b644-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b644-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b644-135">INPUTS</span></span>

### <span data-ttu-id="7b644-136">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="7b644-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="7b644-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b644-137">OUTPUTS</span></span>

### <span data-ttu-id="7b644-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b644-138">System.Boolean</span></span>

## <span data-ttu-id="7b644-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b644-139">NOTES</span></span>

<span data-ttu-id="7b644-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7b644-140">ALIASES</span></span>

<span data-ttu-id="7b644-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="7b644-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b644-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7b644-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b644-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b644-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b644-144">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7b644-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b644-145">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="7b644-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="7b644-146">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="7b644-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="7b644-147">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="7b644-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="7b644-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7b644-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b644-149">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="7b644-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="7b644-150">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b644-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="7b644-151">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b644-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7b644-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b644-152">RELATED LINKS</span></span>

