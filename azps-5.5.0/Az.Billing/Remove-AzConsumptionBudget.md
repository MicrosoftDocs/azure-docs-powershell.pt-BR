---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116951"
---
# <span data-ttu-id="4edfc-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="4edfc-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="4edfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4edfc-102">SYNOPSIS</span></span>
<span data-ttu-id="4edfc-103">Remova um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4edfc-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4edfc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4edfc-104">SYNTAX</span></span>

### <span data-ttu-id="4edfc-105">Assinatura (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4edfc-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4edfc-106">Tubulação</span><span class="sxs-lookup"><span data-stu-id="4edfc-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4edfc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4edfc-107">DESCRIPTION</span></span>
<span data-ttu-id="4edfc-108">O Remove-AzConsumptionBudget cmdlet remove um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4edfc-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="4edfc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4edfc-109">EXAMPLES</span></span>

### <span data-ttu-id="4edfc-110">Exemplo 1: Remover um orçamento com um nome de orçamento no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="4edfc-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="4edfc-111">Exemplo 2: Remover um orçamento com um nome de orçamento no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4edfc-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="4edfc-112">Exemplo 3: Remover um orçamento por meio de canos no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="4edfc-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="4edfc-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4edfc-113">PARAMETERS</span></span>

### <span data-ttu-id="4edfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4edfc-114">-DefaultProfile</span></span>
<span data-ttu-id="4edfc-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4edfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4edfc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4edfc-116">-InputObject</span></span>
<span data-ttu-id="4edfc-117">Objeto de orçamento.</span><span class="sxs-lookup"><span data-stu-id="4edfc-117">Budget object.</span></span>

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

### <span data-ttu-id="4edfc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4edfc-118">-Name</span></span>
<span data-ttu-id="4edfc-119">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="4edfc-119">Name of a budget.</span></span>

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

### <span data-ttu-id="4edfc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4edfc-120">-PassThru</span></span>
<span data-ttu-id="4edfc-121">O Cmdlet retornará verdadeiro se um orçamento tiver sido removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="4edfc-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="4edfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4edfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="4edfc-123">Grupo de Recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="4edfc-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="4edfc-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4edfc-124">-Confirm</span></span>
<span data-ttu-id="4edfc-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4edfc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4edfc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4edfc-126">-WhatIf</span></span>
<span data-ttu-id="4edfc-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4edfc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4edfc-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4edfc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4edfc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4edfc-129">CommonParameters</span></span>
<span data-ttu-id="4edfc-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4edfc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4edfc-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4edfc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4edfc-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="4edfc-132">INPUTS</span></span>

### <span data-ttu-id="4edfc-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="4edfc-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="4edfc-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="4edfc-134">OUTPUTS</span></span>

### <span data-ttu-id="4edfc-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4edfc-135">System.Boolean</span></span>

## <span data-ttu-id="4edfc-136">Notas</span><span class="sxs-lookup"><span data-stu-id="4edfc-136">NOTES</span></span>

## <span data-ttu-id="4edfc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4edfc-137">RELATED LINKS</span></span>
