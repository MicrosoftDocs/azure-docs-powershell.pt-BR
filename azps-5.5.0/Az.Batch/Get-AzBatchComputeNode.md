---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115997"
---
# <span data-ttu-id="5b0f6-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5b0f6-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="5b0f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0f6-103">Obtém nós de computação em lotes de um pool.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="5b0f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b0f6-104">SYNTAX</span></span>

### <span data-ttu-id="5b0f6-105">ODataFilter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b0f6-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b0f6-106">Id</span><span class="sxs-lookup"><span data-stu-id="5b0f6-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b0f6-107">Parentobject</span><span class="sxs-lookup"><span data-stu-id="5b0f6-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b0f6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b0f6-108">DESCRIPTION</span></span>
<span data-ttu-id="5b0f6-109">O cmdlet **Get-AzBatchComputeNode** obtém nós de computação em lote do Azure de um pool.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="5b0f6-110">Especifique o *parâmetro PoolID* ou *Pool.*</span><span class="sxs-lookup"><span data-stu-id="5b0f6-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="5b0f6-111">Especifique *o parâmetro Id* para obter um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="5b0f6-112">*Especifique o* parâmetro Filtro para obter os nós de computação que corresponderem a um filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="5b0f6-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="5b0f6-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b0f6-113">EXAMPLES</span></span>

### <span data-ttu-id="5b0f6-114">Exemplo 1: Obter um nó de computação por ID</span><span class="sxs-lookup"><span data-stu-id="5b0f6-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="5b0f6-115">Esse comando obtém o nó de computação que tem o ID tvm-2316545714_1-20150725t21320z do pool que tem o Pool de ID.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="5b0f6-116">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5b0f6-117">Exemplo 2: Obter todos os nós de computação ocioso de um pool</span><span class="sxs-lookup"><span data-stu-id="5b0f6-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="5b0f6-118">Esse comando obtém todos os nós de computação ocioso contidos no pool que tem o Pool de ID06.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="5b0f6-119">O comando especifica o estado ocioso usando o *parâmetro* Filtro.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="5b0f6-120">Exemplo 3: Obter todos os nós de computação em um pool especificado</span><span class="sxs-lookup"><span data-stu-id="5b0f6-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
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
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="5b0f6-121">Esse comando obtém o pool que tem o Pool de ID07 usando o cmdlet Get-AzBatchPool usuário.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="5b0f6-122">O comando passa esse pool para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b0f6-123">Esse cmdlet obtém todos os nós de computação desse pool.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="5b0f6-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b0f6-124">PARAMETERS</span></span>

### <span data-ttu-id="5b0f6-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5b0f6-125">-BatchContext</span></span>
<span data-ttu-id="5b0f6-126">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5b0f6-127">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5b0f6-128">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5b0f6-129">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5b0f6-130">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5b0f6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0f6-131">-DefaultProfile</span></span>
<span data-ttu-id="5b0f6-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b0f6-133">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5b0f6-133">-Filter</span></span>
<span data-ttu-id="5b0f6-134">Especifica uma cláusula de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="5b0f6-135">Esse cmdlet retorna nós de computação que corresponderem ao filtro especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="5b0f6-136">Se você não especificar um filtro, esse cmdlet retornará todos os nós de computação para o pool.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="5b0f6-137">-ID</span><span class="sxs-lookup"><span data-stu-id="5b0f6-137">-Id</span></span>
<span data-ttu-id="5b0f6-138">Especifica a ID do nó de computação que este cmdlet obtém do pool.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="5b0f6-139">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="5b0f6-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5b0f6-140">-MaxCount</span></span>
<span data-ttu-id="5b0f6-141">Especifica o número máximo de nós de computação a retornar.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="5b0f6-142">Se você especificar um valor zero (0) ou menos, o cmdlet não usará um limite superior.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5b0f6-143">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="5b0f6-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="5b0f6-144">-Pool</span></span>
<span data-ttu-id="5b0f6-145">Especifica o pool, como um **objeto PSCloudPool,** que contém os nós de computação.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="5b0f6-146">Para obter um **objeto PSCloudPool,** use Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="5b0f6-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5b0f6-147">-PoolId</span></span>
<span data-ttu-id="5b0f6-148">Especifica a ID do pool que contém os nós de computação.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="5b0f6-149">-Selecionar</span><span class="sxs-lookup"><span data-stu-id="5b0f6-149">-Select</span></span>
<span data-ttu-id="5b0f6-150">Especifica uma cláusula de seleção OData.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="5b0f6-151">Especifique um valor para esse parâmetro para obter propriedades específicas, em vez de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="5b0f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0f6-152">CommonParameters</span></span>
<span data-ttu-id="5b0f6-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b0f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0f6-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b0f6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0f6-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b0f6-155">INPUTS</span></span>

### <span data-ttu-id="5b0f6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5b0f6-156">System.String</span></span>

### <span data-ttu-id="5b0f6-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="5b0f6-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="5b0f6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5b0f6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5b0f6-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b0f6-159">OUTPUTS</span></span>

### <span data-ttu-id="5b0f6-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5b0f6-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="5b0f6-161">Notas</span><span class="sxs-lookup"><span data-stu-id="5b0f6-161">NOTES</span></span>

## <span data-ttu-id="5b0f6-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b0f6-162">RELATED LINKS</span></span>

[<span data-ttu-id="5b0f6-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5b0f6-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="5b0f6-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="5b0f6-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="5b0f6-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="5b0f6-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="5b0f6-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5b0f6-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5b0f6-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5b0f6-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="5b0f6-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5b0f6-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="5b0f6-169">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="5b0f6-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
