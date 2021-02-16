---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127137"
---
# <span data-ttu-id="ef81f-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ef81f-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="ef81f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef81f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef81f-103">Obtém trabalhos de manual de automação.</span><span class="sxs-lookup"><span data-stu-id="ef81f-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="ef81f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef81f-104">SYNTAX</span></span>

### <span data-ttu-id="ef81f-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef81f-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef81f-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="ef81f-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef81f-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ef81f-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef81f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef81f-108">DESCRIPTION</span></span>
<span data-ttu-id="ef81f-109">O **cmdlet Get-AzAutomationJob** obtém trabalhos de livro de executar no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ef81f-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="ef81f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ef81f-110">EXAMPLES</span></span>

### <span data-ttu-id="ef81f-111">Exemplo 1: Obter um trabalho específico da sua agenda de trabalho</span><span class="sxs-lookup"><span data-stu-id="ef81f-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="ef81f-112">Esse comando obtém o trabalho que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="ef81f-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="ef81f-113">Exemplo 2: Obter todos os trabalhos para uma agenda de tarefas</span><span class="sxs-lookup"><span data-stu-id="ef81f-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="ef81f-114">Esse comando obtém todos os trabalhos associados a uma runbook chamada Runbook02.</span><span class="sxs-lookup"><span data-stu-id="ef81f-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="ef81f-115">Exemplo 3: Obter todos os trabalhos em execução</span><span class="sxs-lookup"><span data-stu-id="ef81f-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="ef81f-116">Esse comando obtém todos os trabalhos em execução na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ef81f-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ef81f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef81f-117">PARAMETERS</span></span>

### <span data-ttu-id="ef81f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef81f-118">-AutomationAccountName</span></span>
<span data-ttu-id="ef81f-119">Especifica o nome de uma conta de Automação para a qual este cmdlet obtém trabalhos.</span><span class="sxs-lookup"><span data-stu-id="ef81f-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="ef81f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef81f-120">-DefaultProfile</span></span>
<span data-ttu-id="ef81f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ef81f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef81f-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ef81f-122">-EndTime</span></span>
<span data-ttu-id="ef81f-123">Especifica a hora de término de um trabalho como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="ef81f-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ef81f-124">Você pode especificar uma cadeia de caracteres que pode ser convertida em **um DateTimeOffset válido.**</span><span class="sxs-lookup"><span data-stu-id="ef81f-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="ef81f-125">Este cmdlet obtém trabalhos que têm uma hora de término em ou antes do valor especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ef81f-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef81f-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ef81f-126">-Id</span></span>
<span data-ttu-id="ef81f-127">Especifica a ID de um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ef81f-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef81f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef81f-128">-ResourceGroupName</span></span>
<span data-ttu-id="ef81f-129">Especifica o nome de um grupo de recursos no qual este cmdlet obtém trabalhos.</span><span class="sxs-lookup"><span data-stu-id="ef81f-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="ef81f-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ef81f-130">-RunbookName</span></span>
<span data-ttu-id="ef81f-131">Especifica o nome de uma runbook para a qual este cmdlet obtém trabalhos.</span><span class="sxs-lookup"><span data-stu-id="ef81f-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef81f-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ef81f-132">-StartTime</span></span>
<span data-ttu-id="ef81f-133">Especifica a hora de início de um trabalho como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="ef81f-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ef81f-134">Este cmdlet obtém trabalhos que têm uma hora de início em ou após o valor especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ef81f-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef81f-135">-Status</span><span class="sxs-lookup"><span data-stu-id="ef81f-135">-Status</span></span>
<span data-ttu-id="ef81f-136">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ef81f-136">Specifies the status of a job.</span></span>
<span data-ttu-id="ef81f-137">Este cmdlet obtém trabalhos que têm um status correspondente a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ef81f-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="ef81f-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="ef81f-138">Valid values are:</span></span> 
- <span data-ttu-id="ef81f-139">Ativar</span><span class="sxs-lookup"><span data-stu-id="ef81f-139">Activating</span></span>
- <span data-ttu-id="ef81f-140">Concluído</span><span class="sxs-lookup"><span data-stu-id="ef81f-140">Completed</span></span>
- <span data-ttu-id="ef81f-141">Falhou</span><span class="sxs-lookup"><span data-stu-id="ef81f-141">Failed</span></span>
- <span data-ttu-id="ef81f-142">Enfileirado</span><span class="sxs-lookup"><span data-stu-id="ef81f-142">Queued</span></span>
- <span data-ttu-id="ef81f-143">Retomar</span><span class="sxs-lookup"><span data-stu-id="ef81f-143">Resuming</span></span>
- <span data-ttu-id="ef81f-144">Executando</span><span class="sxs-lookup"><span data-stu-id="ef81f-144">Running</span></span>
- <span data-ttu-id="ef81f-145">Começando</span><span class="sxs-lookup"><span data-stu-id="ef81f-145">Starting</span></span>
- <span data-ttu-id="ef81f-146">Parou</span><span class="sxs-lookup"><span data-stu-id="ef81f-146">Stopped</span></span>
- <span data-ttu-id="ef81f-147">Parar</span><span class="sxs-lookup"><span data-stu-id="ef81f-147">Stopping</span></span>
- <span data-ttu-id="ef81f-148">Suspenso</span><span class="sxs-lookup"><span data-stu-id="ef81f-148">Suspended</span></span>
- <span data-ttu-id="ef81f-149">Suspender</span><span class="sxs-lookup"><span data-stu-id="ef81f-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef81f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef81f-150">CommonParameters</span></span>
<span data-ttu-id="ef81f-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef81f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef81f-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef81f-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef81f-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="ef81f-153">INPUTS</span></span>

### <span data-ttu-id="ef81f-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ef81f-154">System.Guid</span></span>

### <span data-ttu-id="ef81f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ef81f-155">System.String</span></span>

## <span data-ttu-id="ef81f-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="ef81f-156">OUTPUTS</span></span>

### <span data-ttu-id="ef81f-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="ef81f-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="ef81f-158">Notas</span><span class="sxs-lookup"><span data-stu-id="ef81f-158">NOTES</span></span>

## <span data-ttu-id="ef81f-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef81f-159">RELATED LINKS</span></span>

[<span data-ttu-id="ef81f-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ef81f-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="ef81f-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ef81f-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="ef81f-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ef81f-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="ef81f-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ef81f-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


