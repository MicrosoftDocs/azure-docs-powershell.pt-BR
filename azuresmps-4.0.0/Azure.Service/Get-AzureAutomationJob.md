---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946369"
---
# <span data-ttu-id="d0f1e-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0f1e-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="d0f1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0f1e-102">SYNOPSIS</span></span>

<span data-ttu-id="d0f1e-103">Obtém um ou mais trabalhos do runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="d0f1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0f1e-104">SYNTAX</span></span>

### <span data-ttu-id="d0f1e-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0f1e-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d0f1e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="d0f1e-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0f1e-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d0f1e-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0f1e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0f1e-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d0f1e-109">O cmdlet **Get-AzureAutomationJob** Obtém um ou mais trabalhos de runbook na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d0f1e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="d0f1e-111">Exemplo 1: obter um trabalho de runbook específico</span><span class="sxs-lookup"><span data-stu-id="d0f1e-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="d0f1e-112">Esse comando obtém o trabalho que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="d0f1e-113">Exemplo 2: obter todos os trabalhos de um runbook</span><span class="sxs-lookup"><span data-stu-id="d0f1e-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="d0f1e-114">Esse comando obtém todos os trabalhos associados a um runbook chamado MyRunbook.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="d0f1e-115">Exemplo 2: obter todos os trabalhos em execução</span><span class="sxs-lookup"><span data-stu-id="d0f1e-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="d0f1e-116">Esse comando obtém todos os trabalhos em execução na conta de automação com o nome Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="d0f1e-117">OS</span><span class="sxs-lookup"><span data-stu-id="d0f1e-117">PARAMETERS</span></span>

### <span data-ttu-id="d0f1e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0f1e-118">-AutomationAccountName</span></span>
<span data-ttu-id="d0f1e-119">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="d0f1e-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d0f1e-120">-EndTime</span></span>
<span data-ttu-id="d0f1e-121">Especifica a hora de término de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="d0f1e-122">-Id</span></span>
<span data-ttu-id="d0f1e-123">Especifica a ID de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1e-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d0f1e-124">-Profile</span></span>
<span data-ttu-id="d0f1e-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d0f1e-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0f1e-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d0f1e-127">-RunbookName</span></span>
<span data-ttu-id="d0f1e-128">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1e-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d0f1e-129">-StartTime</span></span>
<span data-ttu-id="d0f1e-130">Especifica a hora de início de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1e-131">-Status</span><span class="sxs-lookup"><span data-stu-id="d0f1e-131">-Status</span></span>
<span data-ttu-id="d0f1e-132">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-132">Specifies the status of a job.</span></span>
<span data-ttu-id="d0f1e-133">Este cmdlet obtém trabalhos que têm um status correspondente a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="d0f1e-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="d0f1e-134">Valid values are:</span></span> 

- <span data-ttu-id="d0f1e-135">Feito</span><span class="sxs-lookup"><span data-stu-id="d0f1e-135">Completed</span></span>
- <span data-ttu-id="d0f1e-136">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="d0f1e-136">Failed</span></span>
- <span data-ttu-id="d0f1e-137">Na fila</span><span class="sxs-lookup"><span data-stu-id="d0f1e-137">Queued</span></span>
- <span data-ttu-id="d0f1e-138">Iniciais</span><span class="sxs-lookup"><span data-stu-id="d0f1e-138">Starting</span></span>
- <span data-ttu-id="d0f1e-139">Resuming</span><span class="sxs-lookup"><span data-stu-id="d0f1e-139">Resuming</span></span>
- <span data-ttu-id="d0f1e-140">Executando</span><span class="sxs-lookup"><span data-stu-id="d0f1e-140">Running</span></span>
- <span data-ttu-id="d0f1e-141">Terminou</span><span class="sxs-lookup"><span data-stu-id="d0f1e-141">Stopped</span></span>
- <span data-ttu-id="d0f1e-142">Interromper</span><span class="sxs-lookup"><span data-stu-id="d0f1e-142">Stopping</span></span>
- <span data-ttu-id="d0f1e-143">Interrompido</span><span class="sxs-lookup"><span data-stu-id="d0f1e-143">Suspended</span></span>
- <span data-ttu-id="d0f1e-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="d0f1e-144">Suspending</span></span>
- <span data-ttu-id="d0f1e-145">Activa</span><span class="sxs-lookup"><span data-stu-id="d0f1e-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f1e-146">CommonParameters</span></span>
<span data-ttu-id="d0f1e-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f1e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f1e-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f1e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f1e-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0f1e-149">INPUTS</span></span>

## <span data-ttu-id="d0f1e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0f1e-150">OUTPUTS</span></span>

### <span data-ttu-id="d0f1e-151">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="d0f1e-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="d0f1e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0f1e-152">NOTES</span></span>

## <span data-ttu-id="d0f1e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0f1e-153">RELATED LINKS</span></span>

[<span data-ttu-id="d0f1e-154">Currículo-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0f1e-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="d0f1e-155">Parar-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0f1e-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="d0f1e-156">Suspender-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0f1e-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


