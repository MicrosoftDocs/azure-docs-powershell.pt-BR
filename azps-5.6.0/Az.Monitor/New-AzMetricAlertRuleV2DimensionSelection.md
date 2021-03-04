---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886748"
---
# <span data-ttu-id="380b9-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="380b9-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="380b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380b9-102">SYNOPSIS</span></span>
<span data-ttu-id="380b9-103">Cria um objeto de seleção de dimensão local que pode ser usado para construir um critério de alerta métrico.</span><span class="sxs-lookup"><span data-stu-id="380b9-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="380b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="380b9-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="380b9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="380b9-105">DESCRIPTION</span></span>
<span data-ttu-id="380b9-106">O cmdlet **New-AzMetricAlertRuleV2DimensionSelection** cria um objeto de seleção de dimensão local para ajudar na construção de critérios de alerta métricos usando o cmdlet [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="380b9-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="380b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="380b9-107">EXAMPLES</span></span>

### <span data-ttu-id="380b9-108">Exemplo 1: Criar um objeto de seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="380b9-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="380b9-109">Este comando cria um objeto de seleção de dimensão que especifica que os valores precisam ser selecionados {1,3,4} para Dimension "LUN"</span><span class="sxs-lookup"><span data-stu-id="380b9-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="380b9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="380b9-110">PARAMETERS</span></span>

### <span data-ttu-id="380b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380b9-111">-DefaultProfile</span></span>
<span data-ttu-id="380b9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="380b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380b9-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="380b9-113">-DimensionName</span></span>
<span data-ttu-id="380b9-114">O nome da dimensão</span><span class="sxs-lookup"><span data-stu-id="380b9-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380b9-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="380b9-115">-ValuesToExclude</span></span>
<span data-ttu-id="380b9-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="380b9-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380b9-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="380b9-117">-ValuesToInclude</span></span>
<span data-ttu-id="380b9-118">The IncludeValues</span><span class="sxs-lookup"><span data-stu-id="380b9-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380b9-119">CommonParameters</span></span>
<span data-ttu-id="380b9-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380b9-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="380b9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380b9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="380b9-122">INPUTS</span></span>

### <span data-ttu-id="380b9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="380b9-123">System.String</span></span>

### <span data-ttu-id="380b9-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="380b9-124">System.String[]</span></span>

## <span data-ttu-id="380b9-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="380b9-125">OUTPUTS</span></span>

### <span data-ttu-id="380b9-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="380b9-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="380b9-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="380b9-127">NOTES</span></span>

## <span data-ttu-id="380b9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="380b9-128">RELATED LINKS</span></span>
