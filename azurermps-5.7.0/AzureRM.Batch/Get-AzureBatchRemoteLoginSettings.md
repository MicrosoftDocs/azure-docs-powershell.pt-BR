---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 01ded3d4e9d77edac39e7c632f46d6e7ecf9eeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427691"
---
# <span data-ttu-id="f3c1f-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="f3c1f-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="f3c1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c1f-103">Obtém as configurações de logon remoto para um nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3c1f-104">SYNTAX</span></span>

### <span data-ttu-id="f3c1f-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3c1f-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c1f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c1f-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c1f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3c1f-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c1f-108">O cmdlet **Get-AzureBatchRemoteLoginSettings** Obtém as configurações de logon remoto para um nó de computação em um pool baseado em infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="f3c1f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3c1f-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c1f-110">Exemplo 1: obter configurações de logon remoto para todos os nós em um pool</span><span class="sxs-lookup"><span data-stu-id="f3c1f-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="f3c1f-111">O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="f3c1f-112">O comando armazena o contexto na variável $Context para usar no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="f3c1f-113">O segundo comando obtém cada nó de computação no pool que tem o ID ContosoPool usando **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="f3c1f-114">O comando passa cada nó de computador para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3c1f-115">O comando obtém as configurações de logon remoto para cada nó de computação.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="f3c1f-116">Exemplo 2: obter configurações de logon remoto para um nó</span><span class="sxs-lookup"><span data-stu-id="f3c1f-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="f3c1f-117">O primeiro comando obtém um contexto de conta em lotes que contém as teclas de acesso para a sua assinatura e, em seguida, armazena-a na variável $Context.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="f3c1f-118">O segundo comando obtém as configurações de logon remoto para o nó de computação com a ID especificada no pool que tem a ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="f3c1f-119">OS</span><span class="sxs-lookup"><span data-stu-id="f3c1f-119">PARAMETERS</span></span>

### <span data-ttu-id="f3c1f-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f3c1f-120">-BatchContext</span></span>
<span data-ttu-id="f3c1f-121">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f3c1f-122">Para obter um **BatchAccountContext** que contenha as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c1f-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="f3c1f-123">-ComputeNode</span></span>
<span data-ttu-id="f3c1f-124">Especifica um nó de computação, como um objeto **PSComputeNode** , para o qual esse cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="f3c1f-125">Para obter um objeto do nó de computação, use o cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c1f-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="f3c1f-126">-ComputeNodeId</span></span>
<span data-ttu-id="f3c1f-127">Especifica a ID do nó de computação para a qual obter as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="f3c1f-128">para o qual este cmdlet obtém as configurações de logon remoto.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c1f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c1f-129">-DefaultProfile</span></span>
<span data-ttu-id="f3c1f-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c1f-131">-Poolid</span><span class="sxs-lookup"><span data-stu-id="f3c1f-131">-PoolId</span></span>
<span data-ttu-id="f3c1f-132">Especifica a ID do pool que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c1f-133">CommonParameters</span></span>
<span data-ttu-id="f3c1f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c1f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c1f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c1f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3c1f-136">INPUTS</span></span>

### <span data-ttu-id="f3c1f-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f3c1f-137">BatchAccountContext</span></span>
<span data-ttu-id="f3c1f-138">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f3c1f-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f3c1f-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f3c1f-139">PSComputeNode</span></span>
<span data-ttu-id="f3c1f-140">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f3c1f-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="f3c1f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3c1f-141">OUTPUTS</span></span>

### <span data-ttu-id="f3c1f-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="f3c1f-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="f3c1f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3c1f-143">NOTES</span></span>

## <span data-ttu-id="f3c1f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3c1f-144">RELATED LINKS</span></span>

[<span data-ttu-id="f3c1f-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f3c1f-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f3c1f-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f3c1f-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="f3c1f-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="f3c1f-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="f3c1f-148">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="f3c1f-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


