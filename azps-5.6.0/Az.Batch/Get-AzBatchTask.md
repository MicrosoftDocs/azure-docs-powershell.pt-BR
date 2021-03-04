---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893242"
---
# <span data-ttu-id="2ee8a-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2ee8a-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="2ee8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee8a-103">Obtém as tarefas Em lotes para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="2ee8a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ee8a-104">SYNTAX</span></span>

### <span data-ttu-id="2ee8a-105">ODataFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ee8a-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee8a-106">Id</span><span class="sxs-lookup"><span data-stu-id="2ee8a-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee8a-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="2ee8a-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ee8a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ee8a-108">DESCRIPTION</span></span>
<span data-ttu-id="2ee8a-109">O cmdlet **Get-AzBatchTask** obtém tarefas do Lote do Azure para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="2ee8a-110">Especifique um trabalho pelo parâmetro *JobId* ou pelo *parâmetro Job.*</span><span class="sxs-lookup"><span data-stu-id="2ee8a-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="2ee8a-111">Para obter uma única tarefa, especifique o *parâmetro Id.*</span><span class="sxs-lookup"><span data-stu-id="2ee8a-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="2ee8a-112">Você pode especificar o parâmetro *Filter* para obter as tarefas que corresponderem a um filtro OData (Protocolo de Dados Abertos).</span><span class="sxs-lookup"><span data-stu-id="2ee8a-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="2ee8a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-113">EXAMPLES</span></span>

### <span data-ttu-id="2ee8a-114">Exemplo 1: Obter uma tarefa por ID</span><span class="sxs-lookup"><span data-stu-id="2ee8a-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="2ee8a-115">Este comando obtém a tarefa com a ID Task03 no trabalho Job01.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="2ee8a-116">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2ee8a-117">Exemplo 2: Obter todas as tarefas concluídas de um trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="2ee8a-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="2ee8a-118">Este comando obtém as tarefas concluídas do trabalho que tem a ID Job02.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="2ee8a-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-119">PARAMETERS</span></span>

### <span data-ttu-id="2ee8a-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2ee8a-120">-BatchContext</span></span>
<span data-ttu-id="2ee8a-121">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2ee8a-122">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2ee8a-123">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2ee8a-124">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2ee8a-125">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2ee8a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee8a-126">-DefaultProfile</span></span>
<span data-ttu-id="2ee8a-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee8a-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="2ee8a-128">-Expand</span></span>
<span data-ttu-id="2ee8a-129">Especifica uma cláusula de expansão OData.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="2ee8a-130">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal a obter.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="2ee8a-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="2ee8a-131">-Filter</span></span>
<span data-ttu-id="2ee8a-132">Especifica uma cláusula de filtro OData para tarefas.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="2ee8a-133">Se você não especificar um filtro, este cmdlet retornará todas as tarefas para a conta ou o trabalho batch.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="2ee8a-134">-Id</span><span class="sxs-lookup"><span data-stu-id="2ee8a-134">-Id</span></span>
<span data-ttu-id="2ee8a-135">Especifica a ID da tarefa que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="2ee8a-136">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="2ee8a-137">-Job</span><span class="sxs-lookup"><span data-stu-id="2ee8a-137">-Job</span></span>
<span data-ttu-id="2ee8a-138">Especifica o trabalho que contém tarefas que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="2ee8a-139">Para obter um **objeto PSCloudJob,** use Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="2ee8a-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="2ee8a-140">-JobId</span></span>
<span data-ttu-id="2ee8a-141">Especifica a ID do trabalho que contém as tarefas que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ee8a-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2ee8a-142">-MaxCount</span></span>
<span data-ttu-id="2ee8a-143">Especifica o número máximo de tarefas a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="2ee8a-144">Se você especificar um valor zero (0) ou menor, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2ee8a-145">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="2ee8a-146">-Select</span><span class="sxs-lookup"><span data-stu-id="2ee8a-146">-Select</span></span>
<span data-ttu-id="2ee8a-147">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="2ee8a-148">Especifique um valor para que esse parâmetro receba propriedades específicas, em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="2ee8a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee8a-149">CommonParameters</span></span>
<span data-ttu-id="2ee8a-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee8a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee8a-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ee8a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee8a-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-152">INPUTS</span></span>

### <span data-ttu-id="2ee8a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2ee8a-153">System.String</span></span>

### <span data-ttu-id="2ee8a-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="2ee8a-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="2ee8a-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ee8a-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ee8a-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-156">OUTPUTS</span></span>

### <span data-ttu-id="2ee8a-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2ee8a-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="2ee8a-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ee8a-158">NOTES</span></span>

## <span data-ttu-id="2ee8a-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ee8a-159">RELATED LINKS</span></span>

[<span data-ttu-id="2ee8a-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2ee8a-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2ee8a-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2ee8a-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2ee8a-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2ee8a-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="2ee8a-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2ee8a-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="2ee8a-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2ee8a-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="2ee8a-165">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="2ee8a-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
