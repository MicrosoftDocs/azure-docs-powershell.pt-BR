---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 636ceb216c7bb6aec2016bdd047a26f707108c9b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956005"
---
# <span data-ttu-id="35474-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35474-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="35474-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35474-102">SYNOPSIS</span></span>
<span data-ttu-id="35474-103">Modifica as propriedades de uma conta em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="35474-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="35474-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35474-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35474-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35474-105">DESCRIPTION</span></span>
<span data-ttu-id="35474-106">O cmdlet **set-AzBatchComputeNodeUser** modifica as propriedades de uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="35474-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="35474-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35474-107">EXAMPLES</span></span>

### <span data-ttu-id="35474-108">Exemplo 1: atualizar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="35474-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="35474-109">Esse comando modifica a conta de usuário chamada PFuller no nó de computação que tem o ID especificado no pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="35474-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="35474-110">O comando altera a senha da conta e o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="35474-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="35474-111">OS</span><span class="sxs-lookup"><span data-stu-id="35474-111">PARAMETERS</span></span>

### <span data-ttu-id="35474-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="35474-112">-BatchContext</span></span>
<span data-ttu-id="35474-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="35474-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="35474-114">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="35474-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="35474-115">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="35474-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="35474-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="35474-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="35474-117">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="35474-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="35474-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="35474-118">-ComputeNodeId</span></span>
<span data-ttu-id="35474-119">Especifica a ID do nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="35474-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="35474-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35474-120">-DefaultProfile</span></span>
<span data-ttu-id="35474-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35474-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35474-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="35474-122">-ExpiryTime</span></span>
<span data-ttu-id="35474-123">Especifica o tempo de expiração da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="35474-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="35474-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="35474-124">-Name</span></span>
<span data-ttu-id="35474-125">Especifica o nome da conta de usuário que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="35474-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35474-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="35474-126">-Password</span></span>
<span data-ttu-id="35474-127">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="35474-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="35474-128">-Poolid</span><span class="sxs-lookup"><span data-stu-id="35474-128">-PoolId</span></span>
<span data-ttu-id="35474-129">Especifica a ID do pool que contém o nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="35474-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="35474-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35474-130">CommonParameters</span></span>
<span data-ttu-id="35474-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35474-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35474-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35474-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35474-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35474-133">INPUTS</span></span>

### <span data-ttu-id="35474-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="35474-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="35474-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35474-135">OUTPUTS</span></span>

### <span data-ttu-id="35474-136">System. void</span><span class="sxs-lookup"><span data-stu-id="35474-136">System.Void</span></span>

## <span data-ttu-id="35474-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35474-137">NOTES</span></span>

## <span data-ttu-id="35474-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35474-138">RELATED LINKS</span></span>

[<span data-ttu-id="35474-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="35474-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="35474-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35474-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="35474-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35474-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="35474-142">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="35474-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
