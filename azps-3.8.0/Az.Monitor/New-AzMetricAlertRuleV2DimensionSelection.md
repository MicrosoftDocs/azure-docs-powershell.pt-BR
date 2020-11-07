---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 57741aa1f06816e8fac1bbb6722ea4d3c6f66761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940395"
---
# <span data-ttu-id="0792b-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0792b-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="0792b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0792b-102">SYNOPSIS</span></span>
<span data-ttu-id="0792b-103">Cria um objeto de seleção de dimensão local que pode ser usado para construir um critério de alerta métrico.</span><span class="sxs-lookup"><span data-stu-id="0792b-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="0792b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0792b-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0792b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0792b-105">DESCRIPTION</span></span>
<span data-ttu-id="0792b-106">O cmdlet **New-AzMetricAlertRuleV2DimensionSelection** cria um objeto de seleção de dimensão local para ajudar na construção de critérios de alerta métrico usando o cmdlet **New-AzMetricAlertRuleV2Criteria** .</span><span class="sxs-lookup"><span data-stu-id="0792b-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="0792b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0792b-107">EXAMPLES</span></span>

### <span data-ttu-id="0792b-108">Exemplo 1: criar um objeto de seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="0792b-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="0792b-109">Esse comando cria um objeto de seleção de dimensão que especifica que os valores {1,3,4} precisam ser selecionados para a dimensão "LUN"</span><span class="sxs-lookup"><span data-stu-id="0792b-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="0792b-110">OS</span><span class="sxs-lookup"><span data-stu-id="0792b-110">PARAMETERS</span></span>

### <span data-ttu-id="0792b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0792b-111">-DefaultProfile</span></span>
<span data-ttu-id="0792b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0792b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0792b-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="0792b-113">-DimensionName</span></span>
<span data-ttu-id="0792b-114">O nome da dimensão</span><span class="sxs-lookup"><span data-stu-id="0792b-114">The Dimension name</span></span>

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

### <span data-ttu-id="0792b-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="0792b-115">-ValuesToExclude</span></span>
<span data-ttu-id="0792b-116">O ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="0792b-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="0792b-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="0792b-117">-ValuesToInclude</span></span>
<span data-ttu-id="0792b-118">O IncludeValues</span><span class="sxs-lookup"><span data-stu-id="0792b-118">The IncludeValues</span></span>

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

### <span data-ttu-id="0792b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0792b-119">CommonParameters</span></span>
<span data-ttu-id="0792b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0792b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0792b-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0792b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0792b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0792b-122">INPUTS</span></span>

### <span data-ttu-id="0792b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0792b-123">System.String</span></span>

### <span data-ttu-id="0792b-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="0792b-124">System.String[]</span></span>

## <span data-ttu-id="0792b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0792b-125">OUTPUTS</span></span>

### <span data-ttu-id="0792b-126">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="0792b-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="0792b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0792b-127">NOTES</span></span>

## <span data-ttu-id="0792b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0792b-128">RELATED LINKS</span></span>
