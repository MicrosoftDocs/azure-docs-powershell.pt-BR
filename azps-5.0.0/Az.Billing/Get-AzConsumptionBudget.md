---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118422"
---
# <span data-ttu-id="330d4-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="330d4-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="330d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="330d4-102">SYNOPSIS</span></span>
<span data-ttu-id="330d4-103">Obter uma lista de orçamentos em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="330d4-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="330d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="330d4-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="330d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="330d4-105">DESCRIPTION</span></span>
<span data-ttu-id="330d4-106">O cmdlet Get-AzConsumptionBudget Obtém uma lista de orçamentos em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="330d4-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="330d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="330d4-107">EXAMPLES</span></span>

### <span data-ttu-id="330d4-108">Exemplo 1: obter uma lista de orçamentos no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="330d4-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="330d4-109">Exemplo 2: obter uma lista de orçamentos em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="330d4-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="330d4-110">Exemplo 3: obter um orçamento com o nome do orçamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="330d4-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="330d4-111">Exemplo 4: obter um orçamento com o nome do orçamento em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="330d4-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="330d4-112">OS</span><span class="sxs-lookup"><span data-stu-id="330d4-112">PARAMETERS</span></span>

### <span data-ttu-id="330d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330d4-113">-DefaultProfile</span></span>
<span data-ttu-id="330d4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="330d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="330d4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="330d4-115">-Name</span></span>
<span data-ttu-id="330d4-116">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="330d4-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="330d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="330d4-118">Grupo de recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="330d4-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="330d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330d4-119">CommonParameters</span></span>
<span data-ttu-id="330d4-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="330d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330d4-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="330d4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330d4-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="330d4-122">INPUTS</span></span>

### <span data-ttu-id="330d4-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="330d4-123">None</span></span>

## <span data-ttu-id="330d4-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="330d4-124">OUTPUTS</span></span>

### <span data-ttu-id="330d4-125">Microsoft. Azure. Commands. consumo. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="330d4-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="330d4-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="330d4-126">NOTES</span></span>

## <span data-ttu-id="330d4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="330d4-127">RELATED LINKS</span></span>
