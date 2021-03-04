---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1c4e0fa2a8e204ee3b0dad160d3cfb54f58b4323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888392"
---
# <span data-ttu-id="9c64a-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="9c64a-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="9c64a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c64a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c64a-103">Crie ou atualize um conjunto de dados de referência no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="9c64a-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="9c64a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c64a-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c64a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c64a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c64a-106">Crie ou atualize um conjunto de dados de referência no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="9c64a-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="9c64a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c64a-107">EXAMPLES</span></span>

### <span data-ttu-id="9c64a-108">Exemplo 1: Criar um conjunto de dados de referência para um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="9c64a-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="9c64a-109">Esse comando cria um conjunto de dados de referência para um ambiente específico.</span><span class="sxs-lookup"><span data-stu-id="9c64a-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="9c64a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c64a-110">PARAMETERS</span></span>

### <span data-ttu-id="9c64a-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="9c64a-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="9c64a-112">O comportamento de comparação de chave do conjunto de dados de referência pode ser definido usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="9c64a-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="9c64a-113">Por padrão, o valor é 'Ordinal' - o que significa que a comparação de chaves sensíveis a caso será executada ao ingressar dados de referência com eventos ou ao adicionar novos dados de referência.</span><span class="sxs-lookup"><span data-stu-id="9c64a-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="9c64a-114">Quando 'OrdinalIgnoreCase' for definida, a comparação sem maiúsculas de minúsculas será usada.</span><span class="sxs-lookup"><span data-stu-id="9c64a-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c64a-115">-DefaultProfile</span></span>
<span data-ttu-id="9c64a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c64a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c64a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9c64a-117">-EnvironmentName</span></span>
<span data-ttu-id="9c64a-118">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="9c64a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="9c64a-119">-KeyProperty</span></span>
<span data-ttu-id="9c64a-120">A lista de propriedades principais do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="9c64a-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="9c64a-121">Para construir, consulte a seção NOTES para propriedades KEYPROPERTY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9c64a-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-122">-Location</span><span class="sxs-lookup"><span data-stu-id="9c64a-122">-Location</span></span>
<span data-ttu-id="9c64a-123">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c64a-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9c64a-124">-Name</span></span>
<span data-ttu-id="9c64a-125">Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="9c64a-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c64a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c64a-127">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c64a-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c64a-128">-SubscriptionId</span></span>
<span data-ttu-id="9c64a-129">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c64a-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c64a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c64a-130">-Tag</span></span>
<span data-ttu-id="9c64a-131">Pares de valores-chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="9c64a-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="9c64a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c64a-132">-Confirm</span></span>
<span data-ttu-id="9c64a-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c64a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c64a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c64a-134">-WhatIf</span></span>
<span data-ttu-id="9c64a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c64a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c64a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c64a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c64a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c64a-137">CommonParameters</span></span>
<span data-ttu-id="9c64a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c64a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c64a-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c64a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c64a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c64a-140">INPUTS</span></span>

## <span data-ttu-id="9c64a-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c64a-141">OUTPUTS</span></span>

### <span data-ttu-id="9c64a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="9c64a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="9c64a-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c64a-143">NOTES</span></span>

<span data-ttu-id="9c64a-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9c64a-144">ALIASES</span></span>

<span data-ttu-id="9c64a-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9c64a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c64a-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9c64a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c64a-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c64a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c64a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: a lista de propriedades principais do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="9c64a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="9c64a-149">`[Name <String>]`: O nome da propriedade key.</span><span class="sxs-lookup"><span data-stu-id="9c64a-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="9c64a-150">`[Type <ReferenceDataKeyPropertyType?>]`: O tipo da propriedade key.</span><span class="sxs-lookup"><span data-stu-id="9c64a-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="9c64a-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c64a-151">RELATED LINKS</span></span>

