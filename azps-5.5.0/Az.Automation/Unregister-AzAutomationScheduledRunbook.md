---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117989"
---
# <span data-ttu-id="23cd0-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="23cd0-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="23cd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="23cd0-103">Remove uma associação entre uma agenda e uma agenda.</span><span class="sxs-lookup"><span data-stu-id="23cd0-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="23cd0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23cd0-104">SYNTAX</span></span>

### <span data-ttu-id="23cd0-105">ByJobScheduleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23cd0-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23cd0-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="23cd0-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cd0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="23cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="23cd0-108">O **cmdlet Unregister-AzAutomationScheduledRunbook** remove a associação entre um runbook de Automação do Azure e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="23cd0-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="23cd0-109">O cronograma não inicia mais o livro de executar.</span><span class="sxs-lookup"><span data-stu-id="23cd0-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="23cd0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23cd0-110">EXAMPLES</span></span>

### <span data-ttu-id="23cd0-111">Exemplo 1: Remover a associação entre uma agenda e uma agenda</span><span class="sxs-lookup"><span data-stu-id="23cd0-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="23cd0-112">Esse comando remove a associação entre o runbook chamado Runbk01 e o cronograma chamado Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="23cd0-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="23cd0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23cd0-113">PARAMETERS</span></span>

### <span data-ttu-id="23cd0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23cd0-114">-AutomationAccountName</span></span>
<span data-ttu-id="23cd0-115">Especifica uma conta de Automação para o runbook no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="23cd0-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="23cd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cd0-116">-DefaultProfile</span></span>
<span data-ttu-id="23cd0-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="23cd0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23cd0-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="23cd0-118">-Force</span></span>
<span data-ttu-id="23cd0-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="23cd0-119">ps_force</span></span>

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

### <span data-ttu-id="23cd0-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="23cd0-120">-JobScheduleId</span></span>
<span data-ttu-id="23cd0-121">Especifica a ID de um livro de executar agendado.</span><span class="sxs-lookup"><span data-stu-id="23cd0-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="23cd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="23cd0-123">Especifica o nome de um grupo de recursos para o livro de executar agendado.</span><span class="sxs-lookup"><span data-stu-id="23cd0-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="23cd0-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="23cd0-124">-RunbookName</span></span>
<span data-ttu-id="23cd0-125">Especifica o nome do livro de runbook que este cmdlet divide de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="23cd0-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="23cd0-126">-Nomedo Agendamento</span><span class="sxs-lookup"><span data-stu-id="23cd0-126">-ScheduleName</span></span>
<span data-ttu-id="23cd0-127">Especifica o nome do cronograma a partir do qual este cmdlet desmarca uma runbook.</span><span class="sxs-lookup"><span data-stu-id="23cd0-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="23cd0-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="23cd0-128">-Confirm</span></span>
<span data-ttu-id="23cd0-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cd0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cd0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cd0-130">-WhatIf</span></span>
<span data-ttu-id="23cd0-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="23cd0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cd0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23cd0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cd0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cd0-133">CommonParameters</span></span>
<span data-ttu-id="23cd0-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cd0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cd0-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cd0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cd0-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="23cd0-136">INPUTS</span></span>

### <span data-ttu-id="23cd0-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23cd0-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="23cd0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="23cd0-138">System.String</span></span>

## <span data-ttu-id="23cd0-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="23cd0-139">OUTPUTS</span></span>

### <span data-ttu-id="23cd0-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="23cd0-140">System.Void</span></span>

## <span data-ttu-id="23cd0-141">Notas</span><span class="sxs-lookup"><span data-stu-id="23cd0-141">NOTES</span></span>

## <span data-ttu-id="23cd0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23cd0-142">RELATED LINKS</span></span>

[<span data-ttu-id="23cd0-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="23cd0-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="23cd0-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="23cd0-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


