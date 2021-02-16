---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118521"
---
# <span data-ttu-id="64da1-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="64da1-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="64da1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64da1-102">SYNOPSIS</span></span>
<span data-ttu-id="64da1-103">Atualiza o conjunto de dados de referência com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="64da1-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="64da1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64da1-104">SYNTAX</span></span>

### <span data-ttu-id="64da1-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="64da1-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64da1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64da1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64da1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="64da1-107">DESCRIPTION</span></span>
<span data-ttu-id="64da1-108">Atualiza o conjunto de dados de referência com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="64da1-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="64da1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64da1-109">EXAMPLES</span></span>

### <span data-ttu-id="64da1-110">Exemplo 1: Atualizar um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="64da1-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="64da1-111">Esse comando atualiza um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="64da1-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="64da1-112">Exemplo 2: Atualizar um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="64da1-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="64da1-113">Esse comando atualiza um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="64da1-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="64da1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64da1-114">PARAMETERS</span></span>

### <span data-ttu-id="64da1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64da1-115">-DefaultProfile</span></span>
<span data-ttu-id="64da1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64da1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64da1-117">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="64da1-117">-EnvironmentName</span></span>
<span data-ttu-id="64da1-118">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="64da1-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="64da1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64da1-119">-InputObject</span></span>
<span data-ttu-id="64da1-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="64da1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64da1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="64da1-121">-Name</span></span>
<span data-ttu-id="64da1-122">O nome do conjunto de dados de referência insights de série de tempo associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="64da1-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="64da1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64da1-123">-ResourceGroupName</span></span>
<span data-ttu-id="64da1-124">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da1-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="64da1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64da1-125">-SubscriptionId</span></span>
<span data-ttu-id="64da1-126">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da1-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="64da1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="64da1-127">-Tag</span></span>
<span data-ttu-id="64da1-128">Pares de valor-chave de propriedades adicionais para o conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="64da1-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="64da1-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="64da1-129">-Confirm</span></span>
<span data-ttu-id="64da1-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64da1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64da1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64da1-131">-WhatIf</span></span>
<span data-ttu-id="64da1-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="64da1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64da1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64da1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64da1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64da1-134">CommonParameters</span></span>
<span data-ttu-id="64da1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64da1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64da1-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64da1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64da1-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="64da1-137">INPUTS</span></span>

### <span data-ttu-id="64da1-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="64da1-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="64da1-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="64da1-139">OUTPUTS</span></span>

### <span data-ttu-id="64da1-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="64da1-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="64da1-141">Notas</span><span class="sxs-lookup"><span data-stu-id="64da1-141">NOTES</span></span>

<span data-ttu-id="64da1-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="64da1-142">ALIASES</span></span>

<span data-ttu-id="64da1-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="64da1-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64da1-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="64da1-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64da1-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64da1-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64da1-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="64da1-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64da1-147">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="64da1-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="64da1-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="64da1-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="64da1-149">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="64da1-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="64da1-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="64da1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64da1-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="64da1-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="64da1-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da1-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="64da1-153">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="64da1-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="64da1-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64da1-154">RELATED LINKS</span></span>

