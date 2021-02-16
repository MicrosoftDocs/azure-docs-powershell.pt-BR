---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117965"
---
# <span data-ttu-id="3549c-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="3549c-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="3549c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3549c-102">SYNOPSIS</span></span>
<span data-ttu-id="3549c-103">Obtém o status de preparação e liberação de tarefas em lotes.</span><span class="sxs-lookup"><span data-stu-id="3549c-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="3549c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3549c-104">SYNTAX</span></span>

### <span data-ttu-id="3549c-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3549c-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3549c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="3549c-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3549c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3549c-107">DESCRIPTION</span></span>
<span data-ttu-id="3549c-108">O cmdlet **Get-AzBatch JobPreparationAndReleaseTaskStatus** obtém o status de tarefa de preparação e lançamento de tarefas em lote do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="3549c-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="3549c-109">Você deve fornecer o parâmetro *ID* ou uma **instância do PSCloudCloudCloud para** este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3549c-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="3549c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3549c-110">EXAMPLES</span></span>

### <span data-ttu-id="3549c-111">Exemplo 1: Obter o status de preparação e liberação de um trabalho</span><span class="sxs-lookup"><span data-stu-id="3549c-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="3549c-112">Esse comando obtém o status de preparação e liberação da tarefa para o trabalho "Teste".</span><span class="sxs-lookup"><span data-stu-id="3549c-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="3549c-113">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="3549c-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3549c-114">Exemplo 2: Obter o status de preparação e liberação de um trabalho com Filtrar e Selecionar especificado</span><span class="sxs-lookup"><span data-stu-id="3549c-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="3549c-115">Este comando obtém o status da tarefa de preparação e liberação do trabalho "Teste" no nó "tvm-2316545714_1-20170613t201733z" e usa a cláusula Select para especificar apenas as informações jobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="3549c-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="3549c-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3549c-116">PARAMETERS</span></span>

### <span data-ttu-id="3549c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3549c-117">-BatchContext</span></span>
<span data-ttu-id="3549c-118">A instância BatchAccountContext a ser usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="3549c-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="3549c-119">Use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3549c-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="3549c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3549c-120">-DefaultProfile</span></span>
<span data-ttu-id="3549c-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3549c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3549c-122">-Expandir</span><span class="sxs-lookup"><span data-stu-id="3549c-122">-Expand</span></span>
<span data-ttu-id="3549c-123">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="3549c-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="3549c-124">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obter.</span><span class="sxs-lookup"><span data-stu-id="3549c-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="3549c-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3549c-125">-Filter</span></span>
<span data-ttu-id="3549c-126">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3549c-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="3549c-127">Se você não especificar um filtro, esse cmdlet retornará toda a preparação do trabalho e liberará o status da tarefa para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3549c-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="3549c-128">-ID</span><span class="sxs-lookup"><span data-stu-id="3549c-128">-Id</span></span>
<span data-ttu-id="3549c-129">Especifica a ID do trabalho cujas tarefas de preparação e lançamento devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="3549c-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="3549c-130">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="3549c-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3549c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3549c-131">-InputObject</span></span>
<span data-ttu-id="3549c-132">Especifica um objeto **PSCloudCloud Que** representa o trabalho para obter o status da tarefa de preparação e lançamento.</span><span class="sxs-lookup"><span data-stu-id="3549c-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="3549c-133">Para obter um **objeto PSCloudCloud,** use Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3549c-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3549c-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3549c-134">-MaxCount</span></span>
<span data-ttu-id="3549c-135">Especifica o número máximo de trabalhos de preparação e liberação do status da tarefa' a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3549c-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="3549c-136">Se você especificar um valor zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="3549c-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3549c-137">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="3549c-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3549c-138">-Selecionar</span><span class="sxs-lookup"><span data-stu-id="3549c-138">-Select</span></span>
<span data-ttu-id="3549c-139">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="3549c-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="3549c-140">Especifique um valor para esse parâmetro para obter propriedades específicas, em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="3549c-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="3549c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3549c-141">CommonParameters</span></span>
<span data-ttu-id="3549c-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3549c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3549c-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3549c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3549c-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="3549c-144">INPUTS</span></span>

### <span data-ttu-id="3549c-145">Microsoft.Azure.Commands.Batch. Models.PSCloudCloud</span><span class="sxs-lookup"><span data-stu-id="3549c-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="3549c-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3549c-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3549c-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="3549c-147">OUTPUTS</span></span>

### <span data-ttu-id="3549c-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="3549c-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="3549c-149">Notas</span><span class="sxs-lookup"><span data-stu-id="3549c-149">NOTES</span></span>

## <span data-ttu-id="3549c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3549c-150">RELATED LINKS</span></span>

[<span data-ttu-id="3549c-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3549c-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="3549c-152">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="3549c-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
