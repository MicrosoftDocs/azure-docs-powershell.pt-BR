---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281682"
---
# <span data-ttu-id="fbdb8-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="fbdb8-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="fbdb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbdb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdb8-103">Modifica as propriedades de uma conta em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="fbdb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbdb8-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbdb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbdb8-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdb8-106">O cmdlet **set-AzBatchComputeNodeUser** modifica as propriedades de uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="fbdb8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbdb8-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdb8-108">Exemplo 1: atualizar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="fbdb8-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="fbdb8-109">Esse comando modifica a conta de usuário chamada PFuller no nó de computação que tem o ID especificado no pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="fbdb8-110">O comando altera a senha da conta e o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="fbdb8-111">OS</span><span class="sxs-lookup"><span data-stu-id="fbdb8-111">PARAMETERS</span></span>

### <span data-ttu-id="fbdb8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fbdb8-112">-BatchContext</span></span>
<span data-ttu-id="fbdb8-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fbdb8-114">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fbdb8-115">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fbdb8-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fbdb8-117">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fbdb8-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="fbdb8-118">-ComputeNodeId</span></span>
<span data-ttu-id="fbdb8-119">Especifica a ID do nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdb8-120">-DefaultProfile</span></span>
<span data-ttu-id="fbdb8-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbdb8-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fbdb8-122">-ExpiryTime</span></span>
<span data-ttu-id="fbdb8-123">Especifica o tempo de expiração da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbdb8-124">-Name</span></span>
<span data-ttu-id="fbdb8-125">Especifica o nome da conta de usuário que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb8-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="fbdb8-126">-Password</span></span>
<span data-ttu-id="fbdb8-127">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb8-128">-Poolid</span><span class="sxs-lookup"><span data-stu-id="fbdb8-128">-PoolId</span></span>
<span data-ttu-id="fbdb8-129">Especifica a ID do pool que contém o nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdb8-130">CommonParameters</span></span>
<span data-ttu-id="fbdb8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbdb8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdb8-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbdb8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdb8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbdb8-133">INPUTS</span></span>

### <span data-ttu-id="fbdb8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fbdb8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fbdb8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbdb8-135">OUTPUTS</span></span>

### <span data-ttu-id="fbdb8-136">System. void</span><span class="sxs-lookup"><span data-stu-id="fbdb8-136">System.Void</span></span>

## <span data-ttu-id="fbdb8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbdb8-137">NOTES</span></span>

## <span data-ttu-id="fbdb8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbdb8-138">RELATED LINKS</span></span>

[<span data-ttu-id="fbdb8-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fbdb8-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fbdb8-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="fbdb8-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="fbdb8-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="fbdb8-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="fbdb8-142">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="fbdb8-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
