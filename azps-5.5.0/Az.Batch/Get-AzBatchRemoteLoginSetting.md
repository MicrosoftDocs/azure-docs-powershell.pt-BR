---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117946"
---
# <span data-ttu-id="d3989-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="d3989-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="d3989-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3989-102">SYNOPSIS</span></span>
<span data-ttu-id="d3989-103">Obtém configurações de logon remotas para um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="d3989-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="d3989-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3989-104">SYNTAX</span></span>

### <span data-ttu-id="d3989-105">ID (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3989-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3989-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d3989-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3989-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3989-107">DESCRIPTION</span></span>
<span data-ttu-id="d3989-108">O cmdlet **Get-AzBatchRemoteLoginSetting obtém** configurações de logon remotas para um nó de computação em um pool baseado em infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="d3989-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="d3989-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3989-109">EXAMPLES</span></span>

### <span data-ttu-id="d3989-110">Exemplo 1: Obter configurações de logon remoto para todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="d3989-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="d3989-111">O primeiro comando obtém um contexto de conta em lotes que contém teclas de acesso para sua assinatura usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="d3989-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="d3989-112">O comando armazena o contexto na $Context variável a ser usada no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="d3989-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="d3989-113">O segundo comando obtém cada nó de computação no pool que tem a ID ContosoPool usando **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="d3989-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="d3989-114">O comando passa cada nó do computador para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3989-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3989-115">O comando obtém as configurações de logon remoto para cada nó de computação.</span><span class="sxs-lookup"><span data-stu-id="d3989-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="d3989-116">Exemplo 2: Obter configurações de logon remoto para um nó</span><span class="sxs-lookup"><span data-stu-id="d3989-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="d3989-117">O primeiro comando obtém um contexto de conta em lotes que contém chaves de acesso para sua assinatura e o armazena na variável $Context lote.</span><span class="sxs-lookup"><span data-stu-id="d3989-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="d3989-118">O segundo comando obtém as configurações de logon remoto para o nó de computação que tem a ID especificada no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="d3989-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="d3989-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3989-119">PARAMETERS</span></span>

### <span data-ttu-id="d3989-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3989-120">-BatchContext</span></span>
<span data-ttu-id="d3989-121">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d3989-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3989-122">Para obter um **BatchAccountContext** que contenha teclas de acesso para sua assinatura, use o cmdlet Get-AzBatchAccountKey dados.</span><span class="sxs-lookup"><span data-stu-id="d3989-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="d3989-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d3989-123">-ComputeNode</span></span>
<span data-ttu-id="d3989-124">Especifica um nó de computação, como um objeto **PSComputeNode,** para o qual esse cmdlet obtém configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="d3989-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="d3989-125">Para obter um objeto de nó de computação, use o cmdlet Get-AzBatchComputeNode computador.</span><span class="sxs-lookup"><span data-stu-id="d3989-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="d3989-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d3989-126">-ComputeNodeId</span></span>
<span data-ttu-id="d3989-127">Especifica a ID do nó de computação para o qual obter as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="d3989-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="d3989-128">para as quais este cmdlet obtém configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="d3989-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="d3989-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3989-129">-DefaultProfile</span></span>
<span data-ttu-id="d3989-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3989-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3989-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d3989-131">-PoolId</span></span>
<span data-ttu-id="d3989-132">Especifica a ID do pool que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3989-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="d3989-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3989-133">CommonParameters</span></span>
<span data-ttu-id="d3989-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3989-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3989-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3989-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3989-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="d3989-136">INPUTS</span></span>

### <span data-ttu-id="d3989-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d3989-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d3989-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3989-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d3989-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="d3989-139">OUTPUTS</span></span>

### <span data-ttu-id="d3989-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="d3989-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="d3989-141">Notas</span><span class="sxs-lookup"><span data-stu-id="d3989-141">NOTES</span></span>

## <span data-ttu-id="d3989-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3989-142">RELATED LINKS</span></span>

[<span data-ttu-id="d3989-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3989-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d3989-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d3989-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d3989-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="d3989-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="d3989-146">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="d3989-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
