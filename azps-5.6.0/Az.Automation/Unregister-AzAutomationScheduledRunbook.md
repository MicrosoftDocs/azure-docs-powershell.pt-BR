---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 68f86795a36e605457982898b24cd6dab878ee1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893406"
---
# <span data-ttu-id="e1021-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e1021-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="e1021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1021-102">SYNOPSIS</span></span>
<span data-ttu-id="e1021-103">Remove uma associação entre uma runbook e uma agenda.</span><span class="sxs-lookup"><span data-stu-id="e1021-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="e1021-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1021-104">SYNTAX</span></span>

### <span data-ttu-id="e1021-105">ByJobScheduleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1021-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1021-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="e1021-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1021-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1021-107">DESCRIPTION</span></span>
<span data-ttu-id="e1021-108">O **cmdlet Unregister-AzAutomationScheduledRunbook** remove a associação entre um runbook de Automação do Azure e uma agenda.</span><span class="sxs-lookup"><span data-stu-id="e1021-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="e1021-109">A agenda não inicia mais o runbook.</span><span class="sxs-lookup"><span data-stu-id="e1021-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="e1021-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1021-110">EXAMPLES</span></span>

### <span data-ttu-id="e1021-111">Exemplo 1: Remover a associação entre um runbook e uma agenda</span><span class="sxs-lookup"><span data-stu-id="e1021-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="e1021-112">Este comando remove a associação entre o runbook chamado Runbk01 e a agenda chamada Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="e1021-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="e1021-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1021-113">PARAMETERS</span></span>

### <span data-ttu-id="e1021-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1021-114">-AutomationAccountName</span></span>
<span data-ttu-id="e1021-115">Especifica uma conta de Automação para o runbook no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="e1021-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e1021-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1021-116">-DefaultProfile</span></span>
<span data-ttu-id="e1021-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e1021-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1021-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e1021-118">-Force</span></span>
<span data-ttu-id="e1021-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="e1021-119">ps_force</span></span>

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

### <span data-ttu-id="e1021-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="e1021-120">-JobScheduleId</span></span>
<span data-ttu-id="e1021-121">Especifica a ID de um runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="e1021-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1021-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1021-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1021-123">Especifica o nome de um grupo de recursos para o runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="e1021-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="e1021-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e1021-124">-RunbookName</span></span>
<span data-ttu-id="e1021-125">Especifica o nome do runbook que esse cmdlet dissocia de uma agenda.</span><span class="sxs-lookup"><span data-stu-id="e1021-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1021-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="e1021-126">-ScheduleName</span></span>
<span data-ttu-id="e1021-127">Especifica o nome do cronograma do qual esse cmdlet dissocia um runbook.</span><span class="sxs-lookup"><span data-stu-id="e1021-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1021-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1021-128">-Confirm</span></span>
<span data-ttu-id="e1021-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1021-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1021-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1021-130">-WhatIf</span></span>
<span data-ttu-id="e1021-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1021-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1021-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1021-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1021-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1021-133">CommonParameters</span></span>
<span data-ttu-id="e1021-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1021-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1021-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1021-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1021-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1021-136">INPUTS</span></span>

### <span data-ttu-id="e1021-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1021-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e1021-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e1021-138">System.String</span></span>

## <span data-ttu-id="e1021-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1021-139">OUTPUTS</span></span>

### <span data-ttu-id="e1021-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="e1021-140">System.Void</span></span>

## <span data-ttu-id="e1021-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1021-141">NOTES</span></span>

## <span data-ttu-id="e1021-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1021-142">RELATED LINKS</span></span>

[<span data-ttu-id="e1021-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e1021-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="e1021-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e1021-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


