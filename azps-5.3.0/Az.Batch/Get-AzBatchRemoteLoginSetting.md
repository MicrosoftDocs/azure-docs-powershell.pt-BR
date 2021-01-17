---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430487"
---
# <span data-ttu-id="e9550-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="e9550-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="e9550-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9550-102">SYNOPSIS</span></span>
<span data-ttu-id="e9550-103">Obtém as configurações de logon remoto para um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="e9550-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="e9550-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9550-104">SYNTAX</span></span>

### <span data-ttu-id="e9550-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9550-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9550-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9550-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9550-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9550-107">DESCRIPTION</span></span>
<span data-ttu-id="e9550-108">O cmdlet **Get-AzBatchRemoteLoginSetting** Obtém as configurações de logon remoto para um nó de computação em um pool baseado em infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e9550-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="e9550-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9550-109">EXAMPLES</span></span>

### <span data-ttu-id="e9550-110">Exemplo 1: obter configurações de logon remoto para todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="e9550-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="e9550-111">O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="e9550-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e9550-112">O comando armazena o contexto na variável $Context para usar no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="e9550-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="e9550-113">O segundo comando obtém cada nó de computação no pool que tem o ID ContosoPool usando **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="e9550-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="e9550-114">O comando passa cada nó de computador para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9550-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e9550-115">O comando obtém as configurações de logon remoto para cada nó de computação.</span><span class="sxs-lookup"><span data-stu-id="e9550-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="e9550-116">Exemplo 2: obter configurações de logon remoto para um nó</span><span class="sxs-lookup"><span data-stu-id="e9550-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="e9550-117">O primeiro comando obtém um contexto de conta em lotes que contém as teclas de acesso para a sua assinatura e, em seguida, armazena-a na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="e9550-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="e9550-118">O segundo comando obtém as configurações de logon remoto para o nó de computação com a ID especificada no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="e9550-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="e9550-119">OS</span><span class="sxs-lookup"><span data-stu-id="e9550-119">PARAMETERS</span></span>

### <span data-ttu-id="e9550-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e9550-120">-BatchContext</span></span>
<span data-ttu-id="e9550-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e9550-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e9550-122">Para obter um **BatchAccountContext** que contenha as teclas de acesso para a sua assinatura, use o cmdlet Get-AzBatchAccountKey.</span><span class="sxs-lookup"><span data-stu-id="e9550-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="e9550-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9550-123">-ComputeNode</span></span>
<span data-ttu-id="e9550-124">Especifica um nó de computação, como um objeto **PSComputeNode** , para o qual esse cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="e9550-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="e9550-125">Para obter um objeto do nó de computação, use o cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="e9550-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9550-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e9550-126">-ComputeNodeId</span></span>
<span data-ttu-id="e9550-127">Especifica a ID do nó de computação para a qual obter as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="e9550-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="e9550-128">para o qual este cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="e9550-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9550-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9550-129">-DefaultProfile</span></span>
<span data-ttu-id="e9550-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9550-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9550-131">-Poolid</span><span class="sxs-lookup"><span data-stu-id="e9550-131">-PoolId</span></span>
<span data-ttu-id="e9550-132">Especifica a ID do pool que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e9550-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="e9550-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9550-133">CommonParameters</span></span>
<span data-ttu-id="e9550-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9550-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9550-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9550-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9550-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9550-136">INPUTS</span></span>

### <span data-ttu-id="e9550-137">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9550-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="e9550-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9550-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e9550-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9550-139">OUTPUTS</span></span>

### <span data-ttu-id="e9550-140">Microsoft.Azure.Commands.Batch. Modelos. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="e9550-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="e9550-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9550-141">NOTES</span></span>

## <span data-ttu-id="e9550-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9550-142">RELATED LINKS</span></span>

[<span data-ttu-id="e9550-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e9550-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e9550-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9550-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="e9550-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="e9550-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="e9550-146">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="e9550-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
