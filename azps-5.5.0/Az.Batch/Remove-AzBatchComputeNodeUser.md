---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115968"
---
# <span data-ttu-id="88546-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88546-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="88546-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88546-102">SYNOPSIS</span></span>
<span data-ttu-id="88546-103">Exclui uma conta de usuário de um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="88546-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="88546-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88546-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88546-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="88546-105">DESCRIPTION</span></span>
<span data-ttu-id="88546-106">O cmdlet **Remove-AzBatchComputeNodeUser** exclui uma conta de usuário de um nó de computação do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="88546-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="88546-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88546-107">EXAMPLES</span></span>

### <span data-ttu-id="88546-108">Exemplo 1: Excluir um usuário de um nó de computação sem confirmação</span><span class="sxs-lookup"><span data-stu-id="88546-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="88546-109">Esse comando exclui o usuário chamado Usuário14 do nó de computação chamado ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="88546-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="88546-110">O nó de computação está no pool chamado Pool01.</span><span class="sxs-lookup"><span data-stu-id="88546-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="88546-111">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="88546-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="88546-112">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="88546-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="88546-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88546-113">PARAMETERS</span></span>

### <span data-ttu-id="88546-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88546-114">-BatchContext</span></span>
<span data-ttu-id="88546-115">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="88546-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88546-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="88546-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88546-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="88546-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88546-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="88546-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88546-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88546-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88546-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="88546-120">-ComputeNodeId</span></span>
<span data-ttu-id="88546-121">Especifica a ID do nó de computação no qual esse cmdlet exclui a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="88546-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="88546-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88546-122">-DefaultProfile</span></span>
<span data-ttu-id="88546-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="88546-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88546-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="88546-124">-Name</span></span>
<span data-ttu-id="88546-125">Especifica o nome da conta de usuário a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="88546-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="88546-126">Não é possível especificar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="88546-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="88546-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88546-127">-PoolId</span></span>
<span data-ttu-id="88546-128">Especifica a ID do pool que contém o nó de computação no qual excluir a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="88546-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="88546-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88546-129">-Confirm</span></span>
<span data-ttu-id="88546-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88546-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88546-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88546-131">-WhatIf</span></span>
<span data-ttu-id="88546-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88546-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88546-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88546-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88546-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88546-134">CommonParameters</span></span>
<span data-ttu-id="88546-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88546-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88546-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88546-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88546-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="88546-137">INPUTS</span></span>

### <span data-ttu-id="88546-138">System.String</span><span class="sxs-lookup"><span data-stu-id="88546-138">System.String</span></span>

### <span data-ttu-id="88546-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88546-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88546-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="88546-140">OUTPUTS</span></span>

### <span data-ttu-id="88546-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="88546-141">System.Void</span></span>

## <span data-ttu-id="88546-142">Notas</span><span class="sxs-lookup"><span data-stu-id="88546-142">NOTES</span></span>

## <span data-ttu-id="88546-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88546-143">RELATED LINKS</span></span>

[<span data-ttu-id="88546-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88546-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88546-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88546-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88546-146">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="88546-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
