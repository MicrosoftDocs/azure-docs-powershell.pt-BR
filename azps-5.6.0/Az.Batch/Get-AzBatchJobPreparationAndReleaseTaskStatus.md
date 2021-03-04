---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889319"
---
# <span data-ttu-id="09034-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="09034-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="09034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09034-102">SYNOPSIS</span></span>
<span data-ttu-id="09034-103">Obtém o status da tarefa de preparação e lançamento do trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="09034-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="09034-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09034-104">SYNTAX</span></span>

### <span data-ttu-id="09034-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09034-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09034-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="09034-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09034-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09034-107">DESCRIPTION</span></span>
<span data-ttu-id="09034-108">O cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** obtém o status da tarefa de preparação e liberação do trabalho em lote do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="09034-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="09034-109">Você deve fornecer o *parâmetro Id* ou uma **instância do PSCloudJob** a este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09034-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="09034-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09034-110">EXAMPLES</span></span>

### <span data-ttu-id="09034-111">Exemplo 1: Obter o status de preparação e versão do trabalho</span><span class="sxs-lookup"><span data-stu-id="09034-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="09034-112">Este comando obtém o status da tarefa de preparação e liberação do trabalho "Test".</span><span class="sxs-lookup"><span data-stu-id="09034-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="09034-113">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="09034-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="09034-114">Exemplo 2: Obter o status de preparação e versão do trabalho com Filter e Select especificados</span><span class="sxs-lookup"><span data-stu-id="09034-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="09034-115">Este comando obtém o status da tarefa de preparação e liberação do trabalho "Test" no nó "tvm-2316545714_1-20170613t201733z" e usa a cláusula Select para especificar apenas retornar as informações JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="09034-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="09034-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09034-116">PARAMETERS</span></span>

### <span data-ttu-id="09034-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="09034-117">-BatchContext</span></span>
<span data-ttu-id="09034-118">A instância BatchAccountContext a ser usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="09034-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="09034-119">Use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="09034-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="09034-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09034-120">-DefaultProfile</span></span>
<span data-ttu-id="09034-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="09034-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09034-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="09034-122">-Expand</span></span>
<span data-ttu-id="09034-123">Especifica uma cláusula de expansão do Protocolo de Dados Abertos (OData).</span><span class="sxs-lookup"><span data-stu-id="09034-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="09034-124">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obter.</span><span class="sxs-lookup"><span data-stu-id="09034-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="09034-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="09034-125">-Filter</span></span>
<span data-ttu-id="09034-126">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="09034-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="09034-127">Se você não especificar um filtro, este cmdlet retornará toda a preparação do trabalho e o status da tarefa de versão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="09034-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="09034-128">-Id</span><span class="sxs-lookup"><span data-stu-id="09034-128">-Id</span></span>
<span data-ttu-id="09034-129">Especifica a ID do trabalho cujas tarefas de preparação e lançamento devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="09034-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="09034-130">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="09034-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="09034-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09034-131">-InputObject</span></span>
<span data-ttu-id="09034-132">Especifica um **objeto PSCloudJob** que representa o trabalho para obter o status da tarefa de preparação e lançamento.</span><span class="sxs-lookup"><span data-stu-id="09034-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="09034-133">Para obter um **objeto PSCloudJob,** use Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09034-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="09034-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="09034-134">-MaxCount</span></span>
<span data-ttu-id="09034-135">Especifica o número máximo de trabalhos de preparação e liberação de status da tarefa' a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="09034-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="09034-136">Se você especificar um valor zero (0) ou menor, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="09034-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="09034-137">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="09034-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="09034-138">-Select</span><span class="sxs-lookup"><span data-stu-id="09034-138">-Select</span></span>
<span data-ttu-id="09034-139">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="09034-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="09034-140">Especifique um valor para que esse parâmetro receba propriedades específicas, em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="09034-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="09034-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09034-141">CommonParameters</span></span>
<span data-ttu-id="09034-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09034-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09034-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09034-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09034-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09034-144">INPUTS</span></span>

### <span data-ttu-id="09034-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="09034-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="09034-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="09034-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="09034-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09034-147">OUTPUTS</span></span>

### <span data-ttu-id="09034-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="09034-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="09034-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="09034-149">NOTES</span></span>

## <span data-ttu-id="09034-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09034-150">RELATED LINKS</span></span>

[<span data-ttu-id="09034-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="09034-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="09034-152">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="09034-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
