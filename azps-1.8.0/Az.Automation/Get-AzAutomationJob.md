---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: ae638c693366568458a4194d1625d19eaac6af93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601613"
---
# <span data-ttu-id="1d08e-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d08e-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="1d08e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d08e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d08e-103">Obtém trabalhos do runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="1d08e-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="1d08e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d08e-104">SYNTAX</span></span>

### <span data-ttu-id="1d08e-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d08e-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d08e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="1d08e-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d08e-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="1d08e-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d08e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d08e-108">DESCRIPTION</span></span>
<span data-ttu-id="1d08e-109">O cmdlet **Get-AzAutomationJob** Obtém os trabalhos do runbook na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d08e-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="1d08e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d08e-110">EXAMPLES</span></span>

### <span data-ttu-id="1d08e-111">Exemplo 1: obter um trabalho de runbook específico</span><span class="sxs-lookup"><span data-stu-id="1d08e-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="1d08e-112">Esse comando obtém o trabalho que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="1d08e-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="1d08e-113">Exemplo 2: obter todos os trabalhos de um runbook</span><span class="sxs-lookup"><span data-stu-id="1d08e-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="1d08e-114">Esse comando obtém todos os trabalhos associados a um runbook chamado Runbook02.</span><span class="sxs-lookup"><span data-stu-id="1d08e-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="1d08e-115">Exemplo 3: obter todos os trabalhos em execução</span><span class="sxs-lookup"><span data-stu-id="1d08e-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="1d08e-116">Esse comando obtém todos os trabalhos em execução na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1d08e-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d08e-117">OS</span><span class="sxs-lookup"><span data-stu-id="1d08e-117">PARAMETERS</span></span>

### <span data-ttu-id="1d08e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d08e-118">-AutomationAccountName</span></span>
<span data-ttu-id="1d08e-119">Especifica o nome de uma conta de automação para a qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1d08e-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="1d08e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d08e-120">-DefaultProfile</span></span>
<span data-ttu-id="1d08e-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1d08e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d08e-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1d08e-122">-EndTime</span></span>
<span data-ttu-id="1d08e-123">Especifica a hora de término de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="1d08e-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1d08e-124">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="1d08e-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="1d08e-125">Esse cmdlet obtém trabalhos que têm uma hora de término em ou antes do valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1d08e-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d08e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1d08e-126">-Id</span></span>
<span data-ttu-id="1d08e-127">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1d08e-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1d08e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d08e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d08e-129">Especifica o nome de um grupo de recursos em que este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1d08e-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="1d08e-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1d08e-130">-RunbookName</span></span>
<span data-ttu-id="1d08e-131">Especifica o nome de um runbook para o qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="1d08e-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="1d08e-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1d08e-132">-StartTime</span></span>
<span data-ttu-id="1d08e-133">Especifica a hora de início de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="1d08e-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1d08e-134">Esse cmdlet obtém os trabalhos que têm uma hora de início em ou após o valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1d08e-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d08e-135">-Status</span><span class="sxs-lookup"><span data-stu-id="1d08e-135">-Status</span></span>
<span data-ttu-id="1d08e-136">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="1d08e-136">Specifies the status of a job.</span></span>
<span data-ttu-id="1d08e-137">Este cmdlet obtém trabalhos que têm um status correspondente a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1d08e-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="1d08e-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1d08e-138">Valid values are:</span></span> 
- <span data-ttu-id="1d08e-139">Activa</span><span class="sxs-lookup"><span data-stu-id="1d08e-139">Activating</span></span>
- <span data-ttu-id="1d08e-140">Feito</span><span class="sxs-lookup"><span data-stu-id="1d08e-140">Completed</span></span>
- <span data-ttu-id="1d08e-141">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="1d08e-141">Failed</span></span>
- <span data-ttu-id="1d08e-142">Na fila</span><span class="sxs-lookup"><span data-stu-id="1d08e-142">Queued</span></span>
- <span data-ttu-id="1d08e-143">Resuming</span><span class="sxs-lookup"><span data-stu-id="1d08e-143">Resuming</span></span>
- <span data-ttu-id="1d08e-144">Executando</span><span class="sxs-lookup"><span data-stu-id="1d08e-144">Running</span></span>
- <span data-ttu-id="1d08e-145">Iniciais</span><span class="sxs-lookup"><span data-stu-id="1d08e-145">Starting</span></span>
- <span data-ttu-id="1d08e-146">Terminou</span><span class="sxs-lookup"><span data-stu-id="1d08e-146">Stopped</span></span>
- <span data-ttu-id="1d08e-147">Interromper</span><span class="sxs-lookup"><span data-stu-id="1d08e-147">Stopping</span></span>
- <span data-ttu-id="1d08e-148">Interrompido</span><span class="sxs-lookup"><span data-stu-id="1d08e-148">Suspended</span></span>
- <span data-ttu-id="1d08e-149">Suspending</span><span class="sxs-lookup"><span data-stu-id="1d08e-149">Suspending</span></span>

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

### <span data-ttu-id="1d08e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d08e-150">CommonParameters</span></span>
<span data-ttu-id="1d08e-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d08e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d08e-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d08e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d08e-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d08e-153">INPUTS</span></span>

### <span data-ttu-id="1d08e-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1d08e-154">System.Guid</span></span>

### <span data-ttu-id="1d08e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1d08e-155">System.String</span></span>

## <span data-ttu-id="1d08e-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d08e-156">OUTPUTS</span></span>

### <span data-ttu-id="1d08e-157">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="1d08e-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="1d08e-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d08e-158">NOTES</span></span>

## <span data-ttu-id="1d08e-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d08e-159">RELATED LINKS</span></span>

[<span data-ttu-id="1d08e-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1d08e-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="1d08e-161">Currículo-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d08e-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="1d08e-162">Parar-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d08e-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="1d08e-163">Suspender-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d08e-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


