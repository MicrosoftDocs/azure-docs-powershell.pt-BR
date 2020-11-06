---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601598"
---
# <span data-ttu-id="711dd-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="711dd-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="711dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="711dd-102">SYNOPSIS</span></span>
<span data-ttu-id="711dd-103">Obtém runbooks de automação e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="711dd-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="711dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="711dd-104">SYNTAX</span></span>

### <span data-ttu-id="711dd-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="711dd-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711dd-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="711dd-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711dd-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="711dd-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711dd-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="711dd-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711dd-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="711dd-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="711dd-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="711dd-110">DESCRIPTION</span></span>
<span data-ttu-id="711dd-111">O cmdlet **Get-AzAutomationScheduledRunbook** Obtém um ou mais Runbooks de automação do Azure e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="711dd-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="711dd-112">Por padrão, esse cmdlet obtém todos os runbooks programados.</span><span class="sxs-lookup"><span data-stu-id="711dd-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="711dd-113">Especifique o nome de um runbook ou um cronograma ou ambos para ver agendas de runbook específicas.</span><span class="sxs-lookup"><span data-stu-id="711dd-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="711dd-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="711dd-114">EXAMPLES</span></span>

### <span data-ttu-id="711dd-115">Exemplo 1: obter todos os runbooks agendados</span><span class="sxs-lookup"><span data-stu-id="711dd-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="711dd-116">Esse comando obtém todos os runbooks agendados na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="711dd-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="711dd-117">Exemplo 2: obter todos os cronogramas associados a um runbook</span><span class="sxs-lookup"><span data-stu-id="711dd-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="711dd-118">Esse comando obtém todos os runbooks agendados para o runbook Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="711dd-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="711dd-119">Exemplo 3: obter todos os runbooks associados a um cronograma</span><span class="sxs-lookup"><span data-stu-id="711dd-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="711dd-120">Esse comando obtém todos os runbooks agendados para o Schedule Schedule01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="711dd-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="711dd-121">OS</span><span class="sxs-lookup"><span data-stu-id="711dd-121">PARAMETERS</span></span>

### <span data-ttu-id="711dd-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="711dd-122">-AutomationAccountName</span></span>
<span data-ttu-id="711dd-123">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="711dd-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="711dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711dd-124">-DefaultProfile</span></span>
<span data-ttu-id="711dd-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="711dd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="711dd-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="711dd-126">-JobScheduleId</span></span>
<span data-ttu-id="711dd-127">Especifica a ID de um trabalho agendado que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="711dd-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="711dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="711dd-129">Especifica o nome de um grupo de recursos para os runbooks agendados que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="711dd-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="711dd-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="711dd-130">-RunbookName</span></span>
<span data-ttu-id="711dd-131">Especifica o nome de um runbook para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="711dd-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="711dd-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="711dd-132">-ScheduleName</span></span>
<span data-ttu-id="711dd-133">Especifica o nome de um cronograma para o qual esse cmdlet obtém runbooks agendados.</span><span class="sxs-lookup"><span data-stu-id="711dd-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="711dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711dd-134">CommonParameters</span></span>
<span data-ttu-id="711dd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="711dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711dd-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="711dd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711dd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="711dd-137">INPUTS</span></span>

### <span data-ttu-id="711dd-138">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="711dd-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="711dd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="711dd-139">System.String</span></span>

## <span data-ttu-id="711dd-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="711dd-140">OUTPUTS</span></span>

### <span data-ttu-id="711dd-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="711dd-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="711dd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="711dd-142">NOTES</span></span>

## <span data-ttu-id="711dd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="711dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="711dd-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="711dd-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="711dd-145">Cancelar registro-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="711dd-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


