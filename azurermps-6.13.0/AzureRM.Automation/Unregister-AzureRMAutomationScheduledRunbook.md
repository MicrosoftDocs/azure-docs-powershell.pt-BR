---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ab55201ab2566c814455b6b0f6fe3c2ddf6b3a57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433328"
---
# <span data-ttu-id="7532c-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7532c-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="7532c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7532c-102">SYNOPSIS</span></span>
<span data-ttu-id="7532c-103">Remove uma associação entre um runbook e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7532c-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7532c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7532c-104">SYNTAX</span></span>

### <span data-ttu-id="7532c-105">ByJobScheduleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="7532c-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7532c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="7532c-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7532c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7532c-107">DESCRIPTION</span></span>
<span data-ttu-id="7532c-108">O cmdlet **Unregister-AzureRmAutomationScheduledRunbook** remove a associação entre um runbook de automação do Azure e um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7532c-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="7532c-109">O cronograma não inicia mais o runbook.</span><span class="sxs-lookup"><span data-stu-id="7532c-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="7532c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7532c-110">EXAMPLES</span></span>

### <span data-ttu-id="7532c-111">Exemplo 1: remover a associação entre um runbook e um cronograma</span><span class="sxs-lookup"><span data-stu-id="7532c-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="7532c-112">Esse comando Remove a associação entre o runbook chamado Runbk01 e o agendamento chamado Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="7532c-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="7532c-113">OS</span><span class="sxs-lookup"><span data-stu-id="7532c-113">PARAMETERS</span></span>

### <span data-ttu-id="7532c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7532c-114">-AutomationAccountName</span></span>
<span data-ttu-id="7532c-115">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="7532c-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7532c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7532c-116">-DefaultProfile</span></span>
<span data-ttu-id="7532c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7532c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7532c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7532c-118">-Force</span></span>
<span data-ttu-id="7532c-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="7532c-119">ps_force</span></span>

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

### <span data-ttu-id="7532c-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="7532c-120">-JobScheduleId</span></span>
<span data-ttu-id="7532c-121">Especifica a ID de um runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="7532c-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="7532c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7532c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7532c-123">Especifica o nome de um grupo de recursos para o runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="7532c-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="7532c-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="7532c-124">-RunbookName</span></span>
<span data-ttu-id="7532c-125">Especifica o nome do runbook que este cmdlet dissocia de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7532c-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="7532c-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="7532c-126">-ScheduleName</span></span>
<span data-ttu-id="7532c-127">Especifica o nome do cronograma a partir do qual esse cmdlet dissocia um runbook.</span><span class="sxs-lookup"><span data-stu-id="7532c-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="7532c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7532c-128">-Confirm</span></span>
<span data-ttu-id="7532c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7532c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7532c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7532c-130">-WhatIf</span></span>
<span data-ttu-id="7532c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7532c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7532c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7532c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7532c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7532c-133">CommonParameters</span></span>
<span data-ttu-id="7532c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7532c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7532c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7532c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7532c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7532c-136">INPUTS</span></span>

### <span data-ttu-id="7532c-137">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7532c-137">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7532c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7532c-138">System.String</span></span>

## <span data-ttu-id="7532c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7532c-139">OUTPUTS</span></span>

### <span data-ttu-id="7532c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="7532c-140">System.Void</span></span>

## <span data-ttu-id="7532c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7532c-141">NOTES</span></span>

## <span data-ttu-id="7532c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7532c-142">RELATED LINKS</span></span>

[<span data-ttu-id="7532c-143">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7532c-143">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="7532c-144">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="7532c-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


