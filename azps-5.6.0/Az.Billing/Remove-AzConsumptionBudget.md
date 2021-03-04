---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: 58a4b7be314489a847479692a08f495fcf4c7146
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889314"
---
# <span data-ttu-id="d238c-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="d238c-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="d238c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d238c-102">SYNOPSIS</span></span>
<span data-ttu-id="d238c-103">Remova um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d238c-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d238c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d238c-104">SYNTAX</span></span>

### <span data-ttu-id="d238c-105">Assinatura (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d238c-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d238c-106">Canalização</span><span class="sxs-lookup"><span data-stu-id="d238c-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d238c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d238c-107">DESCRIPTION</span></span>
<span data-ttu-id="d238c-108">O Remove-AzConsumptionBudget cmdlet remove um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d238c-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d238c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d238c-109">EXAMPLES</span></span>

### <span data-ttu-id="d238c-110">Exemplo 1: Remover um orçamento com um nome de orçamento no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="d238c-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="d238c-111">Exemplo 2: Remover um orçamento com um nome de orçamento no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d238c-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="d238c-112">Exemplo 3: Remover um orçamento por meio de canalização no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="d238c-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="d238c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d238c-113">PARAMETERS</span></span>

### <span data-ttu-id="d238c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d238c-114">-DefaultProfile</span></span>
<span data-ttu-id="d238c-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d238c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d238c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d238c-116">-InputObject</span></span>
<span data-ttu-id="d238c-117">Objeto Budget.</span><span class="sxs-lookup"><span data-stu-id="d238c-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d238c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d238c-118">-Name</span></span>
<span data-ttu-id="d238c-119">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="d238c-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d238c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d238c-120">-PassThru</span></span>
<span data-ttu-id="d238c-121">O Cmdlet retornará true se um orçamento tiver sido removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="d238c-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="d238c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d238c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d238c-123">Grupo de Recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="d238c-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d238c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d238c-124">-Confirm</span></span>
<span data-ttu-id="d238c-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d238c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d238c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d238c-126">-WhatIf</span></span>
<span data-ttu-id="d238c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d238c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d238c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d238c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d238c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d238c-129">CommonParameters</span></span>
<span data-ttu-id="d238c-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d238c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d238c-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d238c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d238c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d238c-132">INPUTS</span></span>

### <span data-ttu-id="d238c-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="d238c-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="d238c-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d238c-134">OUTPUTS</span></span>

### <span data-ttu-id="d238c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d238c-135">System.Boolean</span></span>

## <span data-ttu-id="d238c-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d238c-136">NOTES</span></span>

## <span data-ttu-id="d238c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d238c-137">RELATED LINKS</span></span>
