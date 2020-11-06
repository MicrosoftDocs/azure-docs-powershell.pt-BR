---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: 9f9b2a406d5fc728e9297fc4093a60b3f6ec4bf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432944"
---
# <span data-ttu-id="0d42a-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0d42a-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="0d42a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d42a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d42a-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="0d42a-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d42a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d42a-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d42a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d42a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d42a-106">O cmdlet **set-AzureBatchPool** atualiza as propriedades de um pool no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d42a-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="0d42a-107">Use o cmdlet Get-AzureBatchPool para obter um objeto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="0d42a-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="0d42a-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="0d42a-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="0d42a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d42a-109">EXAMPLES</span></span>

### <span data-ttu-id="0d42a-110">Exemplo 1: atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="0d42a-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="0d42a-111">O primeiro comando obtém um pool usando **Get-AzureBatchPool** e, em seguida, armazena-o na variável $pool.</span><span class="sxs-lookup"><span data-stu-id="0d42a-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="0d42a-112">Os próximos três comandos modificam a especificação Start Task no objeto $Pool.</span><span class="sxs-lookup"><span data-stu-id="0d42a-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="0d42a-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Pool.</span><span class="sxs-lookup"><span data-stu-id="0d42a-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="0d42a-114">OS</span><span class="sxs-lookup"><span data-stu-id="0d42a-114">PARAMETERS</span></span>

### <span data-ttu-id="0d42a-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0d42a-115">-BatchContext</span></span>
<span data-ttu-id="0d42a-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="0d42a-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d42a-117">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="0d42a-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0d42a-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="0d42a-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0d42a-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0d42a-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0d42a-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0d42a-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0d42a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d42a-121">-DefaultProfile</span></span>
<span data-ttu-id="0d42a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d42a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d42a-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="0d42a-123">-Pool</span></span>
<span data-ttu-id="0d42a-124">Especifica o **PSCloudPool** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="0d42a-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d42a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d42a-125">CommonParameters</span></span>
<span data-ttu-id="0d42a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d42a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d42a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d42a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d42a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d42a-128">INPUTS</span></span>

### <span data-ttu-id="0d42a-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d42a-129">BatchAccountContext</span></span>
<span data-ttu-id="0d42a-130">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0d42a-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0d42a-131">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="0d42a-131">PSCloudPool</span></span>
<span data-ttu-id="0d42a-132">O parâmetro ' Pool ' aceita o valor do tipo ' PSCloudPool ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="0d42a-132">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="0d42a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d42a-133">OUTPUTS</span></span>

## <span data-ttu-id="0d42a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d42a-134">NOTES</span></span>

## <span data-ttu-id="0d42a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d42a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d42a-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0d42a-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="0d42a-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0d42a-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0d42a-138">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0d42a-138">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="0d42a-139">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="0d42a-139">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="0d42a-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="0d42a-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


