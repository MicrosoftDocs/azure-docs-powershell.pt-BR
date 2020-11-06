---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: c6a89a5c42daea7991711dfa0c96953856949aed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427283"
---
# <span data-ttu-id="8649c-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="8649c-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="8649c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8649c-102">SYNOPSIS</span></span>
<span data-ttu-id="8649c-103">Modifica as propriedades de uma conta em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="8649c-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8649c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8649c-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8649c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8649c-105">DESCRIPTION</span></span>
<span data-ttu-id="8649c-106">O cmdlet **set-AzureBatchComputeNodeUser** modifica as propriedades de uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="8649c-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="8649c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8649c-107">EXAMPLES</span></span>

### <span data-ttu-id="8649c-108">Exemplo 1: atualizar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="8649c-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="8649c-109">Esse comando modifica a conta de usuário chamada PFuller no nó de computação que tem o ID especificado no pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="8649c-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="8649c-110">O comando altera a senha da conta e o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="8649c-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="8649c-111">OS</span><span class="sxs-lookup"><span data-stu-id="8649c-111">PARAMETERS</span></span>

### <span data-ttu-id="8649c-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8649c-112">-BatchContext</span></span>
<span data-ttu-id="8649c-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8649c-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8649c-114">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="8649c-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8649c-115">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="8649c-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8649c-116">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="8649c-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8649c-117">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8649c-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8649c-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="8649c-118">-ComputeNodeId</span></span>
<span data-ttu-id="8649c-119">Especifica a ID do nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8649c-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8649c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8649c-120">-DefaultProfile</span></span>
<span data-ttu-id="8649c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8649c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8649c-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8649c-122">-ExpiryTime</span></span>
<span data-ttu-id="8649c-123">Especifica o tempo de expiração da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="8649c-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="8649c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8649c-124">-Name</span></span>
<span data-ttu-id="8649c-125">Especifica o nome da conta de usuário que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8649c-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8649c-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="8649c-126">-Password</span></span>
<span data-ttu-id="8649c-127">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="8649c-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="8649c-128">-Poolid</span><span class="sxs-lookup"><span data-stu-id="8649c-128">-PoolId</span></span>
<span data-ttu-id="8649c-129">Especifica a ID do pool que contém o nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="8649c-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8649c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8649c-130">CommonParameters</span></span>
<span data-ttu-id="8649c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8649c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8649c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8649c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8649c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8649c-133">INPUTS</span></span>

### <span data-ttu-id="8649c-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8649c-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8649c-135">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8649c-135">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8649c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8649c-136">OUTPUTS</span></span>

### <span data-ttu-id="8649c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="8649c-137">System.Void</span></span>

## <span data-ttu-id="8649c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8649c-138">NOTES</span></span>

## <span data-ttu-id="8649c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8649c-139">RELATED LINKS</span></span>

[<span data-ttu-id="8649c-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8649c-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8649c-141">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="8649c-141">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="8649c-142">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="8649c-142">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="8649c-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="8649c-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


