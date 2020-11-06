---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 6e825e6d582117a919691aea4780868191e8e4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609860"
---
# <span data-ttu-id="c3c4d-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3c4d-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="c3c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c4d-103">Obtém trabalhos do runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3c4d-104">SYNTAX</span></span>

### <span data-ttu-id="c3c4d-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3c4d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3c4d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c3c4d-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3c4d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c3c4d-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c4d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="c3c4d-109">O cmdlet **Get-AzureRmAutomationJob** Obtém os trabalhos do runbook na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="c3c4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3c4d-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c4d-111">Exemplo 1: obter um trabalho de runbook específico</span><span class="sxs-lookup"><span data-stu-id="c3c4d-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="c3c4d-112">Esse comando obtém o trabalho que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="c3c4d-113">Exemplo 2: obter todos os trabalhos de um runbook</span><span class="sxs-lookup"><span data-stu-id="c3c4d-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="c3c4d-114">Esse comando obtém todos os trabalhos associados a um runbook chamado Runbook02.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="c3c4d-115">Exemplo 3: obter todos os trabalhos em execução</span><span class="sxs-lookup"><span data-stu-id="c3c4d-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="c3c4d-116">Esse comando obtém todos os trabalhos em execução na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c3c4d-117">OS</span><span class="sxs-lookup"><span data-stu-id="c3c4d-117">PARAMETERS</span></span>

### <span data-ttu-id="c3c4d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3c4d-118">-AutomationAccountName</span></span>
<span data-ttu-id="c3c4d-119">Especifica o nome de uma conta de automação para a qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c3c4d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c4d-120">-DefaultProfile</span></span>
<span data-ttu-id="c3c4d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3c4d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3c4d-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c3c4d-122">-EndTime</span></span>
<span data-ttu-id="c3c4d-123">Especifica a hora de término de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c3c4d-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c3c4d-124">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c3c4d-125">Esse cmdlet obtém trabalhos que têm uma hora de término em ou antes do valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3c4d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="c3c4d-126">-Id</span></span>
<span data-ttu-id="c3c4d-127">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3c4d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c4d-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3c4d-129">Especifica o nome de um grupo de recursos em que este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c3c4d-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c3c4d-130">-RunbookName</span></span>
<span data-ttu-id="c3c4d-131">Especifica o nome de um runbook para o qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c3c4d-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3c4d-132">-StartTime</span></span>
<span data-ttu-id="c3c4d-133">Especifica a hora de início de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c3c4d-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c3c4d-134">Esse cmdlet obtém os trabalhos que têm uma hora de início em ou após o valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3c4d-135">-Status</span><span class="sxs-lookup"><span data-stu-id="c3c4d-135">-Status</span></span>
<span data-ttu-id="c3c4d-136">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-136">Specifies the status of a job.</span></span>
<span data-ttu-id="c3c4d-137">Este cmdlet obtém trabalhos que têm um status correspondente a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="c3c4d-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c3c4d-138">Valid values are:</span></span> 
- <span data-ttu-id="c3c4d-139">Activa</span><span class="sxs-lookup"><span data-stu-id="c3c4d-139">Activating</span></span>
- <span data-ttu-id="c3c4d-140">Feito</span><span class="sxs-lookup"><span data-stu-id="c3c4d-140">Completed</span></span>
- <span data-ttu-id="c3c4d-141">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="c3c4d-141">Failed</span></span>
- <span data-ttu-id="c3c4d-142">Na fila</span><span class="sxs-lookup"><span data-stu-id="c3c4d-142">Queued</span></span>
- <span data-ttu-id="c3c4d-143">Resuming</span><span class="sxs-lookup"><span data-stu-id="c3c4d-143">Resuming</span></span>
- <span data-ttu-id="c3c4d-144">Executando</span><span class="sxs-lookup"><span data-stu-id="c3c4d-144">Running</span></span>
- <span data-ttu-id="c3c4d-145">Iniciais</span><span class="sxs-lookup"><span data-stu-id="c3c4d-145">Starting</span></span>
- <span data-ttu-id="c3c4d-146">Terminou</span><span class="sxs-lookup"><span data-stu-id="c3c4d-146">Stopped</span></span>
- <span data-ttu-id="c3c4d-147">Interromper</span><span class="sxs-lookup"><span data-stu-id="c3c4d-147">Stopping</span></span>
- <span data-ttu-id="c3c4d-148">Interrompido</span><span class="sxs-lookup"><span data-stu-id="c3c4d-148">Suspended</span></span>
- <span data-ttu-id="c3c4d-149">Suspending</span><span class="sxs-lookup"><span data-stu-id="c3c4d-149">Suspending</span></span>

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

### <span data-ttu-id="c3c4d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c4d-150">CommonParameters</span></span>
<span data-ttu-id="c3c4d-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c4d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c4d-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c4d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c4d-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3c4d-153">INPUTS</span></span>

### <span data-ttu-id="c3c4d-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c3c4d-154">System.Guid</span></span>

### <span data-ttu-id="c3c4d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c4d-155">System.String</span></span>

## <span data-ttu-id="c3c4d-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3c4d-156">OUTPUTS</span></span>

### <span data-ttu-id="c3c4d-157">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="c3c4d-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c3c4d-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3c4d-158">NOTES</span></span>

## <span data-ttu-id="c3c4d-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3c4d-159">RELATED LINKS</span></span>

[<span data-ttu-id="c3c4d-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c3c4d-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="c3c4d-161">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3c4d-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c3c4d-162">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3c4d-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="c3c4d-163">Suspender-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c3c4d-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


