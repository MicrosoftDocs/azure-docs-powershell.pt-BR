---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 203573856740e0e155e7dff0755ecad1b5399440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601479"
---
# <span data-ttu-id="7478f-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7478f-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="7478f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7478f-102">SYNOPSIS</span></span>
<span data-ttu-id="7478f-103">Remove uma associação entre um runbook e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7478f-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="7478f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7478f-104">SYNTAX</span></span>

### <span data-ttu-id="7478f-105">ByJobScheduleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="7478f-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7478f-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="7478f-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7478f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7478f-107">DESCRIPTION</span></span>
<span data-ttu-id="7478f-108">O cmdlet **Unregister-AzAutomationScheduledRunbook** remove a associação entre um runbook de automação do Azure e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7478f-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="7478f-109">O cronograma não inicia mais o runbook.</span><span class="sxs-lookup"><span data-stu-id="7478f-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="7478f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7478f-110">EXAMPLES</span></span>

### <span data-ttu-id="7478f-111">Exemplo 1: remover a associação entre um runbook e um cronograma</span><span class="sxs-lookup"><span data-stu-id="7478f-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="7478f-112">Esse comando Remove a associação entre o runbook chamado Runbk01 e o agendamento chamado Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="7478f-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="7478f-113">OS</span><span class="sxs-lookup"><span data-stu-id="7478f-113">PARAMETERS</span></span>

### <span data-ttu-id="7478f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7478f-114">-AutomationAccountName</span></span>
<span data-ttu-id="7478f-115">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="7478f-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7478f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7478f-116">-DefaultProfile</span></span>
<span data-ttu-id="7478f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7478f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7478f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7478f-118">-Force</span></span>
<span data-ttu-id="7478f-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="7478f-119">ps_force</span></span>

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

### <span data-ttu-id="7478f-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="7478f-120">-JobScheduleId</span></span>
<span data-ttu-id="7478f-121">Especifica a ID de um runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="7478f-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="7478f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7478f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7478f-123">Especifica o nome de um grupo de recursos para o runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="7478f-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="7478f-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="7478f-124">-RunbookName</span></span>
<span data-ttu-id="7478f-125">Especifica o nome do runbook que este cmdlet dissocia de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7478f-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="7478f-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="7478f-126">-ScheduleName</span></span>
<span data-ttu-id="7478f-127">Especifica o nome do cronograma a partir do qual esse cmdlet dissocia um runbook.</span><span class="sxs-lookup"><span data-stu-id="7478f-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="7478f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7478f-128">-Confirm</span></span>
<span data-ttu-id="7478f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7478f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7478f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7478f-130">-WhatIf</span></span>
<span data-ttu-id="7478f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7478f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7478f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7478f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7478f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7478f-133">CommonParameters</span></span>
<span data-ttu-id="7478f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7478f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7478f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7478f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7478f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7478f-136">INPUTS</span></span>

### <span data-ttu-id="7478f-137">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7478f-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7478f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7478f-138">System.String</span></span>

## <span data-ttu-id="7478f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7478f-139">OUTPUTS</span></span>

### <span data-ttu-id="7478f-140">System. void</span><span class="sxs-lookup"><span data-stu-id="7478f-140">System.Void</span></span>

## <span data-ttu-id="7478f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7478f-141">NOTES</span></span>

## <span data-ttu-id="7478f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7478f-142">RELATED LINKS</span></span>

[<span data-ttu-id="7478f-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7478f-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="7478f-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7478f-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


