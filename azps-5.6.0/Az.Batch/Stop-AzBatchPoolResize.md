---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 339c3a537e84ff63a6eac0a6f1f63669ce4567ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886364"
---
# <span data-ttu-id="baefc-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="baefc-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="baefc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baefc-102">SYNOPSIS</span></span>
<span data-ttu-id="baefc-103">Interrompe uma operação de resize de pool.</span><span class="sxs-lookup"><span data-stu-id="baefc-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="baefc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="baefc-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baefc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="baefc-105">DESCRIPTION</span></span>
<span data-ttu-id="baefc-106">O cmdlet **Stop-AzBatchPoolResize** interrompe uma operação de resize do Lote do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="baefc-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="baefc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baefc-107">EXAMPLES</span></span>

### <span data-ttu-id="baefc-108">Exemplo 1: parar de ressarcar um pool</span><span class="sxs-lookup"><span data-stu-id="baefc-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="baefc-109">Este comando interrompe uma operação de resize no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="baefc-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="baefc-110">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.</span><span class="sxs-lookup"><span data-stu-id="baefc-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="baefc-111">Exemplo 2: pare de resizing um pool usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="baefc-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="baefc-112">Esse comando para de ressarcar um pool usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="baefc-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="baefc-113">O comando obtém o pool que tem a ID ContosoPool06 usando o cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="baefc-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="baefc-114">O comando passa esse objeto pool para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="baefc-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="baefc-115">O comando interrompe a operação de resize nesse pool.</span><span class="sxs-lookup"><span data-stu-id="baefc-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="baefc-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="baefc-116">PARAMETERS</span></span>

### <span data-ttu-id="baefc-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="baefc-117">-BatchContext</span></span>
<span data-ttu-id="baefc-118">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="baefc-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="baefc-119">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="baefc-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="baefc-120">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="baefc-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="baefc-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="baefc-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="baefc-122">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="baefc-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="baefc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baefc-123">-DefaultProfile</span></span>
<span data-ttu-id="baefc-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="baefc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baefc-125">-Id</span><span class="sxs-lookup"><span data-stu-id="baefc-125">-Id</span></span>
<span data-ttu-id="baefc-126">Especifica a ID do pool para o qual este cmdlet interrompe uma operação de resizing.</span><span class="sxs-lookup"><span data-stu-id="baefc-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baefc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baefc-127">CommonParameters</span></span>
<span data-ttu-id="baefc-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baefc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baefc-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baefc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baefc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baefc-130">INPUTS</span></span>

### <span data-ttu-id="baefc-131">System.String</span><span class="sxs-lookup"><span data-stu-id="baefc-131">System.String</span></span>

### <span data-ttu-id="baefc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="baefc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="baefc-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="baefc-133">OUTPUTS</span></span>

### <span data-ttu-id="baefc-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="baefc-134">System.Void</span></span>

## <span data-ttu-id="baefc-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="baefc-135">NOTES</span></span>

## <span data-ttu-id="baefc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baefc-136">RELATED LINKS</span></span>

[<span data-ttu-id="baefc-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="baefc-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="baefc-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="baefc-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="baefc-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="baefc-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="baefc-140">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="baefc-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
