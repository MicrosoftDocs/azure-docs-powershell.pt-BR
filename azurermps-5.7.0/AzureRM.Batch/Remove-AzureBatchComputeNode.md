---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 6350505efe3f3e7c571fee6940cf678706c4fc7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610125"
---
# <span data-ttu-id="91085-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="91085-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="91085-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91085-102">SYNOPSIS</span></span>
<span data-ttu-id="91085-103">Remove nós de computação de um pool.</span><span class="sxs-lookup"><span data-stu-id="91085-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91085-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91085-104">SYNTAX</span></span>

### <span data-ttu-id="91085-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="91085-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91085-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="91085-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91085-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91085-107">DESCRIPTION</span></span>
<span data-ttu-id="91085-108">O cmdlet **Remove-AzureBatchComputeNode** remove os nós de computação em lotes do Azure de um pool.</span><span class="sxs-lookup"><span data-stu-id="91085-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="91085-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91085-109">EXAMPLES</span></span>

### <span data-ttu-id="91085-110">Exemplo 1: remover um nó de computação</span><span class="sxs-lookup"><span data-stu-id="91085-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="91085-111">Esse comando Remove o nó de computação com a ID especificada do pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="91085-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="91085-112">O comando especifica a opção terminar a desalocação.</span><span class="sxs-lookup"><span data-stu-id="91085-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="91085-113">O tempo limite de redimensionamento é de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="91085-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="91085-114">Exemplo 2: remover um nó de computação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="91085-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="91085-115">Esse comando obtém o nó de computação com a ID especificada do pool com a ID Pool07 usando o cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="91085-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="91085-116">O comando passa esse nó para o cmdlet atual usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="91085-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="91085-117">O cmdlet atual remove o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="91085-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="91085-118">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="91085-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="91085-119">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="91085-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="91085-120">Exemplo 3: remover vários nós</span><span class="sxs-lookup"><span data-stu-id="91085-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="91085-121">Esse comando remove dois nós de computação do pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="91085-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="91085-122">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="91085-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="91085-123">OS</span><span class="sxs-lookup"><span data-stu-id="91085-123">PARAMETERS</span></span>

### <span data-ttu-id="91085-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="91085-124">-BatchContext</span></span>
<span data-ttu-id="91085-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="91085-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="91085-126">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="91085-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="91085-127">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="91085-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="91085-128">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="91085-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="91085-129">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="91085-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="91085-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="91085-130">-ComputeNode</span></span>
<span data-ttu-id="91085-131">Especifica o objeto **PSComputeNode** que representa o nó de computação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="91085-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91085-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="91085-132">-DeallocationOption</span></span>
<span data-ttu-id="91085-133">Especifica uma opção de desalocação para a operação de remoção que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="91085-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="91085-134">O valor padrão é ReQueue.</span><span class="sxs-lookup"><span data-stu-id="91085-134">The default value is Requeue.</span></span>

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91085-135">-DefaultProfile</span></span>
<span data-ttu-id="91085-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91085-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91085-137">-Force</span><span class="sxs-lookup"><span data-stu-id="91085-137">-Force</span></span>
<span data-ttu-id="91085-138">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="91085-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-139">-IDs</span><span class="sxs-lookup"><span data-stu-id="91085-139">-Ids</span></span>
<span data-ttu-id="91085-140">Especifica uma matriz de IDs de nós de computadores que este cmdlet Remove do pool.</span><span class="sxs-lookup"><span data-stu-id="91085-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-141">-Poolid</span><span class="sxs-lookup"><span data-stu-id="91085-141">-PoolId</span></span>
<span data-ttu-id="91085-142">Especifica a ID do pool que contém os nós de computadores que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="91085-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91085-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="91085-143">-ResizeTimeout</span></span>
<span data-ttu-id="91085-144">Especifica o intervalo de tempo limite para a remoção dos nós de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="91085-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="91085-145">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="91085-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="91085-146">O valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="91085-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91085-147">-Confirm</span></span>
<span data-ttu-id="91085-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91085-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91085-149">-WhatIf</span></span>
<span data-ttu-id="91085-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91085-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91085-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91085-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91085-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91085-152">CommonParameters</span></span>
<span data-ttu-id="91085-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91085-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91085-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91085-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91085-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91085-155">INPUTS</span></span>

### <span data-ttu-id="91085-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="91085-156">BatchAccountContext</span></span>
<span data-ttu-id="91085-157">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="91085-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="91085-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="91085-158">PSComputeNode</span></span>
<span data-ttu-id="91085-159">O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="91085-159">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="91085-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91085-160">OUTPUTS</span></span>

## <span data-ttu-id="91085-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91085-161">NOTES</span></span>

## <span data-ttu-id="91085-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91085-162">RELATED LINKS</span></span>

[<span data-ttu-id="91085-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="91085-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="91085-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="91085-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="91085-165">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="91085-165">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


