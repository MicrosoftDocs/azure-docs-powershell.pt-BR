---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441423"
---
# <span data-ttu-id="138ee-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="138ee-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="138ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="138ee-102">SYNOPSIS</span></span>
<span data-ttu-id="138ee-103">Obtém trabalhos do runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="138ee-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="138ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="138ee-104">SYNTAX</span></span>

### <span data-ttu-id="138ee-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="138ee-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="138ee-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="138ee-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="138ee-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="138ee-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="138ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="138ee-108">DESCRIPTION</span></span>
<span data-ttu-id="138ee-109">O cmdlet **Get-AzureRmAutomationJob** Obtém os trabalhos do runbook na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="138ee-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="138ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="138ee-110">EXAMPLES</span></span>

### <span data-ttu-id="138ee-111">Exemplo 1: obter um trabalho de runbook específico</span><span class="sxs-lookup"><span data-stu-id="138ee-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="138ee-112">Esse comando obtém o trabalho que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="138ee-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="138ee-113">Exemplo 2: obter todos os trabalhos de um runbook</span><span class="sxs-lookup"><span data-stu-id="138ee-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="138ee-114">Esse comando obtém todos os trabalhos associados a um runbook chamado Runbook02.</span><span class="sxs-lookup"><span data-stu-id="138ee-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="138ee-115">Exemplo 3: obter todos os trabalhos em execução</span><span class="sxs-lookup"><span data-stu-id="138ee-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="138ee-116">Esse comando obtém todos os trabalhos em execução na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="138ee-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="138ee-117">OS</span><span class="sxs-lookup"><span data-stu-id="138ee-117">PARAMETERS</span></span>

### <span data-ttu-id="138ee-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="138ee-118">-AutomationAccountName</span></span>
<span data-ttu-id="138ee-119">Especifica o nome de uma conta de automação para a qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="138ee-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="138ee-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="138ee-120">-EndTime</span></span>
<span data-ttu-id="138ee-121">Especifica a hora de término de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="138ee-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="138ee-122">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="138ee-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="138ee-123">Esse cmdlet obtém trabalhos que têm uma hora de término em ou antes do valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="138ee-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="138ee-124">-ID</span><span class="sxs-lookup"><span data-stu-id="138ee-124">-Id</span></span>
<span data-ttu-id="138ee-125">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="138ee-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="138ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="138ee-127">Especifica o nome de um grupo de recursos em que este cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="138ee-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="138ee-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="138ee-128">-RunbookName</span></span>
<span data-ttu-id="138ee-129">Especifica o nome de um runbook para o qual esse cmdlet recebe trabalhos.</span><span class="sxs-lookup"><span data-stu-id="138ee-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="138ee-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="138ee-130">-StartTime</span></span>
<span data-ttu-id="138ee-131">Especifica a hora de início de um trabalho como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="138ee-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="138ee-132">Esse cmdlet obtém os trabalhos que têm uma hora de início em ou após o valor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="138ee-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="138ee-133">-Status</span><span class="sxs-lookup"><span data-stu-id="138ee-133">-Status</span></span>
<span data-ttu-id="138ee-134">Especifica o status de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="138ee-134">Specifies the status of a job.</span></span>
<span data-ttu-id="138ee-135">Este cmdlet obtém trabalhos que têm um status correspondente a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="138ee-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="138ee-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="138ee-136">Valid values are:</span></span> 

- <span data-ttu-id="138ee-137">Activa</span><span class="sxs-lookup"><span data-stu-id="138ee-137">Activating</span></span>
- <span data-ttu-id="138ee-138">Feito</span><span class="sxs-lookup"><span data-stu-id="138ee-138">Completed</span></span>
- <span data-ttu-id="138ee-139">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="138ee-139">Failed</span></span>
- <span data-ttu-id="138ee-140">Na fila</span><span class="sxs-lookup"><span data-stu-id="138ee-140">Queued</span></span>
- <span data-ttu-id="138ee-141">Resuming</span><span class="sxs-lookup"><span data-stu-id="138ee-141">Resuming</span></span>
- <span data-ttu-id="138ee-142">Executando</span><span class="sxs-lookup"><span data-stu-id="138ee-142">Running</span></span>
- <span data-ttu-id="138ee-143">Iniciais</span><span class="sxs-lookup"><span data-stu-id="138ee-143">Starting</span></span>
- <span data-ttu-id="138ee-144">Terminou</span><span class="sxs-lookup"><span data-stu-id="138ee-144">Stopped</span></span>
- <span data-ttu-id="138ee-145">Interromper</span><span class="sxs-lookup"><span data-stu-id="138ee-145">Stopping</span></span>
- <span data-ttu-id="138ee-146">Interrompido</span><span class="sxs-lookup"><span data-stu-id="138ee-146">Suspended</span></span>
- <span data-ttu-id="138ee-147">Suspending</span><span class="sxs-lookup"><span data-stu-id="138ee-147">Suspending</span></span>

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

### <span data-ttu-id="138ee-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138ee-148">-DefaultProfile</span></span>
<span data-ttu-id="138ee-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="138ee-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="138ee-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138ee-150">CommonParameters</span></span>
<span data-ttu-id="138ee-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="138ee-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138ee-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="138ee-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138ee-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="138ee-153">INPUTS</span></span>

## <span data-ttu-id="138ee-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="138ee-154">OUTPUTS</span></span>

### <span data-ttu-id="138ee-155">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="138ee-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="138ee-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="138ee-156">NOTES</span></span>

## <span data-ttu-id="138ee-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="138ee-157">RELATED LINKS</span></span>

[<span data-ttu-id="138ee-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="138ee-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="138ee-159">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="138ee-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="138ee-160">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="138ee-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="138ee-161">Suspender-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="138ee-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


