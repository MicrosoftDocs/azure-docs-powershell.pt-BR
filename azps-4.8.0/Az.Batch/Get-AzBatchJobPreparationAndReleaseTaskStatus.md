---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955141"
---
# <span data-ttu-id="95c15-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="95c15-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="95c15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95c15-102">SYNOPSIS</span></span>
<span data-ttu-id="95c15-103">Obtém o status da tarefa de liberação e preparação do trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="95c15-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="95c15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95c15-104">SYNTAX</span></span>

### <span data-ttu-id="95c15-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="95c15-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95c15-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95c15-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c15-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95c15-107">DESCRIPTION</span></span>
<span data-ttu-id="95c15-108">O cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** Obtém a preparação do trabalho em lotes do Azure e o status da tarefa de liberação para um trabalho em lotes.</span><span class="sxs-lookup"><span data-stu-id="95c15-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="95c15-109">Você deve fornecer o parâmetro *ID* ou uma instância **PSCloudJob** para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95c15-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="95c15-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95c15-110">EXAMPLES</span></span>

### <span data-ttu-id="95c15-111">Exemplo 1: obter a preparação do trabalho e o status de lançamento de um trabalho</span><span class="sxs-lookup"><span data-stu-id="95c15-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="95c15-112">Esse comando obtém a preparação do trabalho e o status da tarefa de liberação do trabalho "teste".</span><span class="sxs-lookup"><span data-stu-id="95c15-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="95c15-113">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="95c15-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="95c15-114">Exemplo 2: obter a preparação do trabalho e o status de lançamento de um trabalho com filtro e selecionar especificado</span><span class="sxs-lookup"><span data-stu-id="95c15-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="95c15-115">Este comando obtém a preparação do trabalho e o status da tarefa de liberação para o trabalho "Test" no nó "TVM-2316545714_1-20170613t201733z" e usa a cláusula SELECT para especificar a reutilização das informações do JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="95c15-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="95c15-116">OS</span><span class="sxs-lookup"><span data-stu-id="95c15-116">PARAMETERS</span></span>

### <span data-ttu-id="95c15-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95c15-117">-BatchContext</span></span>
<span data-ttu-id="95c15-118">A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="95c15-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="95c15-119">Use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="95c15-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="95c15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c15-120">-DefaultProfile</span></span>
<span data-ttu-id="95c15-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95c15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c15-122">-Expandir</span><span class="sxs-lookup"><span data-stu-id="95c15-122">-Expand</span></span>
<span data-ttu-id="95c15-123">Especifica uma cláusula de expansão do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="95c15-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="95c15-124">Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.</span><span class="sxs-lookup"><span data-stu-id="95c15-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="95c15-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="95c15-125">-Filter</span></span>
<span data-ttu-id="95c15-126">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="95c15-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="95c15-127">Se você não especificar um filtro, esse cmdlet retornará toda a preparação do trabalho e liberar o status da tarefa para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="95c15-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="95c15-128">-ID</span><span class="sxs-lookup"><span data-stu-id="95c15-128">-Id</span></span>
<span data-ttu-id="95c15-129">Especifica a ID do trabalho cujas tarefas de preparação e liberação devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="95c15-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="95c15-130">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="95c15-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="95c15-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95c15-131">-InputObject</span></span>
<span data-ttu-id="95c15-132">Especifica um objeto **PSCloudJob** que representa o trabalho para obter o status da tarefa de lançamento e preparação de.</span><span class="sxs-lookup"><span data-stu-id="95c15-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="95c15-133">Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="95c15-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="95c15-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="95c15-134">-MaxCount</span></span>
<span data-ttu-id="95c15-135">Especifica o número máximo de preparação de trabalhos e o status da tarefa de liberação ' a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="95c15-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="95c15-136">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="95c15-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="95c15-137">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="95c15-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="95c15-138">-Selecione</span><span class="sxs-lookup"><span data-stu-id="95c15-138">-Select</span></span>
<span data-ttu-id="95c15-139">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="95c15-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="95c15-140">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="95c15-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="95c15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c15-141">CommonParameters</span></span>
<span data-ttu-id="95c15-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c15-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95c15-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c15-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95c15-144">INPUTS</span></span>

### <span data-ttu-id="95c15-145">Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="95c15-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="95c15-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95c15-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="95c15-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95c15-147">OUTPUTS</span></span>

### <span data-ttu-id="95c15-148">Microsoft.Azure.Commands.Batch. Modelos. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="95c15-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="95c15-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95c15-149">NOTES</span></span>

## <span data-ttu-id="95c15-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95c15-150">RELATED LINKS</span></span>

[<span data-ttu-id="95c15-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="95c15-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="95c15-152">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="95c15-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
