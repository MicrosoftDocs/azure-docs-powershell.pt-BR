---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955117"
---
# <span data-ttu-id="150e8-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="150e8-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="150e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="150e8-102">SYNOPSIS</span></span>
<span data-ttu-id="150e8-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="150e8-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="150e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="150e8-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="150e8-105">DESCRIPTION</span></span>
<span data-ttu-id="150e8-106">O cmdlet **set-AzBatchPool** atualiza as propriedades de um pool no serviço de lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="150e8-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="150e8-107">Use o cmdlet Get-AzBatchPool para obter um objeto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="150e8-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="150e8-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para confirmar suas alterações no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="150e8-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="150e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="150e8-109">EXAMPLES</span></span>

### <span data-ttu-id="150e8-110">Exemplo 1: atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="150e8-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="150e8-111">O primeiro comando obtém um pool usando **Get-AzBatchPool** e, em seguida, armazena-o na variável $pool.</span><span class="sxs-lookup"><span data-stu-id="150e8-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="150e8-112">Os próximos três comandos modificam a especificação Start Task no objeto $Pool.</span><span class="sxs-lookup"><span data-stu-id="150e8-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="150e8-113">O comando final atualiza o serviço em lotes para corresponder ao objeto local em $Pool.</span><span class="sxs-lookup"><span data-stu-id="150e8-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="150e8-114">OS</span><span class="sxs-lookup"><span data-stu-id="150e8-114">PARAMETERS</span></span>

### <span data-ttu-id="150e8-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="150e8-115">-BatchContext</span></span>
<span data-ttu-id="150e8-116">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="150e8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="150e8-117">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="150e8-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="150e8-118">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="150e8-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="150e8-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="150e8-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="150e8-120">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="150e8-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="150e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150e8-121">-DefaultProfile</span></span>
<span data-ttu-id="150e8-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="150e8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150e8-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="150e8-123">-Pool</span></span>
<span data-ttu-id="150e8-124">Especifica o **PSCloudPool** para o qual esse cmdlet atualiza o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="150e8-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="150e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150e8-125">CommonParameters</span></span>
<span data-ttu-id="150e8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150e8-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="150e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150e8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="150e8-128">INPUTS</span></span>

### <span data-ttu-id="150e8-129">Microsoft.Azure.Commands.Batch. Modelos. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="150e8-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="150e8-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="150e8-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="150e8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="150e8-131">OUTPUTS</span></span>

### <span data-ttu-id="150e8-132">System. void</span><span class="sxs-lookup"><span data-stu-id="150e8-132">System.Void</span></span>

## <span data-ttu-id="150e8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="150e8-133">NOTES</span></span>

## <span data-ttu-id="150e8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="150e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="150e8-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="150e8-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="150e8-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="150e8-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="150e8-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="150e8-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="150e8-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="150e8-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="150e8-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="150e8-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
