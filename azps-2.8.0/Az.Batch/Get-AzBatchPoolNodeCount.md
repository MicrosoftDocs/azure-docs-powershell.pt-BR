---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 0390e6f156e305c3ba5f34d78dcf33520098bee3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597700"
---
# <span data-ttu-id="42d8f-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="42d8f-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="42d8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="42d8f-103">Obtém o número do nó do lote por estado do nó agrupado por ID do pool.</span><span class="sxs-lookup"><span data-stu-id="42d8f-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="42d8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42d8f-104">SYNTAX</span></span>

### <span data-ttu-id="42d8f-105">AzureBatchPoolNodeCounts (padrão)</span><span class="sxs-lookup"><span data-stu-id="42d8f-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42d8f-106">Poolid</span><span class="sxs-lookup"><span data-stu-id="42d8f-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d8f-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="42d8f-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d8f-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="42d8f-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d8f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42d8f-109">DESCRIPTION</span></span>
<span data-ttu-id="42d8f-110">O cmdlet Get-AzBatchPoolNodeCount permite que os clientes obtenham contagens de nós back por estado de nó agrupadas por pool.</span><span class="sxs-lookup"><span data-stu-id="42d8f-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="42d8f-111">Estados de nó possíveis são: Creating, Idle, leavingPool, offline, preempção, reinicialização, recriação de imagens, execução, início, startTaskFailed, desconhecido, inutilizável e waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="42d8f-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="42d8f-112">O cmdlet usa poolid ou parâmetro de pool para filtrar somente o pool com ID de pool especificado.</span><span class="sxs-lookup"><span data-stu-id="42d8f-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="42d8f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42d8f-113">EXAMPLES</span></span>

### <span data-ttu-id="42d8f-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42d8f-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="42d8f-115">Listar contagens de nó por estado do nó para pools em contexto atual da conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="42d8f-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="42d8f-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="42d8f-116">Example 2</span></span>

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

<span data-ttu-id="42d8f-117">Mostrar contagens de nós por estado do nó para um pool com ID de pool específico.</span><span class="sxs-lookup"><span data-stu-id="42d8f-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="42d8f-118">OS</span><span class="sxs-lookup"><span data-stu-id="42d8f-118">PARAMETERS</span></span>

### <span data-ttu-id="42d8f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="42d8f-119">-BatchContext</span></span>
<span data-ttu-id="42d8f-120">A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="42d8f-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="42d8f-121">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="42d8f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="42d8f-122">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="42d8f-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="42d8f-123">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="42d8f-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="42d8f-124">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="42d8f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="42d8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d8f-125">-DefaultProfile</span></span>
<span data-ttu-id="42d8f-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42d8f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d8f-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="42d8f-127">-MaxCount</span></span>
<span data-ttu-id="42d8f-128">Especifica o número máximo de pools a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="42d8f-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="42d8f-129">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="42d8f-129">The default value is 10.</span></span>

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

### <span data-ttu-id="42d8f-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="42d8f-130">-Pool</span></span>
<span data-ttu-id="42d8f-131">Especifica o **PSCloudPool** para o qual obter contagens de nós.</span><span class="sxs-lookup"><span data-stu-id="42d8f-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="42d8f-132">-Poolid</span><span class="sxs-lookup"><span data-stu-id="42d8f-132">-PoolId</span></span>
<span data-ttu-id="42d8f-133">A ID do pool para o qual obter contagens de nós.</span><span class="sxs-lookup"><span data-stu-id="42d8f-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="42d8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d8f-134">CommonParameters</span></span>
<span data-ttu-id="42d8f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d8f-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d8f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d8f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42d8f-137">INPUTS</span></span>

### <span data-ttu-id="42d8f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="42d8f-138">System.String</span></span>

### <span data-ttu-id="42d8f-139">Microsoft.Azure.Commands.Batch. Modelos. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="42d8f-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="42d8f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="42d8f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="42d8f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42d8f-141">OUTPUTS</span></span>

### <span data-ttu-id="42d8f-142">Microsoft.Azure.Commands.Batch. Modelos. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="42d8f-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="42d8f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42d8f-143">NOTES</span></span>

## <span data-ttu-id="42d8f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42d8f-144">RELATED LINKS</span></span>

[<span data-ttu-id="42d8f-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="42d8f-145">Get-AzBatchAccountKeys</span></span>]()

[<span data-ttu-id="42d8f-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="42d8f-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="42d8f-147">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="42d8f-147">Azure Batch Cmdlets</span></span>]()

