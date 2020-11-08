---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113151"
---
# <span data-ttu-id="f67bc-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="f67bc-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="f67bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f67bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f67bc-103">Criar ou atualizar um conjunto de dados de referência no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="f67bc-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="f67bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f67bc-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f67bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f67bc-105">DESCRIPTION</span></span>
<span data-ttu-id="f67bc-106">Criar ou atualizar um conjunto de dados de referência no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="f67bc-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="f67bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f67bc-107">EXAMPLES</span></span>

### <span data-ttu-id="f67bc-108">Exemplo 1: criar um conjunto de dados de referência para um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="f67bc-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="f67bc-109">Esse comando cria um conjunto de dados de referência para um ambiente específico.</span><span class="sxs-lookup"><span data-stu-id="f67bc-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="f67bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="f67bc-110">PARAMETERS</span></span>

### <span data-ttu-id="f67bc-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="f67bc-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="f67bc-112">O comportamento de comparação da chave definir dados de referência pode ser definido usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f67bc-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="f67bc-113">Por padrão, o valor é ' ordinal ', o que significa que a comparação de teclas diferenciadas entre maiúsculas e minúsculas será executada durante a junção de dados de referência com eventos ou ao adicionar novos dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f67bc-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="f67bc-114">Quando ' OrdinalIgnoreCase ' é definido, a comparação de maiúsculas e minúsculas será usada.</span><span class="sxs-lookup"><span data-stu-id="f67bc-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="f67bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67bc-115">-DefaultProfile</span></span>
<span data-ttu-id="f67bc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f67bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f67bc-117">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="f67bc-117">-EnvironmentName</span></span>
<span data-ttu-id="f67bc-118">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f67bc-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f67bc-119">-Keyproperty</span><span class="sxs-lookup"><span data-stu-id="f67bc-119">-KeyProperty</span></span>
<span data-ttu-id="f67bc-120">A lista de propriedades de chave para o conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f67bc-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="f67bc-121">Para construir, consulte a seção de observações para as propriedades de Keyproperty e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f67bc-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="f67bc-122">-Local</span><span class="sxs-lookup"><span data-stu-id="f67bc-122">-Location</span></span>
<span data-ttu-id="f67bc-123">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f67bc-123">The location of the resource.</span></span>

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

### <span data-ttu-id="f67bc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f67bc-124">-Name</span></span>
<span data-ttu-id="f67bc-125">Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f67bc-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="f67bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f67bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="f67bc-127">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f67bc-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f67bc-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f67bc-128">-SubscriptionId</span></span>
<span data-ttu-id="f67bc-129">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f67bc-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f67bc-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="f67bc-130">-Tag</span></span>
<span data-ttu-id="f67bc-131">Pares de valores chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="f67bc-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="f67bc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f67bc-132">-Confirm</span></span>
<span data-ttu-id="f67bc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f67bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f67bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f67bc-134">-WhatIf</span></span>
<span data-ttu-id="f67bc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f67bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f67bc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f67bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f67bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67bc-137">CommonParameters</span></span>
<span data-ttu-id="f67bc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67bc-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f67bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67bc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f67bc-140">INPUTS</span></span>

## <span data-ttu-id="f67bc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f67bc-141">OUTPUTS</span></span>

### <span data-ttu-id="f67bc-142">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="f67bc-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="f67bc-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f67bc-143">NOTES</span></span>

<span data-ttu-id="f67bc-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f67bc-144">ALIASES</span></span>

<span data-ttu-id="f67bc-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f67bc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f67bc-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f67bc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f67bc-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f67bc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f67bc-148">Keyproperty <IReferenceDataSetKeyProperty [] >: a lista de propriedades de chave para o conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f67bc-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="f67bc-149">`[Name <String>]`: O nome da propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f67bc-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="f67bc-150">`[Type <ReferenceDataKeyPropertyType?>]`: O tipo da propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f67bc-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="f67bc-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f67bc-151">RELATED LINKS</span></span>

