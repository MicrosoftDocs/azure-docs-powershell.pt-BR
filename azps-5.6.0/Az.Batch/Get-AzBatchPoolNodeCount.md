---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 10338e63ed060c1b93c67a2050d28346641f1911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892876"
---
# <span data-ttu-id="a82cf-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="a82cf-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="a82cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a82cf-103">Obtém contagens de nós em lotes por estado de nó agrupado por id do pool.</span><span class="sxs-lookup"><span data-stu-id="a82cf-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="a82cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a82cf-104">SYNTAX</span></span>

### <span data-ttu-id="a82cf-105">AzureBatchPoolNodeCounts (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a82cf-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a82cf-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="a82cf-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a82cf-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="a82cf-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a82cf-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="a82cf-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a82cf-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a82cf-109">DESCRIPTION</span></span>
<span data-ttu-id="a82cf-110">O Get-AzBatchPoolNodeCount cmdlet permite que os clientes recebam novamente as contagens de nós por estado de nó agrupado por pool.</span><span class="sxs-lookup"><span data-stu-id="a82cf-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="a82cf-111">Os estados de nó possíveis estão criando, ocioso, deixandoPool, offline, pré-instalado, reinicializando, reimaginando, executando, iniciando, startTaskFailed, desconhecido, inutilizável e aguardandoForStartTask.</span><span class="sxs-lookup"><span data-stu-id="a82cf-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="a82cf-112">O cmdlet leva o parâmetro PoolId ou Pool para filtrar somente pool com a id do pool especificada.</span><span class="sxs-lookup"><span data-stu-id="a82cf-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="a82cf-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a82cf-113">EXAMPLES</span></span>

### <span data-ttu-id="a82cf-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a82cf-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="a82cf-115">Contagens de nó de lista por estado de nó para pools em contexto de conta em lote atual.</span><span class="sxs-lookup"><span data-stu-id="a82cf-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="a82cf-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a82cf-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="a82cf-117">Mostrar contagens de nó por estado de nó para um pool determinado id de pool.</span><span class="sxs-lookup"><span data-stu-id="a82cf-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="a82cf-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a82cf-118">PARAMETERS</span></span>

### <span data-ttu-id="a82cf-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a82cf-119">-BatchContext</span></span>
<span data-ttu-id="a82cf-120">A instância BatchAccountContext a ser usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="a82cf-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="a82cf-121">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="a82cf-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="a82cf-122">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="a82cf-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="a82cf-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a82cf-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="a82cf-124">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a82cf-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a82cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82cf-125">-DefaultProfile</span></span>
<span data-ttu-id="a82cf-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a82cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a82cf-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a82cf-127">-MaxCount</span></span>
<span data-ttu-id="a82cf-128">Especifica o número máximo de pools a retornar.</span><span class="sxs-lookup"><span data-stu-id="a82cf-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="a82cf-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="a82cf-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82cf-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="a82cf-130">-Pool</span></span>
<span data-ttu-id="a82cf-131">Especifica o **PSCloudPool para** o qual obter contagens de nós.</span><span class="sxs-lookup"><span data-stu-id="a82cf-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a82cf-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a82cf-132">-PoolId</span></span>
<span data-ttu-id="a82cf-133">A id do pool para o qual obter contagens de nós.</span><span class="sxs-lookup"><span data-stu-id="a82cf-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82cf-134">CommonParameters</span></span>
<span data-ttu-id="a82cf-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82cf-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a82cf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82cf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a82cf-137">INPUTS</span></span>

### <span data-ttu-id="a82cf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a82cf-138">System.String</span></span>

### <span data-ttu-id="a82cf-139">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="a82cf-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="a82cf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a82cf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a82cf-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a82cf-141">OUTPUTS</span></span>

### <span data-ttu-id="a82cf-142">Microsoft.Azure.Commands.Batch. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="a82cf-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="a82cf-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="a82cf-143">NOTES</span></span>

## <span data-ttu-id="a82cf-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a82cf-144">RELATED LINKS</span></span>

[<span data-ttu-id="a82cf-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a82cf-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="a82cf-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a82cf-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="a82cf-147">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="a82cf-147">Azure Batch Cmdlets</span></span>]()

