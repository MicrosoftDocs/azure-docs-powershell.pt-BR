---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441410"
---
# <span data-ttu-id="24341-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="24341-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="24341-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24341-102">SYNOPSIS</span></span>
<span data-ttu-id="24341-103">Obtém as configurações de logon remoto para um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="24341-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24341-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24341-104">SYNTAX</span></span>

### <span data-ttu-id="24341-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="24341-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24341-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24341-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24341-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24341-107">DESCRIPTION</span></span>
<span data-ttu-id="24341-108">O cmdlet **Get-AzureBatchRemoteLoginSettings** Obtém as configurações de logon remoto para um nó de computação em um pool baseado em infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="24341-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="24341-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24341-109">EXAMPLES</span></span>

### <span data-ttu-id="24341-110">Exemplo 1: obter configurações de logon remoto para todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="24341-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="24341-111">O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="24341-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="24341-112">O comando armazena o contexto na variável $Context para usar no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="24341-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="24341-113">O segundo comando obtém cada nó de computação no pool que tem o ID ContosoPool usando **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="24341-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="24341-114">O comando passa cada nó de computador para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="24341-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="24341-115">O comando obtém as configurações de logon remoto para cada nó de computação.</span><span class="sxs-lookup"><span data-stu-id="24341-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="24341-116">Exemplo 2: obter configurações de logon remoto para um nó</span><span class="sxs-lookup"><span data-stu-id="24341-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="24341-117">O primeiro comando obtém um contexto de conta em lotes que contém as teclas de acesso para a sua assinatura e, em seguida, armazena-a na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="24341-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="24341-118">O segundo comando obtém as configurações de logon remoto para o nó de computação com a ID especificada no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="24341-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="24341-119">OS</span><span class="sxs-lookup"><span data-stu-id="24341-119">PARAMETERS</span></span>

### <span data-ttu-id="24341-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24341-120">-BatchContext</span></span>
<span data-ttu-id="24341-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="24341-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24341-122">Para obter um **BatchAccountContext** que contenha as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="24341-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="24341-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="24341-123">-ComputeNode</span></span>
<span data-ttu-id="24341-124">Especifica um nó de computação, como um objeto **PSComputeNode** , para o qual esse cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="24341-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="24341-125">Para obter um objeto do nó de computação, use o cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="24341-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="24341-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="24341-126">-ComputeNodeId</span></span>
<span data-ttu-id="24341-127">Especifica a ID do nó de computação para a qual obter as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="24341-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="24341-128">para o qual este cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="24341-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="24341-129">-Poolid</span><span class="sxs-lookup"><span data-stu-id="24341-129">-PoolId</span></span>
<span data-ttu-id="24341-130">Especifica a ID do pool que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="24341-130">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="24341-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24341-131">-DefaultProfile</span></span>
<span data-ttu-id="24341-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24341-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24341-133">CommonParameters</span></span>
<span data-ttu-id="24341-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24341-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24341-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24341-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24341-136">INPUTS</span></span>

### <span data-ttu-id="24341-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24341-137">BatchAccountContext</span></span>
<span data-ttu-id="24341-138">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="24341-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="24341-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="24341-139">PSComputeNode</span></span>
<span data-ttu-id="24341-140">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="24341-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="24341-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24341-141">OUTPUTS</span></span>

### <span data-ttu-id="24341-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="24341-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="24341-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24341-143">NOTES</span></span>

## <span data-ttu-id="24341-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24341-144">RELATED LINKS</span></span>

[<span data-ttu-id="24341-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="24341-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="24341-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="24341-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="24341-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="24341-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="24341-148">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="24341-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


