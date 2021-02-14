---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115969"
---
# <span data-ttu-id="aa368-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="aa368-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="aa368-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa368-102">SYNOPSIS</span></span>
<span data-ttu-id="aa368-103">Atualiza as propriedades de um pool.</span><span class="sxs-lookup"><span data-stu-id="aa368-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="aa368-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa368-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa368-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa368-105">DESCRIPTION</span></span>
<span data-ttu-id="aa368-106">O cmdlet **Set-AzBatchPool** atualiza as propriedades de um pool no serviço Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa368-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="aa368-107">Use o cmdlet Get-AzBatchPool para obter um **objeto PSCloudPool.**</span><span class="sxs-lookup"><span data-stu-id="aa368-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="aa368-108">Modifique as propriedades desse objeto e use o cmdlet atual para comprometer suas alterações no serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="aa368-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="aa368-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa368-109">EXAMPLES</span></span>

### <span data-ttu-id="aa368-110">Exemplo 1: Atualizar um pool</span><span class="sxs-lookup"><span data-stu-id="aa368-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="aa368-111">O primeiro comando obtém um pool usando **Get-AzBatchPool** e o armazena na variável $Pool dados.</span><span class="sxs-lookup"><span data-stu-id="aa368-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="aa368-112">Os três comandos a seguir modificam a especificação da tarefa inicial no $Pool objeto.</span><span class="sxs-lookup"><span data-stu-id="aa368-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="aa368-113">O comando final atualiza o serviço Lote para corresponder ao objeto local no $Pool.</span><span class="sxs-lookup"><span data-stu-id="aa368-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="aa368-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa368-114">PARAMETERS</span></span>

### <span data-ttu-id="aa368-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aa368-115">-BatchContext</span></span>
<span data-ttu-id="aa368-116">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="aa368-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aa368-117">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="aa368-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aa368-118">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="aa368-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aa368-119">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="aa368-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aa368-120">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="aa368-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aa368-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa368-121">-DefaultProfile</span></span>
<span data-ttu-id="aa368-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aa368-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa368-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="aa368-123">-Pool</span></span>
<span data-ttu-id="aa368-124">Especifica o **PSCloudPool** ao qual este cmdlet atualiza o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="aa368-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="aa368-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa368-125">CommonParameters</span></span>
<span data-ttu-id="aa368-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa368-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa368-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa368-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa368-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="aa368-128">INPUTS</span></span>

### <span data-ttu-id="aa368-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="aa368-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="aa368-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aa368-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aa368-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="aa368-131">OUTPUTS</span></span>

### <span data-ttu-id="aa368-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="aa368-132">System.Void</span></span>

## <span data-ttu-id="aa368-133">Notas</span><span class="sxs-lookup"><span data-stu-id="aa368-133">NOTES</span></span>

## <span data-ttu-id="aa368-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa368-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa368-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="aa368-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="aa368-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="aa368-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="aa368-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="aa368-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="aa368-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="aa368-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="aa368-139">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="aa368-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
