---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441206"
---
# <span data-ttu-id="c3faa-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3faa-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="c3faa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3faa-102">SYNOPSIS</span></span>
<span data-ttu-id="c3faa-103">Obtém nós de computação em lotes de um pool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3faa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3faa-104">SYNTAX</span></span>

### <span data-ttu-id="c3faa-105">ODataFilter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3faa-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3faa-106">%</span><span class="sxs-lookup"><span data-stu-id="c3faa-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3faa-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="c3faa-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3faa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3faa-108">DESCRIPTION</span></span>
<span data-ttu-id="c3faa-109">O cmdlet **Get-AzureBatchComputeNode** Obtém os nós de computação em lotes do Azure a partir de um pool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="c3faa-110">Especifique o *poolid* ou o parâmetro do *pool* .</span><span class="sxs-lookup"><span data-stu-id="c3faa-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="c3faa-111">Especifique o parâmetro *ID* para obter um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="c3faa-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="c3faa-112">Especifique o parâmetro *Filter* para obter os nós de computação correspondentes a um filtro do Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="c3faa-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c3faa-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3faa-113">EXAMPLES</span></span>

### <span data-ttu-id="c3faa-114">Exemplo 1: obter um nó de computação por ID</span><span class="sxs-lookup"><span data-stu-id="c3faa-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="c3faa-115">Esse comando obtém o nó de computação que tem a ID TVM-2316545714_1-20150725t213220z do pool que tem a ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="c3faa-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="c3faa-116">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="c3faa-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c3faa-117">Exemplo 2: obter todos os nós de computação ociosa de um pool</span><span class="sxs-lookup"><span data-stu-id="c3faa-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="c3faa-118">Esse comando obtém todos os nós de computação ociosos contidos no pool que tem a ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="c3faa-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="c3faa-119">O comando especifica o estado Idle usando o parâmetro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="c3faa-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="c3faa-120">Exemplo 3: obter todos os nós de computação em um pool especificado</span><span class="sxs-lookup"><span data-stu-id="c3faa-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="c3faa-121">Esse comando obtém o pool com a ID Pool07 usando o cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="c3faa-122">O comando passa o pool para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3faa-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3faa-123">Esse cmdlet obtém todos os nós de computação desse pool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="c3faa-124">OS</span><span class="sxs-lookup"><span data-stu-id="c3faa-124">PARAMETERS</span></span>

### <span data-ttu-id="c3faa-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3faa-125">-BatchContext</span></span>
<span data-ttu-id="c3faa-126">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c3faa-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3faa-127">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c3faa-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c3faa-128">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c3faa-128">-Filter</span></span>
<span data-ttu-id="c3faa-129">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c3faa-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c3faa-130">Esse cmdlet retorna nós de computação que correspondem ao filtro que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3faa-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="c3faa-131">Se você não especificar um filtro, esse cmdlet retornará todos os nós de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="c3faa-132">-ID</span><span class="sxs-lookup"><span data-stu-id="c3faa-132">-Id</span></span>
<span data-ttu-id="c3faa-133">Especifica a ID do nó de computação que esse cmdlet obtém do pool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="c3faa-134">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="c3faa-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3faa-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c3faa-135">-MaxCount</span></span>
<span data-ttu-id="c3faa-136">Especifica o número máximo de nós de computação a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="c3faa-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="c3faa-137">Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="c3faa-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c3faa-138">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="c3faa-138">The default value is 1000.</span></span>

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

### <span data-ttu-id="c3faa-139">-Pool</span><span class="sxs-lookup"><span data-stu-id="c3faa-139">-Pool</span></span>
<span data-ttu-id="c3faa-140">Especifica o pool, como um objeto **PSCloudPool** , que contém os nós de computação.</span><span class="sxs-lookup"><span data-stu-id="c3faa-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="c3faa-141">Para obter um objeto **PSCloudPool** , use o cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="c3faa-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3faa-142">-Poolid</span><span class="sxs-lookup"><span data-stu-id="c3faa-142">-PoolId</span></span>
<span data-ttu-id="c3faa-143">Especifica a ID do pool que contém os nós de computação.</span><span class="sxs-lookup"><span data-stu-id="c3faa-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="c3faa-144">-Selecione</span><span class="sxs-lookup"><span data-stu-id="c3faa-144">-Select</span></span>
<span data-ttu-id="c3faa-145">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="c3faa-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="c3faa-146">Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3faa-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="c3faa-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3faa-147">-DefaultProfile</span></span>
<span data-ttu-id="c3faa-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3faa-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3faa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3faa-149">CommonParameters</span></span>
<span data-ttu-id="c3faa-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3faa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3faa-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3faa-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3faa-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3faa-152">INPUTS</span></span>

### <span data-ttu-id="c3faa-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3faa-153">BatchAccountContext</span></span>
<span data-ttu-id="c3faa-154">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c3faa-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c3faa-155">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c3faa-155">PSCloudPool</span></span>
<span data-ttu-id="c3faa-156">O parâmetro ' Pool ' aceita o valor do tipo ' PSCloudPool ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="c3faa-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="c3faa-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3faa-157">OUTPUTS</span></span>

### <span data-ttu-id="c3faa-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3faa-158">PSComputeNode</span></span>

## <span data-ttu-id="c3faa-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3faa-159">NOTES</span></span>

## <span data-ttu-id="c3faa-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3faa-160">RELATED LINKS</span></span>

[<span data-ttu-id="c3faa-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3faa-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c3faa-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c3faa-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="c3faa-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="c3faa-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="c3faa-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c3faa-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c3faa-165">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3faa-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="c3faa-166">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c3faa-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="c3faa-167">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c3faa-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

