---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 1a177f0987f27f81f0ab27d5e35db11df17ae005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427690"
---
# <span data-ttu-id="da481-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da481-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="da481-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da481-102">SYNOPSIS</span></span>
<span data-ttu-id="da481-103">Obtém as tarefas em lotes para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="da481-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da481-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da481-104">SYNTAX</span></span>

### <span data-ttu-id="da481-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="da481-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da481-106">%</span><span class="sxs-lookup"><span data-stu-id="da481-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da481-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="da481-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da481-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da481-108">DESCRIPTION</span></span>
<span data-ttu-id="da481-109">O cmdlet **Get-AzureBatchTask** Obtém tarefas em lotes do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="da481-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="da481-110">Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .</span><span class="sxs-lookup"><span data-stu-id="da481-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="da481-111">Para obter uma única tarefa, especifique o parâmetro *ID* .</span><span class="sxs-lookup"><span data-stu-id="da481-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="da481-112">Você pode especificar o parâmetro *Filter* para obter as tarefas correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="da481-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="da481-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da481-113">EXAMPLES</span></span>

### <span data-ttu-id="da481-114">Exemplo 1: obter uma tarefa por ID</span><span class="sxs-lookup"><span data-stu-id="da481-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="da481-115">Este comando obtém a tarefa com a ID Task03 no Job Job01.</span><span class="sxs-lookup"><span data-stu-id="da481-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="da481-116">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="da481-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="da481-117">Exemplo 2: obter todas as tarefas concluídas de um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="da481-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="da481-118">Esse comando obtém as tarefas concluídas a partir do trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="da481-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="da481-119">OS</span><span class="sxs-lookup"><span data-stu-id="da481-119">PARAMETERS</span></span>

### <span data-ttu-id="da481-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da481-120">-BatchContext</span></span>
<span data-ttu-id="da481-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="da481-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da481-122">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="da481-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da481-123">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="da481-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da481-124">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="da481-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da481-125">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="da481-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da481-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da481-126">-DefaultProfile</span></span>
<span data-ttu-id="da481-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da481-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-128">-Expandir</span><span class="sxs-lookup"><span data-stu-id="da481-128">-Expand</span></span>
<span data-ttu-id="da481-129">Especifica uma cláusula de expansão OData.</span><span class="sxs-lookup"><span data-stu-id="da481-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="da481-130">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal para obter.</span><span class="sxs-lookup"><span data-stu-id="da481-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="da481-131">-Filter</span></span>
<span data-ttu-id="da481-132">Especifica uma cláusula de filtro OData para tarefas.</span><span class="sxs-lookup"><span data-stu-id="da481-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="da481-133">Se você não especificar um filtro, esse cmdlet retornará todas as tarefas para a conta ou o trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="da481-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-134">-ID</span><span class="sxs-lookup"><span data-stu-id="da481-134">-Id</span></span>
<span data-ttu-id="da481-135">Especifica a ID da tarefa obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da481-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="da481-136">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="da481-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-137">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="da481-137">-Job</span></span>
<span data-ttu-id="da481-138">Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da481-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="da481-139">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="da481-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da481-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="da481-140">-JobId</span></span>
<span data-ttu-id="da481-141">Especifica a ID do trabalho que contém as tarefas obtidas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da481-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da481-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="da481-142">-MaxCount</span></span>
<span data-ttu-id="da481-143">Especifica o número máximo de tarefas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="da481-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="da481-144">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="da481-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="da481-145">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="da481-145">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-146">-Selecione</span><span class="sxs-lookup"><span data-stu-id="da481-146">-Select</span></span>
<span data-ttu-id="da481-147">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="da481-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="da481-148">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="da481-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da481-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da481-149">CommonParameters</span></span>
<span data-ttu-id="da481-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da481-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da481-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da481-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da481-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da481-152">INPUTS</span></span>

### <span data-ttu-id="da481-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da481-153">BatchAccountContext</span></span>
<span data-ttu-id="da481-154">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="da481-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="da481-155">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="da481-155">PSCloudJob</span></span>
<span data-ttu-id="da481-156">O parâmetro ' Job ' aceita o valor do tipo ' PSCloudJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="da481-156">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="da481-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da481-157">OUTPUTS</span></span>

### <span data-ttu-id="da481-158">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="da481-158">PSCloudTask</span></span>

## <span data-ttu-id="da481-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da481-159">NOTES</span></span>

## <span data-ttu-id="da481-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da481-160">RELATED LINKS</span></span>

[<span data-ttu-id="da481-161">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="da481-161">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="da481-162">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="da481-162">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="da481-163">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da481-163">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="da481-164">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da481-164">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="da481-165">Parar-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da481-165">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="da481-166">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="da481-166">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

