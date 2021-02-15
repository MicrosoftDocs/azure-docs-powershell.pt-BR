---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112370"
---
# <span data-ttu-id="c9224-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="c9224-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="c9224-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9224-102">SYNOPSIS</span></span>
<span data-ttu-id="c9224-103">Obtém o conjunto de dados de referência com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="c9224-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9224-104">SYNTAX</span></span>

### <span data-ttu-id="c9224-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c9224-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9224-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c9224-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9224-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9224-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9224-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9224-108">DESCRIPTION</span></span>
<span data-ttu-id="c9224-109">Obtém o conjunto de dados de referência com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="c9224-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9224-110">EXAMPLES</span></span>

### <span data-ttu-id="c9224-111">Exemplo 1: Listar todos os conjuntos de dados de referência no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="c9224-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="c9224-112">Esse comando lista todos os conjuntos de dados de referência sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="c9224-113">Exemplo 2: Obter um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="c9224-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="c9224-114">Esse comando obtém um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="c9224-115">Exemplo 3: Obter um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="c9224-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="c9224-116">Esse comando obtém um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="c9224-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9224-117">PARAMETERS</span></span>

### <span data-ttu-id="c9224-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9224-118">-DefaultProfile</span></span>
<span data-ttu-id="c9224-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9224-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9224-120">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="c9224-120">-EnvironmentName</span></span>
<span data-ttu-id="c9224-121">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c9224-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9224-122">-InputObject</span></span>
<span data-ttu-id="c9224-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c9224-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9224-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9224-124">-Name</span></span>
<span data-ttu-id="c9224-125">O nome do conjunto de dados de referência insights de série de tempo associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="c9224-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9224-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9224-127">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9224-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c9224-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9224-128">-SubscriptionId</span></span>
<span data-ttu-id="c9224-129">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9224-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c9224-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9224-130">CommonParameters</span></span>
<span data-ttu-id="c9224-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9224-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9224-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9224-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9224-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9224-133">INPUTS</span></span>

### <span data-ttu-id="c9224-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="c9224-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="c9224-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9224-135">OUTPUTS</span></span>

### <span data-ttu-id="c9224-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="c9224-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="c9224-137">Notas</span><span class="sxs-lookup"><span data-stu-id="c9224-137">NOTES</span></span>

<span data-ttu-id="c9224-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="c9224-138">ALIASES</span></span>

<span data-ttu-id="c9224-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="c9224-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9224-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c9224-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9224-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9224-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9224-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="c9224-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9224-143">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="c9224-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="c9224-144">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="c9224-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="c9224-145">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c9224-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="c9224-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="c9224-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9224-147">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="c9224-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="c9224-148">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9224-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="c9224-149">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9224-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c9224-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9224-150">RELATED LINKS</span></span>

