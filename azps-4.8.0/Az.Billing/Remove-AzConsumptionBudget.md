---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954432"
---
# <span data-ttu-id="cb2e9-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="cb2e9-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="cb2e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2e9-103">Remova um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="cb2e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb2e9-104">SYNTAX</span></span>

### <span data-ttu-id="cb2e9-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb2e9-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2e9-106">Tubula</span><span class="sxs-lookup"><span data-stu-id="cb2e9-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2e9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb2e9-107">DESCRIPTION</span></span>
<span data-ttu-id="cb2e9-108">O cmdlet Remove-AzConsumptionBudget remove um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="cb2e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb2e9-109">EXAMPLES</span></span>

### <span data-ttu-id="cb2e9-110">Exemplo 1: remover um orçamento com um nome de orçamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="cb2e9-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="cb2e9-111">Exemplo 2: remover um orçamento com um nome de orçamento em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cb2e9-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="cb2e9-112">Exemplo 3: remover um orçamento por meio do encanamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="cb2e9-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="cb2e9-113">OS</span><span class="sxs-lookup"><span data-stu-id="cb2e9-113">PARAMETERS</span></span>

### <span data-ttu-id="cb2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="cb2e9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2e9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb2e9-116">-InputObject</span></span>
<span data-ttu-id="cb2e9-117">Objeto de orçamento.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-117">Budget object.</span></span>

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

### <span data-ttu-id="cb2e9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb2e9-118">-Name</span></span>
<span data-ttu-id="cb2e9-119">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-119">Name of a budget.</span></span>

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

### <span data-ttu-id="cb2e9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb2e9-120">-PassThru</span></span>
<span data-ttu-id="cb2e9-121">O cmdlet retorna true se um orçamento foi removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="cb2e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb2e9-123">Grupo de recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="cb2e9-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb2e9-124">-Confirm</span></span>
<span data-ttu-id="cb2e9-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2e9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2e9-126">-WhatIf</span></span>
<span data-ttu-id="cb2e9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2e9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2e9-129">CommonParameters</span></span>
<span data-ttu-id="cb2e9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2e9-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2e9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2e9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb2e9-132">INPUTS</span></span>

### <span data-ttu-id="cb2e9-133">Microsoft. Azure. Commands. consumo. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="cb2e9-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="cb2e9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb2e9-134">OUTPUTS</span></span>

### <span data-ttu-id="cb2e9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb2e9-135">System.Boolean</span></span>

## <span data-ttu-id="cb2e9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb2e9-136">NOTES</span></span>

## <span data-ttu-id="cb2e9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb2e9-137">RELATED LINKS</span></span>
