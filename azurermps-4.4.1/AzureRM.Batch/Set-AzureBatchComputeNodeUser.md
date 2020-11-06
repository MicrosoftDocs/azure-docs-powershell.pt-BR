---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431136"
---
# <span data-ttu-id="4aba4-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4aba4-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="4aba4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4aba4-102">SYNOPSIS</span></span>
<span data-ttu-id="4aba4-103">Modifica as propriedades de uma conta em um nó de computação em lotes.</span><span class="sxs-lookup"><span data-stu-id="4aba4-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aba4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aba4-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aba4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4aba4-105">DESCRIPTION</span></span>
<span data-ttu-id="4aba4-106">O cmdlet **set-AzureBatchComputeNodeUser** modifica as propriedades de uma conta de usuário em um nó de computação em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="4aba4-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="4aba4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4aba4-107">EXAMPLES</span></span>

### <span data-ttu-id="4aba4-108">Exemplo 1: atualizar uma conta de usuário</span><span class="sxs-lookup"><span data-stu-id="4aba4-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="4aba4-109">Esse comando modifica a conta de usuário chamada PFuller no nó de computação que tem o ID especificado no pool chamado ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="4aba4-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="4aba4-110">O comando altera a senha da conta e o tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="4aba4-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="4aba4-111">OS</span><span class="sxs-lookup"><span data-stu-id="4aba4-111">PARAMETERS</span></span>

### <span data-ttu-id="4aba4-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4aba4-112">-BatchContext</span></span>
<span data-ttu-id="4aba4-113">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="4aba4-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4aba4-114">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="4aba4-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4aba4-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="4aba4-115">-ComputeNodeId</span></span>
<span data-ttu-id="4aba4-116">Especifica a ID do nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="4aba4-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4aba4-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4aba4-117">-ExpiryTime</span></span>
<span data-ttu-id="4aba4-118">Especifica o tempo de expiração da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="4aba4-118">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="4aba4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4aba4-119">-Name</span></span>
<span data-ttu-id="4aba4-120">Especifica o nome da conta de usuário que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4aba4-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4aba4-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="4aba4-121">-Password</span></span>
<span data-ttu-id="4aba4-122">Especifica a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="4aba4-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aba4-123">-Poolid</span><span class="sxs-lookup"><span data-stu-id="4aba4-123">-PoolId</span></span>
<span data-ttu-id="4aba4-124">Especifica a ID do pool que contém o nó de computação em que esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="4aba4-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4aba4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aba4-125">-DefaultProfile</span></span>
<span data-ttu-id="4aba4-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4aba4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aba4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aba4-127">CommonParameters</span></span>
<span data-ttu-id="4aba4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aba4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aba4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aba4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aba4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4aba4-130">INPUTS</span></span>

### <span data-ttu-id="4aba4-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4aba4-131">BatchAccountContext</span></span>
<span data-ttu-id="4aba4-132">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4aba4-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4aba4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4aba4-133">OUTPUTS</span></span>

## <span data-ttu-id="4aba4-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4aba4-134">NOTES</span></span>

## <span data-ttu-id="4aba4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4aba4-135">RELATED LINKS</span></span>

[<span data-ttu-id="4aba4-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4aba4-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4aba4-137">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4aba4-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="4aba4-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="4aba4-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="4aba4-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="4aba4-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


