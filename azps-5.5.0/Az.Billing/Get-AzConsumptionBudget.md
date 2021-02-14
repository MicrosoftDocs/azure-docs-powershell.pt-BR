---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116587"
---
# <span data-ttu-id="f583b-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="f583b-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="f583b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f583b-102">SYNOPSIS</span></span>
<span data-ttu-id="f583b-103">Obter uma lista de orçamentos em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f583b-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f583b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f583b-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="f583b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f583b-105">DESCRIPTION</span></span>
<span data-ttu-id="f583b-106">O Get-AzConsumptionBudget cmdlet obtém uma lista de orçamentos em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f583b-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f583b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f583b-107">EXAMPLES</span></span>

### <span data-ttu-id="f583b-108">Exemplo 1: Obter uma lista de orçamentos no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="f583b-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="f583b-109">Exemplo 2: Obter uma lista de orçamentos no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f583b-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="f583b-110">Exemplo 3: Obter um orçamento com o nome do orçamento no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="f583b-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="f583b-111">Exemplo 4: Obter um orçamento com o nome do orçamento no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f583b-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="f583b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f583b-112">PARAMETERS</span></span>

### <span data-ttu-id="f583b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f583b-113">-DefaultProfile</span></span>
<span data-ttu-id="f583b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f583b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f583b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f583b-115">-Name</span></span>
<span data-ttu-id="f583b-116">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="f583b-116">Name of a budget.</span></span>

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

### <span data-ttu-id="f583b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f583b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f583b-118">Grupo de Recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="f583b-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="f583b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f583b-119">CommonParameters</span></span>
<span data-ttu-id="f583b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f583b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f583b-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f583b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f583b-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f583b-122">INPUTS</span></span>

### <span data-ttu-id="f583b-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f583b-123">None</span></span>

## <span data-ttu-id="f583b-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f583b-124">OUTPUTS</span></span>

### <span data-ttu-id="f583b-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="f583b-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="f583b-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f583b-126">NOTES</span></span>

## <span data-ttu-id="f583b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f583b-127">RELATED LINKS</span></span>
