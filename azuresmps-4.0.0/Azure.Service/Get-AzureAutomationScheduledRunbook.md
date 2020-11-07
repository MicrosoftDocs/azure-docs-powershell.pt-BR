---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946357"
---
# <span data-ttu-id="40dca-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="40dca-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="40dca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40dca-102">SYNOPSIS</span></span>

<span data-ttu-id="40dca-103">Obtém os runbooks de automação do Azure e os cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="40dca-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="40dca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40dca-104">SYNTAX</span></span>

### <span data-ttu-id="40dca-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="40dca-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="40dca-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="40dca-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="40dca-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="40dca-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="40dca-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="40dca-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="40dca-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="40dca-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40dca-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40dca-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="40dca-111">**Get-AzureAutomationScheduledRunbook** Obtém um ou mais Runbooks de automação do Azure e cronogramas associados.</span><span class="sxs-lookup"><span data-stu-id="40dca-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="40dca-112">Por padrão, todos os runbooks programados são retornados.</span><span class="sxs-lookup"><span data-stu-id="40dca-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="40dca-113">Para obter um runbook agendado específico, especifique o nome do runbook e o nome do cronograma.</span><span class="sxs-lookup"><span data-stu-id="40dca-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="40dca-114">Para obter todos os cronogramas associados a um runbook, especifique apenas o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="40dca-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="40dca-115">Para obter todos os runbooks associados a um cronograma, especifique apenas o nome do cronograma.</span><span class="sxs-lookup"><span data-stu-id="40dca-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="40dca-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40dca-116">EXAMPLES</span></span>

### <span data-ttu-id="40dca-117">Exemplo 1: obter todos os runbooks agendados</span><span class="sxs-lookup"><span data-stu-id="40dca-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="40dca-118">Esse comando obtém todos os runbooks agendados na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="40dca-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="40dca-119">Exemplo 2: obter todos os cronogramas associados a um runbook</span><span class="sxs-lookup"><span data-stu-id="40dca-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="40dca-120">Esse comando obtém todos os runbooks agendados para o runbook Runbk01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="40dca-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="40dca-121">Exemplo 3: obter todos os runbooks associados a um cronograma</span><span class="sxs-lookup"><span data-stu-id="40dca-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="40dca-122">Esse comando obtém todos os runbooks agendados para o cronograma Schedule01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="40dca-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="40dca-123">OS</span><span class="sxs-lookup"><span data-stu-id="40dca-123">PARAMETERS</span></span>

### <span data-ttu-id="40dca-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40dca-124">-AutomationAccountName</span></span>
<span data-ttu-id="40dca-125">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="40dca-125">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40dca-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="40dca-126">-JobScheduleId</span></span>
<span data-ttu-id="40dca-127">Especifica a ID de um trabalho agendado.</span><span class="sxs-lookup"><span data-stu-id="40dca-127">Specifies the ID of a scheduled job.</span></span>

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

### <span data-ttu-id="40dca-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="40dca-128">-Profile</span></span>
<span data-ttu-id="40dca-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="40dca-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40dca-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="40dca-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40dca-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="40dca-131">-RunbookName</span></span>
<span data-ttu-id="40dca-132">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="40dca-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40dca-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="40dca-133">-ScheduleName</span></span>
<span data-ttu-id="40dca-134">Especifica o nome de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="40dca-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40dca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dca-135">CommonParameters</span></span>
<span data-ttu-id="40dca-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40dca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dca-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40dca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dca-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40dca-138">INPUTS</span></span>

## <span data-ttu-id="40dca-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40dca-139">OUTPUTS</span></span>

### <span data-ttu-id="40dca-140">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="40dca-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="40dca-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40dca-141">NOTES</span></span>

## <span data-ttu-id="40dca-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40dca-142">RELATED LINKS</span></span>

[<span data-ttu-id="40dca-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="40dca-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="40dca-144">Cancelar registro-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="40dca-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


