---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: da687cc3831f4a3cb278dbf032905b39750b8c8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892247"
---
# <span data-ttu-id="ee26e-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee26e-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="ee26e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee26e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee26e-103">Exclui um agendamento de automação.</span><span class="sxs-lookup"><span data-stu-id="ee26e-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="ee26e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee26e-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee26e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee26e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee26e-106">O cmdlet **Remove-AzAutomationSchedule** exclui uma agenda do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ee26e-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="ee26e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee26e-107">EXAMPLES</span></span>

### <span data-ttu-id="ee26e-108">Exemplo 1: Remover um cronograma</span><span class="sxs-lookup"><span data-stu-id="ee26e-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ee26e-109">Este comando exclui a agenda chamada Agenda01 na conta de automação Contoso17 no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ee26e-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ee26e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee26e-110">PARAMETERS</span></span>

### <span data-ttu-id="ee26e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee26e-111">-AutomationAccountName</span></span>
<span data-ttu-id="ee26e-112">Especifica o nome de uma conta de Automação para a qual este cmdlet remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="ee26e-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee26e-113">-DefaultProfile</span></span>
<span data-ttu-id="ee26e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ee26e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee26e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee26e-115">-Force</span></span>
<span data-ttu-id="ee26e-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="ee26e-116">ps_force</span></span>

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

### <span data-ttu-id="ee26e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ee26e-117">-Name</span></span>
<span data-ttu-id="ee26e-118">Especifica o nome do agendamento que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="ee26e-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee26e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ee26e-120">Especifica o nome de um grupo de recursos para o qual este cmdlet remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="ee26e-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee26e-121">-Confirm</span></span>
<span data-ttu-id="ee26e-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee26e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee26e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee26e-123">-WhatIf</span></span>
<span data-ttu-id="ee26e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee26e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee26e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee26e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee26e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee26e-126">CommonParameters</span></span>
<span data-ttu-id="ee26e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee26e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee26e-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee26e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee26e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee26e-129">INPUTS</span></span>

### <span data-ttu-id="ee26e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ee26e-130">System.String</span></span>

## <span data-ttu-id="ee26e-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee26e-131">OUTPUTS</span></span>

### <span data-ttu-id="ee26e-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee26e-132">System.Void</span></span>

## <span data-ttu-id="ee26e-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee26e-133">NOTES</span></span>

## <span data-ttu-id="ee26e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee26e-134">RELATED LINKS</span></span>

[<span data-ttu-id="ee26e-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee26e-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="ee26e-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee26e-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="ee26e-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ee26e-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


