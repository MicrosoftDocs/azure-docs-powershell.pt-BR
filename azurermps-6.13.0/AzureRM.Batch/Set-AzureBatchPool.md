---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: c0f1dc4972e3b71dce74bffb7a72e782774a2734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426429"
---
# <span data-ttu-id="280c2-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="280c2-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="280c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="280c2-102">SYNOPSIS</span></span>
<span data-ttu-id="280c2-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="280c2-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="280c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="280c2-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="280c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="280c2-105">DESCRIPTION</span></span>
<span data-ttu-id="280c2-106">O cmdlet **set-AzureBatchPool** atualiza as propriedades de um pool no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="280c2-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="280c2-107">Use o cmdlet Get-AzureBatchPool para obter um objeto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="280c2-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="280c2-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="280c2-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="280c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="280c2-109">EXAMPLES</span></span>

### <span data-ttu-id="280c2-110">Exemplo 1: atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="280c2-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="280c2-111">O primeiro comando obtém um pool usando **Get-AzureBatchPool** e, em seguida, armazena-o na variável $pool.</span><span class="sxs-lookup"><span data-stu-id="280c2-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="280c2-112">Os próximos três comandos modificam a especificação Start Task no objeto $Pool.</span><span class="sxs-lookup"><span data-stu-id="280c2-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="280c2-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Pool.</span><span class="sxs-lookup"><span data-stu-id="280c2-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="280c2-114">OS</span><span class="sxs-lookup"><span data-stu-id="280c2-114">PARAMETERS</span></span>

### <span data-ttu-id="280c2-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="280c2-115">-BatchContext</span></span>
<span data-ttu-id="280c2-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="280c2-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="280c2-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="280c2-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="280c2-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="280c2-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="280c2-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="280c2-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="280c2-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="280c2-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="280c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280c2-121">-DefaultProfile</span></span>
<span data-ttu-id="280c2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="280c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="280c2-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="280c2-123">-Pool</span></span>
<span data-ttu-id="280c2-124">Especifica o **PSCloudPool** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="280c2-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="280c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280c2-125">CommonParameters</span></span>
<span data-ttu-id="280c2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="280c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280c2-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="280c2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280c2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="280c2-128">INPUTS</span></span>

### <span data-ttu-id="280c2-129">Microsoft.Azure.Commands.Batch. Modelos. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="280c2-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>
<span data-ttu-id="280c2-130">Parâmetros: pool (ByValue)</span><span class="sxs-lookup"><span data-stu-id="280c2-130">Parameters: Pool (ByValue)</span></span>

### <span data-ttu-id="280c2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="280c2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="280c2-132">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="280c2-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="280c2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="280c2-133">OUTPUTS</span></span>

### <span data-ttu-id="280c2-134">System. void</span><span class="sxs-lookup"><span data-stu-id="280c2-134">System.Void</span></span>

## <span data-ttu-id="280c2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="280c2-135">NOTES</span></span>

## <span data-ttu-id="280c2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="280c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="280c2-137">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="280c2-137">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="280c2-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="280c2-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="280c2-139">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="280c2-139">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="280c2-140">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="280c2-140">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="280c2-141">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="280c2-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


