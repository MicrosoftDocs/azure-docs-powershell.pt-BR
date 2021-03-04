---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 26a280ef567ed09ff14cf143048aadceeeed29e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890483"
---
# <span data-ttu-id="521f8-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="521f8-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="521f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521f8-102">SYNOPSIS</span></span>
<span data-ttu-id="521f8-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="521f8-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="521f8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="521f8-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521f8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="521f8-105">DESCRIPTION</span></span>
<span data-ttu-id="521f8-106">O cmdlet **Set-AzBatchPool** atualiza as propriedades de um pool no serviço batch do Azure.</span><span class="sxs-lookup"><span data-stu-id="521f8-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="521f8-107">Use o cmdlet Get-AzBatchPool para obter um **objeto PSCloudPool.**</span><span class="sxs-lookup"><span data-stu-id="521f8-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="521f8-108">Modifique as propriedades desse objeto e, em seguida, use o cmdlet atual para comprometer suas alterações no serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="521f8-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="521f8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="521f8-109">EXAMPLES</span></span>

### <span data-ttu-id="521f8-110">Exemplo 1: atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="521f8-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="521f8-111">O primeiro comando obtém um pool usando **Get-AzBatchPool** e o armazena na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="521f8-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="521f8-112">Os três comandos a seguir modificam a especificação da tarefa inicial no $Pool objeto.</span><span class="sxs-lookup"><span data-stu-id="521f8-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="521f8-113">O comando final atualiza o serviço Batch para corresponder ao objeto local $Pool.</span><span class="sxs-lookup"><span data-stu-id="521f8-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="521f8-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="521f8-114">PARAMETERS</span></span>

### <span data-ttu-id="521f8-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="521f8-115">-BatchContext</span></span>
<span data-ttu-id="521f8-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="521f8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="521f8-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="521f8-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="521f8-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="521f8-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="521f8-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="521f8-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="521f8-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="521f8-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="521f8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521f8-121">-DefaultProfile</span></span>
<span data-ttu-id="521f8-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="521f8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521f8-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="521f8-123">-Pool</span></span>
<span data-ttu-id="521f8-124">Especifica o **PSCloudPool** ao qual este cmdlet atualiza o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="521f8-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="521f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521f8-125">CommonParameters</span></span>
<span data-ttu-id="521f8-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521f8-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="521f8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521f8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="521f8-128">INPUTS</span></span>

### <span data-ttu-id="521f8-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="521f8-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="521f8-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="521f8-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="521f8-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="521f8-131">OUTPUTS</span></span>

### <span data-ttu-id="521f8-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="521f8-132">System.Void</span></span>

## <span data-ttu-id="521f8-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="521f8-133">NOTES</span></span>

## <span data-ttu-id="521f8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="521f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="521f8-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="521f8-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="521f8-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="521f8-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="521f8-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="521f8-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="521f8-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="521f8-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="521f8-139">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="521f8-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
