---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 956e7a1a2fd0917dd3b647ef547eec165c1cd5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889867"
---
# <span data-ttu-id="a2df3-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a2df3-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a2df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2df3-102">SYNOPSIS</span></span>
<span data-ttu-id="a2df3-103">Atualiza o conjunto de dados de referência com o nome especificado na assinatura especificada, grupo de recursos e ambiente.</span><span class="sxs-lookup"><span data-stu-id="a2df3-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a2df3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a2df3-104">SYNTAX</span></span>

### <span data-ttu-id="a2df3-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a2df3-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2df3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a2df3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2df3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a2df3-107">DESCRIPTION</span></span>
<span data-ttu-id="a2df3-108">Atualiza o conjunto de dados de referência com o nome especificado na assinatura especificada, grupo de recursos e ambiente.</span><span class="sxs-lookup"><span data-stu-id="a2df3-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a2df3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2df3-109">EXAMPLES</span></span>

### <span data-ttu-id="a2df3-110">Exemplo 1: Atualizar um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="a2df3-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a2df3-111">Este comando atualiza um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="a2df3-112">Exemplo 2: Atualizar um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="a2df3-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a2df3-113">Este comando atualiza um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="a2df3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a2df3-114">PARAMETERS</span></span>

### <span data-ttu-id="a2df3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2df3-115">-DefaultProfile</span></span>
<span data-ttu-id="a2df3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2df3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2df3-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a2df3-117">-EnvironmentName</span></span>
<span data-ttu-id="a2df3-118">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2df3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2df3-119">-InputObject</span></span>
<span data-ttu-id="a2df3-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a2df3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2df3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2df3-121">-Name</span></span>
<span data-ttu-id="a2df3-122">O nome do conjunto de dados de referência do Insights da Série de Tempo associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2df3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2df3-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2df3-124">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2df3-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2df3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2df3-125">-SubscriptionId</span></span>
<span data-ttu-id="a2df3-126">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2df3-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2df3-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2df3-127">-Tag</span></span>
<span data-ttu-id="a2df3-128">Pares de valores-chave de propriedades adicionais para o conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="a2df3-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="a2df3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2df3-129">-Confirm</span></span>
<span data-ttu-id="a2df3-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2df3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2df3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2df3-131">-WhatIf</span></span>
<span data-ttu-id="a2df3-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2df3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2df3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2df3-134">CommonParameters</span></span>
<span data-ttu-id="a2df3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2df3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2df3-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2df3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2df3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2df3-137">INPUTS</span></span>

### <span data-ttu-id="a2df3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a2df3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a2df3-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a2df3-139">OUTPUTS</span></span>

### <span data-ttu-id="a2df3-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="a2df3-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="a2df3-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="a2df3-141">NOTES</span></span>

<span data-ttu-id="a2df3-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a2df3-142">ALIASES</span></span>

<span data-ttu-id="a2df3-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a2df3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2df3-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a2df3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2df3-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2df3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2df3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a2df3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2df3-147">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="a2df3-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a2df3-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="a2df3-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a2df3-149">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="a2df3-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a2df3-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a2df3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2df3-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="a2df3-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a2df3-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2df3-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a2df3-153">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2df3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a2df3-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2df3-154">RELATED LINKS</span></span>

