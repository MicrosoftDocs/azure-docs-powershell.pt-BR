---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: a8e79dfcd505de6cb1a539f0b194f549835a95f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432968"
---
# <span data-ttu-id="275a0-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="275a0-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="275a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="275a0-102">SYNOPSIS</span></span>
<span data-ttu-id="275a0-103">Remove uma associação entre um runbook e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="275a0-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="275a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="275a0-104">SYNTAX</span></span>

### <span data-ttu-id="275a0-105">ByJobScheduleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="275a0-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="275a0-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="275a0-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275a0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="275a0-107">DESCRIPTION</span></span>
<span data-ttu-id="275a0-108">O cmdlet **Unregister-AzureRmAutomationScheduledRunbook** remove a associação entre um runbook de automação do Azure e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="275a0-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="275a0-109">O cronograma não inicia mais o runbook.</span><span class="sxs-lookup"><span data-stu-id="275a0-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="275a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="275a0-110">EXAMPLES</span></span>

### <span data-ttu-id="275a0-111">Exemplo 1: remover a associação entre um runbook e um cronograma</span><span class="sxs-lookup"><span data-stu-id="275a0-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="275a0-112">Esse comando Remove a associação entre o runbook chamado Runbk01 e o agendamento chamado Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="275a0-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="275a0-113">OS</span><span class="sxs-lookup"><span data-stu-id="275a0-113">PARAMETERS</span></span>

### <span data-ttu-id="275a0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="275a0-114">-AutomationAccountName</span></span>
<span data-ttu-id="275a0-115">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="275a0-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275a0-116">-DefaultProfile</span></span>
<span data-ttu-id="275a0-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="275a0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="275a0-118">-Force</span></span>
<span data-ttu-id="275a0-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="275a0-119">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="275a0-120">-JobScheduleId</span></span>
<span data-ttu-id="275a0-121">Especifica a ID de um runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="275a0-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="275a0-123">Especifica o nome de um grupo de recursos para o runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="275a0-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="275a0-124">-RunbookName</span></span>
<span data-ttu-id="275a0-125">Especifica o nome do runbook que este cmdlet dissocia de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="275a0-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="275a0-126">-ScheduleName</span></span>
<span data-ttu-id="275a0-127">Especifica o nome do cronograma a partir do qual esse cmdlet dissocia um runbook.</span><span class="sxs-lookup"><span data-stu-id="275a0-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="275a0-128">-Confirm</span></span>
<span data-ttu-id="275a0-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275a0-130">-WhatIf</span></span>
<span data-ttu-id="275a0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="275a0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275a0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="275a0-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275a0-133">CommonParameters</span></span>
<span data-ttu-id="275a0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275a0-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275a0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275a0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="275a0-136">INPUTS</span></span>

### <span data-ttu-id="275a0-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="275a0-137">None</span></span>
<span data-ttu-id="275a0-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="275a0-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="275a0-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="275a0-139">OUTPUTS</span></span>

## <span data-ttu-id="275a0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="275a0-140">NOTES</span></span>

## <span data-ttu-id="275a0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="275a0-141">RELATED LINKS</span></span>

[<span data-ttu-id="275a0-142">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="275a0-142">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="275a0-143">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="275a0-143">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

