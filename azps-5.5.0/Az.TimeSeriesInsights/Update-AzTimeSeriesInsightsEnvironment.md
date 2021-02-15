---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118860"
---
# <span data-ttu-id="9e1d2-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="9e1d2-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="9e1d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1d2-103">Atualiza o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="9e1d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e1d2-104">SYNTAX</span></span>

### <span data-ttu-id="9e1d2-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e1d2-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e1d2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e1d2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e1d2-107">DESCRIPTION</span></span>
<span data-ttu-id="9e1d2-108">Atualiza o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="9e1d2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e1d2-109">EXAMPLES</span></span>

### <span data-ttu-id="9e1d2-110">Exemplo 1: Atualizar um ambiente de insights de séries temporizais gen1</span><span class="sxs-lookup"><span data-stu-id="9e1d2-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="9e1d2-111">Este comando atualiza um ambiente de insights de séries temporizais gen1.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="9e1d2-112">Exemplo 2: Atualizar um ambiente de insights de séries temporizais gen1</span><span class="sxs-lookup"><span data-stu-id="9e1d2-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="9e1d2-113">Este comando atualiza um ambiente de insights de séries temporizais gen1.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="9e1d2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e1d2-114">PARAMETERS</span></span>

### <span data-ttu-id="9e1d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e1d2-115">-AsJob</span></span>
<span data-ttu-id="9e1d2-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9e1d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9e1d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1d2-117">-DefaultProfile</span></span>
<span data-ttu-id="9e1d2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e1d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e1d2-119">-InputObject</span></span>
<span data-ttu-id="9e1d2-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e1d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e1d2-121">-Name</span></span>
<span data-ttu-id="9e1d2-122">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1d2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9e1d2-123">-NoWait</span></span>
<span data-ttu-id="9e1d2-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="9e1d2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9e1d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e1d2-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="9e1d2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-127">-SubscriptionId</span></span>
<span data-ttu-id="9e1d2-128">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9e1d2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e1d2-129">-Tag</span></span>
<span data-ttu-id="9e1d2-130">Pares de valores-chave de propriedades adicionais para o ambiente.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="9e1d2-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9e1d2-131">-Confirm</span></span>
<span data-ttu-id="9e1d2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e1d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e1d2-133">-WhatIf</span></span>
<span data-ttu-id="9e1d2-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e1d2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e1d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1d2-136">CommonParameters</span></span>
<span data-ttu-id="9e1d2-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1d2-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e1d2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1d2-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="9e1d2-139">INPUTS</span></span>

### <span data-ttu-id="9e1d2-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="9e1d2-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="9e1d2-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="9e1d2-141">OUTPUTS</span></span>

### <span data-ttu-id="9e1d2-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="9e1d2-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="9e1d2-143">Notas</span><span class="sxs-lookup"><span data-stu-id="9e1d2-143">NOTES</span></span>

<span data-ttu-id="9e1d2-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="9e1d2-144">ALIASES</span></span>

<span data-ttu-id="9e1d2-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="9e1d2-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e1d2-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e1d2-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e1d2-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="9e1d2-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e1d2-149">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="9e1d2-150">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="9e1d2-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="9e1d2-151">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="9e1d2-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="9e1d2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e1d2-153">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="9e1d2-154">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="9e1d2-155">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9e1d2-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e1d2-156">RELATED LINKS</span></span>

