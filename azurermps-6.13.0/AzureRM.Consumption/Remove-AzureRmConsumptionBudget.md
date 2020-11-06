---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433284"
---
# <span data-ttu-id="fa718-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="fa718-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="fa718-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa718-102">SYNOPSIS</span></span>
<span data-ttu-id="fa718-103">Remova um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa718-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa718-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa718-104">SYNTAX</span></span>

### <span data-ttu-id="fa718-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa718-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa718-106">Tubula</span><span class="sxs-lookup"><span data-stu-id="fa718-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa718-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa718-107">DESCRIPTION</span></span>
<span data-ttu-id="fa718-108">O cmdlet Remove-AzureRmConsumptionBudget remove um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa718-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="fa718-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa718-109">EXAMPLES</span></span>

### <span data-ttu-id="fa718-110">Exemplo 1: remover um orçamento com um nome de orçamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="fa718-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="fa718-111">Exemplo 2: remover um orçamento com um nome de orçamento em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fa718-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="fa718-112">Exemplo 3: remover um orçamento por meio do encanamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="fa718-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="fa718-113">OS</span><span class="sxs-lookup"><span data-stu-id="fa718-113">PARAMETERS</span></span>

### <span data-ttu-id="fa718-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa718-114">-DefaultProfile</span></span>
<span data-ttu-id="fa718-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa718-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa718-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa718-116">-InputObject</span></span>
<span data-ttu-id="fa718-117">Objeto de orçamento.</span><span class="sxs-lookup"><span data-stu-id="fa718-117">Budget object.</span></span>

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

### <span data-ttu-id="fa718-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa718-118">-Name</span></span>
<span data-ttu-id="fa718-119">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="fa718-119">Name of a budget.</span></span>

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

### <span data-ttu-id="fa718-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa718-120">-PassThru</span></span>
<span data-ttu-id="fa718-121">O cmdlet retorna true se um orçamento foi removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="fa718-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="fa718-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa718-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa718-123">Grupo de recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="fa718-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="fa718-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa718-124">-Confirm</span></span>
<span data-ttu-id="fa718-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa718-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa718-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa718-126">-WhatIf</span></span>
<span data-ttu-id="fa718-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa718-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa718-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa718-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa718-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa718-129">CommonParameters</span></span>
<span data-ttu-id="fa718-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa718-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa718-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa718-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa718-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa718-132">INPUTS</span></span>

### <span data-ttu-id="fa718-133">Microsoft. Azure. Commands. consumo. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="fa718-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="fa718-134">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa718-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fa718-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa718-135">OUTPUTS</span></span>

### <span data-ttu-id="fa718-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa718-136">System.Boolean</span></span>

## <span data-ttu-id="fa718-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa718-137">NOTES</span></span>

## <span data-ttu-id="fa718-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa718-138">RELATED LINKS</span></span>