---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: e871b32840db3802fc2bb2fb87871e37cf95dcfe
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601845"
---
# <span data-ttu-id="ecb4e-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecb4e-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="ecb4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb4e-103">Remove nós de computação de um pool.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="ecb4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecb4e-104">SYNTAX</span></span>

### <span data-ttu-id="ecb4e-105">ID (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecb4e-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb4e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb4e-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecb4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecb4e-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb4e-108">O cmdlet **Remove-AzBatchComputeNode** remove os nós de computação em lotes do Azure de um pool.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="ecb4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecb4e-109">EXAMPLES</span></span>

### <span data-ttu-id="ecb4e-110">Exemplo 1: remover um nó de computação</span><span class="sxs-lookup"><span data-stu-id="ecb4e-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="ecb4e-111">Esse comando Remove o nó de computação com a ID especificada do pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="ecb4e-112">O comando especifica a opção terminar a desalocação.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="ecb4e-113">O tempo limite de redimensionamento é de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="ecb4e-114">Exemplo 2: remover um nó de computação usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="ecb4e-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="ecb4e-115">Esse comando obtém o nó de computação com a ID especificada do pool com a ID Pool07 usando o cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="ecb4e-116">O comando passa esse nó para o cmdlet atual usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="ecb4e-117">O cmdlet atual remove o nó de computação.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="ecb4e-118">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ecb4e-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ecb4e-119">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ecb4e-120">Exemplo 3: remover vários nós</span><span class="sxs-lookup"><span data-stu-id="ecb4e-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="ecb4e-121">Esse comando remove dois nós de computação do pool que tem a ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="ecb4e-122">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ecb4e-123">OS</span><span class="sxs-lookup"><span data-stu-id="ecb4e-123">PARAMETERS</span></span>

### <span data-ttu-id="ecb4e-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ecb4e-124">-BatchContext</span></span>
<span data-ttu-id="ecb4e-125">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ecb4e-126">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ecb4e-127">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ecb4e-128">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ecb4e-129">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ecb4e-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecb4e-130">-ComputeNode</span></span>
<span data-ttu-id="ecb4e-131">Especifica o objeto **PSComputeNode** que representa o nó de computação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ecb4e-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ecb4e-132">-DeallocationOption</span></span>
<span data-ttu-id="ecb4e-133">Especifica uma opção de desalocação para a operação de remoção que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="ecb4e-134">O valor padrão é ReQueue.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb4e-135">-DefaultProfile</span></span>
<span data-ttu-id="ecb4e-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb4e-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ecb4e-137">-Force</span></span>
<span data-ttu-id="ecb4e-138">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-139">-IDs</span><span class="sxs-lookup"><span data-stu-id="ecb4e-139">-Ids</span></span>
<span data-ttu-id="ecb4e-140">Especifica uma matriz de IDs de nós de computadores que este cmdlet Remove do pool.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-141">-Poolid</span><span class="sxs-lookup"><span data-stu-id="ecb4e-141">-PoolId</span></span>
<span data-ttu-id="ecb4e-142">Especifica a ID do pool que contém os nós de computadores que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ecb4e-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="ecb4e-143">-ResizeTimeout</span></span>
<span data-ttu-id="ecb4e-144">Especifica o intervalo de tempo limite para a remoção dos nós de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="ecb4e-145">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="ecb4e-146">O valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecb4e-147">-Confirm</span></span>
<span data-ttu-id="ecb4e-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb4e-149">-WhatIf</span></span>
<span data-ttu-id="ecb4e-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb4e-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb4e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb4e-152">CommonParameters</span></span>
<span data-ttu-id="ecb4e-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb4e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb4e-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb4e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb4e-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecb4e-155">INPUTS</span></span>

### <span data-ttu-id="ecb4e-156">Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecb4e-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ecb4e-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ecb4e-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ecb4e-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecb4e-158">OUTPUTS</span></span>

### <span data-ttu-id="ecb4e-159">System. void</span><span class="sxs-lookup"><span data-stu-id="ecb4e-159">System.Void</span></span>

## <span data-ttu-id="ecb4e-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecb4e-160">NOTES</span></span>

## <span data-ttu-id="ecb4e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecb4e-161">RELATED LINKS</span></span>

[<span data-ttu-id="ecb4e-162">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ecb4e-162">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ecb4e-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecb4e-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ecb4e-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecb4e-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


