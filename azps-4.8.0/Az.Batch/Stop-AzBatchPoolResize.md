---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110619"
---
# <span data-ttu-id="bf92a-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bf92a-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="bf92a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf92a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf92a-103">Interrompe uma operação de redimensionamento de pool.</span><span class="sxs-lookup"><span data-stu-id="bf92a-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="bf92a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf92a-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf92a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf92a-105">DESCRIPTION</span></span>
<span data-ttu-id="bf92a-106">O cmdlet **Stop-AzBatchPoolResize** interrompe uma operação de redimensionamento em lotes do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="bf92a-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bf92a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf92a-107">EXAMPLES</span></span>

### <span data-ttu-id="bf92a-108">Exemplo 1: parar o redimensionamento de um pool</span><span class="sxs-lookup"><span data-stu-id="bf92a-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="bf92a-109">Esse comando interrompe uma operação de redimensionamento no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="bf92a-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bf92a-110">Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="bf92a-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bf92a-111">Exemplo 2: parar o redimensionamento de um pool usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="bf92a-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="bf92a-112">Esse comando interrompe o redimensionamento de um pool usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf92a-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="bf92a-113">O comando obtém o pool com a ID ContosoPool06 usando o cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="bf92a-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="bf92a-114">O comando passa esse objeto de pool para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bf92a-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="bf92a-115">O comando interrompe a operação de redimensionamento nesse pool.</span><span class="sxs-lookup"><span data-stu-id="bf92a-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="bf92a-116">OS</span><span class="sxs-lookup"><span data-stu-id="bf92a-116">PARAMETERS</span></span>

### <span data-ttu-id="bf92a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf92a-117">-BatchContext</span></span>
<span data-ttu-id="bf92a-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bf92a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf92a-119">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="bf92a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf92a-120">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="bf92a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf92a-121">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="bf92a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf92a-122">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bf92a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf92a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf92a-123">-DefaultProfile</span></span>
<span data-ttu-id="bf92a-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf92a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf92a-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bf92a-125">-Id</span></span>
<span data-ttu-id="bf92a-126">Especifica a ID do pool para o qual esse cmdlet interrompe uma operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="bf92a-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="bf92a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf92a-127">CommonParameters</span></span>
<span data-ttu-id="bf92a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf92a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf92a-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf92a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf92a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf92a-130">INPUTS</span></span>

### <span data-ttu-id="bf92a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bf92a-131">System.String</span></span>

### <span data-ttu-id="bf92a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf92a-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bf92a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf92a-133">OUTPUTS</span></span>

### <span data-ttu-id="bf92a-134">System. void</span><span class="sxs-lookup"><span data-stu-id="bf92a-134">System.Void</span></span>

## <span data-ttu-id="bf92a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf92a-135">NOTES</span></span>

## <span data-ttu-id="bf92a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf92a-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf92a-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bf92a-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bf92a-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="bf92a-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="bf92a-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bf92a-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="bf92a-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="bf92a-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
