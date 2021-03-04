---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 4b6d508dde18544c00ac3539921e83bd235e6fef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891519"
---
# <span data-ttu-id="6aa59-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="6aa59-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="6aa59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa59-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa59-103">Exclui uma conta de usuário de um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="6aa59-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="6aa59-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6aa59-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6aa59-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6aa59-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa59-106">O cmdlet **Remove-AzBatchComputeNodeUser** exclui uma conta de usuário de um nó de computação do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6aa59-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="6aa59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6aa59-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa59-108">Exemplo 1: Excluir um usuário de um nó de computação sem confirmação</span><span class="sxs-lookup"><span data-stu-id="6aa59-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="6aa59-109">Este comando exclui o usuário chamado User14 do nó de computação chamado ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="6aa59-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="6aa59-110">O nó de computação está no pool chamado Pool01.</span><span class="sxs-lookup"><span data-stu-id="6aa59-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="6aa59-111">Este comando especifica o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="6aa59-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6aa59-112">Portanto, o comando não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6aa59-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6aa59-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6aa59-113">PARAMETERS</span></span>

### <span data-ttu-id="6aa59-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6aa59-114">-BatchContext</span></span>
<span data-ttu-id="6aa59-115">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="6aa59-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6aa59-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="6aa59-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6aa59-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6aa59-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6aa59-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6aa59-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6aa59-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6aa59-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6aa59-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="6aa59-120">-ComputeNodeId</span></span>
<span data-ttu-id="6aa59-121">Especifica a ID do nó de computação no qual esse cmdlet exclui a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="6aa59-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa59-122">-DefaultProfile</span></span>
<span data-ttu-id="6aa59-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6aa59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa59-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6aa59-124">-Name</span></span>
<span data-ttu-id="6aa59-125">Especifica o nome da conta de usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6aa59-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="6aa59-126">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="6aa59-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa59-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6aa59-127">-PoolId</span></span>
<span data-ttu-id="6aa59-128">Especifica a ID do pool que contém o nó de computação no qual excluir a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="6aa59-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa59-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aa59-129">-Confirm</span></span>
<span data-ttu-id="6aa59-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa59-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa59-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa59-131">-WhatIf</span></span>
<span data-ttu-id="6aa59-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6aa59-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aa59-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6aa59-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa59-134">CommonParameters</span></span>
<span data-ttu-id="6aa59-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa59-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aa59-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa59-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aa59-137">INPUTS</span></span>

### <span data-ttu-id="6aa59-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6aa59-138">System.String</span></span>

### <span data-ttu-id="6aa59-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6aa59-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6aa59-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6aa59-140">OUTPUTS</span></span>

### <span data-ttu-id="6aa59-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="6aa59-141">System.Void</span></span>

## <span data-ttu-id="6aa59-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6aa59-142">NOTES</span></span>

## <span data-ttu-id="6aa59-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6aa59-143">RELATED LINKS</span></span>

[<span data-ttu-id="6aa59-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="6aa59-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="6aa59-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6aa59-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6aa59-146">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="6aa59-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
