---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117907"
---
# <span data-ttu-id="8a384-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="8a384-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="8a384-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a384-102">SYNOPSIS</span></span>
<span data-ttu-id="8a384-103">Obtém os dados de referência definidos com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8a384-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a384-104">SYNTAX</span></span>

### <span data-ttu-id="8a384-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a384-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a384-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8a384-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a384-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a384-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a384-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a384-108">DESCRIPTION</span></span>
<span data-ttu-id="8a384-109">Obtém os dados de referência definidos com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="8a384-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a384-110">EXAMPLES</span></span>

### <span data-ttu-id="8a384-111">Exemplo 1: listar todos os conjuntos de dados de referência no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="8a384-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a384-112">Esse comando lista todos os conjuntos de dados de referência no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="8a384-113">Exemplo 2: obter um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="8a384-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a384-114">Esse comando obtém um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="8a384-115">Exemplo 3: obter um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="8a384-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8a384-116">Esse comando obtém um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="8a384-117">OS</span><span class="sxs-lookup"><span data-stu-id="8a384-117">PARAMETERS</span></span>

### <span data-ttu-id="8a384-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a384-118">-DefaultProfile</span></span>
<span data-ttu-id="8a384-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a384-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a384-120">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="8a384-120">-EnvironmentName</span></span>
<span data-ttu-id="8a384-121">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a384-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a384-122">-InputObject</span></span>
<span data-ttu-id="8a384-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8a384-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a384-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a384-124">-Name</span></span>
<span data-ttu-id="8a384-125">O nome do conjunto de dados de referência de série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a384-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a384-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a384-127">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a384-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a384-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a384-128">-SubscriptionId</span></span>
<span data-ttu-id="8a384-129">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a384-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a384-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a384-130">CommonParameters</span></span>
<span data-ttu-id="8a384-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a384-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a384-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a384-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a384-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a384-133">INPUTS</span></span>

### <span data-ttu-id="8a384-134">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="8a384-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="8a384-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a384-135">OUTPUTS</span></span>

### <span data-ttu-id="8a384-136">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="8a384-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="8a384-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a384-137">NOTES</span></span>

<span data-ttu-id="8a384-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8a384-138">ALIASES</span></span>

<span data-ttu-id="8a384-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8a384-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a384-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8a384-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a384-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a384-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a384-142">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8a384-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a384-143">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="8a384-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="8a384-144">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="8a384-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="8a384-145">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="8a384-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="8a384-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8a384-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a384-147">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="8a384-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="8a384-148">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a384-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="8a384-149">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a384-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8a384-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a384-150">RELATED LINKS</span></span>

