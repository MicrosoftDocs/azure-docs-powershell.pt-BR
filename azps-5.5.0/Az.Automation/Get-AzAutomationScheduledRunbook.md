---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116624"
---
# <span data-ttu-id="5eb2f-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5eb2f-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="5eb2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb2f-103">Obtém anuários de automação e agendas associadas.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="5eb2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eb2f-104">SYNTAX</span></span>

### <span data-ttu-id="5eb2f-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb2f-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb2f-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5eb2f-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb2f-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb2f-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb2f-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb2f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eb2f-110">DESCRIPTION</span></span>
<span data-ttu-id="5eb2f-111">O cmdlet **Get-AzAutomationScheduledRunbook** obtém um ou mais runbooks de Automação do Azure e agendas associadas.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="5eb2f-112">Por padrão, esse cmdlet obtém todos os runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="5eb2f-113">Especifique o nome de um runbook ou um cronograma ou ambos para ver cronogramas específicos do runbook.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="5eb2f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5eb2f-114">EXAMPLES</span></span>

### <span data-ttu-id="5eb2f-115">Exemplo 1: Obter todos os runbooks agendados</span><span class="sxs-lookup"><span data-stu-id="5eb2f-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5eb2f-116">Esse comando obtém todos os runbooks agendados na conta automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="5eb2f-117">Exemplo 2: Obter todos os cronogramas associados a um livro de executar</span><span class="sxs-lookup"><span data-stu-id="5eb2f-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="5eb2f-118">Esse comando obtém todos os runbooks agendados do runbook Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="5eb2f-119">Exemplo 3: Obter todos os runbooks associados a um cronograma</span><span class="sxs-lookup"><span data-stu-id="5eb2f-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="5eb2f-120">Esse comando obtém todas as guias de executar agendadas para o cronograma01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5eb2f-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eb2f-121">PARAMETERS</span></span>

### <span data-ttu-id="5eb2f-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-122">-AutomationAccountName</span></span>
<span data-ttu-id="5eb2f-123">Especifica uma conta de Automação para o runbook no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5eb2f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb2f-124">-DefaultProfile</span></span>
<span data-ttu-id="5eb2f-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5eb2f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eb2f-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5eb2f-126">-JobScheduleId</span></span>
<span data-ttu-id="5eb2f-127">Especifica a ID de um trabalho agendado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5eb2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="5eb2f-129">Especifica o nome de um grupo de recursos para runbooks agendados que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5eb2f-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5eb2f-130">-RunbookName</span></span>
<span data-ttu-id="5eb2f-131">Especifica o nome de um livro de runbook para o qual este cmdlet obtém os runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb2f-132">-Nomedo Agendamento</span><span class="sxs-lookup"><span data-stu-id="5eb2f-132">-ScheduleName</span></span>
<span data-ttu-id="5eb2f-133">Especifica o nome de um cronograma para o qual este cmdlet obtém os runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb2f-134">CommonParameters</span></span>
<span data-ttu-id="5eb2f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb2f-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb2f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb2f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="5eb2f-137">INPUTS</span></span>

### <span data-ttu-id="5eb2f-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5eb2f-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5eb2f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5eb2f-139">System.String</span></span>

## <span data-ttu-id="5eb2f-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="5eb2f-140">OUTPUTS</span></span>

### <span data-ttu-id="5eb2f-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="5eb2f-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="5eb2f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="5eb2f-142">NOTES</span></span>

## <span data-ttu-id="5eb2f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb2f-143">RELATED LINKS</span></span>

[<span data-ttu-id="5eb2f-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5eb2f-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="5eb2f-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5eb2f-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


