---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: a0c6952b86485d6ec8417e6399e8f8348cd6f9a4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947265"
---
# <span data-ttu-id="8d7f5-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d7f5-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="8d7f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7f5-103">Obtém as tarefas em lotes para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="8d7f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d7f5-104">SYNTAX</span></span>

### <span data-ttu-id="8d7f5-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d7f5-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d7f5-106">%</span><span class="sxs-lookup"><span data-stu-id="8d7f5-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d7f5-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d7f5-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d7f5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d7f5-108">DESCRIPTION</span></span>
<span data-ttu-id="8d7f5-109">O cmdlet **Get-AzBatchTask** Obtém tarefas em lotes do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="8d7f5-110">Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="8d7f5-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="8d7f5-111">Para obter uma única tarefa, especifique o parâmetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="8d7f5-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="8d7f5-112">Você pode especificar o parâmetro *Filter* para obter as tarefas correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8d7f5-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8d7f5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d7f5-113">EXAMPLES</span></span>

### <span data-ttu-id="8d7f5-114">Exemplo 1: obter uma tarefa por ID</span><span class="sxs-lookup"><span data-stu-id="8d7f5-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="8d7f5-115">Este comando obtém a tarefa com a ID Task03 no Job Job01.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="8d7f5-116">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8d7f5-117">Exemplo 2: obter todas as tarefas concluídas de um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="8d7f5-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="8d7f5-118">Esse comando obtém as tarefas concluídas a partir do trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="8d7f5-119">OS</span><span class="sxs-lookup"><span data-stu-id="8d7f5-119">PARAMETERS</span></span>

### <span data-ttu-id="8d7f5-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8d7f5-120">-BatchContext</span></span>
<span data-ttu-id="8d7f5-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8d7f5-122">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8d7f5-123">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8d7f5-124">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8d7f5-125">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7f5-126">-DefaultProfile</span></span>
<span data-ttu-id="8d7f5-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d7f5-128">-Expandir</span><span class="sxs-lookup"><span data-stu-id="8d7f5-128">-Expand</span></span>
<span data-ttu-id="8d7f5-129">Especifica uma cláusula de expansão OData.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="8d7f5-130">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal para obter.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8d7f5-131">-Filter</span></span>
<span data-ttu-id="8d7f5-132">Especifica uma cláusula de filtro OData para tarefas.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="8d7f5-133">Se você não especificar um filtro, esse cmdlet retornará todas as tarefas para a conta ou o trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-134">-ID</span><span class="sxs-lookup"><span data-stu-id="8d7f5-134">-Id</span></span>
<span data-ttu-id="8d7f5-135">Especifica a ID da tarefa obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="8d7f5-136">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-137">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="8d7f5-137">-Job</span></span>
<span data-ttu-id="8d7f5-138">Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="8d7f5-139">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="8d7f5-140">-JobId</span></span>
<span data-ttu-id="8d7f5-141">Especifica a ID do trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8d7f5-142">-MaxCount</span></span>
<span data-ttu-id="8d7f5-143">Especifica o número máximo de tarefas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="8d7f5-144">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8d7f5-145">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-146">-Selecione</span><span class="sxs-lookup"><span data-stu-id="8d7f5-146">-Select</span></span>
<span data-ttu-id="8d7f5-147">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="8d7f5-148">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7f5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7f5-149">CommonParameters</span></span>
<span data-ttu-id="8d7f5-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d7f5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7f5-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d7f5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7f5-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d7f5-152">INPUTS</span></span>

### <span data-ttu-id="8d7f5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8d7f5-153">System.String</span></span>

### <span data-ttu-id="8d7f5-154">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="8d7f5-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="8d7f5-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8d7f5-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8d7f5-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d7f5-156">OUTPUTS</span></span>

### <span data-ttu-id="8d7f5-157">Microsoft.Azure.Commands.Batch. Modelos. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8d7f5-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="8d7f5-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d7f5-158">NOTES</span></span>

## <span data-ttu-id="8d7f5-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d7f5-159">RELATED LINKS</span></span>

[<span data-ttu-id="8d7f5-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8d7f5-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8d7f5-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8d7f5-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="8d7f5-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d7f5-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="8d7f5-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d7f5-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="8d7f5-164">Parar-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8d7f5-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="8d7f5-165">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8d7f5-165">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


