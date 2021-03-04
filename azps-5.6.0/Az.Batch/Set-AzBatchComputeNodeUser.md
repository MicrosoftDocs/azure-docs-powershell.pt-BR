---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: c76c10d282d7a2b50cf0b35793cdda080d944740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892230"
---
# <span data-ttu-id="3f6ae-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3f6ae-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="3f6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6ae-103">Modifica as propriedades de uma conta em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="3f6ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3f6ae-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f6ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3f6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3f6ae-106">O cmdlet **Set-AzBatchComputeNodeUser** modifica propriedades de uma conta de usuário em um nó de computação do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="3f6ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3f6ae-108">Exemplo 1: atualizar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="3f6ae-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="3f6ae-109">Este comando modifica a conta de usuário chamada PFuller no nó de computação que tem a ID especificada no pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="3f6ae-110">O comando altera a senha da conta e o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="3f6ae-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-111">PARAMETERS</span></span>

### <span data-ttu-id="3f6ae-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3f6ae-112">-BatchContext</span></span>
<span data-ttu-id="3f6ae-113">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3f6ae-114">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3f6ae-115">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3f6ae-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3f6ae-117">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3f6ae-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-118">-ComputeNodeId</span></span>
<span data-ttu-id="3f6ae-119">Especifica a ID do nó de computação no qual esse cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f6ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6ae-120">-DefaultProfile</span></span>
<span data-ttu-id="3f6ae-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f6ae-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3f6ae-122">-ExpiryTime</span></span>
<span data-ttu-id="3f6ae-123">Especifica o tempo de expiração da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="3f6ae-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6ae-124">-Name</span></span>
<span data-ttu-id="3f6ae-125">Especifica o nome da conta de usuário que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3f6ae-126">-Password</span><span class="sxs-lookup"><span data-stu-id="3f6ae-126">-Password</span></span>
<span data-ttu-id="3f6ae-127">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="3f6ae-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-128">-PoolId</span></span>
<span data-ttu-id="3f6ae-129">Especifica a ID do pool que contém o nó de computação no qual esse cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f6ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6ae-130">CommonParameters</span></span>
<span data-ttu-id="3f6ae-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6ae-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6ae-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-133">INPUTS</span></span>

### <span data-ttu-id="3f6ae-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3f6ae-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3f6ae-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-135">OUTPUTS</span></span>

### <span data-ttu-id="3f6ae-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f6ae-136">System.Void</span></span>

## <span data-ttu-id="3f6ae-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="3f6ae-137">NOTES</span></span>

## <span data-ttu-id="3f6ae-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f6ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f6ae-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f6ae-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3f6ae-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3f6ae-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="3f6ae-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3f6ae-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="3f6ae-142">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="3f6ae-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
