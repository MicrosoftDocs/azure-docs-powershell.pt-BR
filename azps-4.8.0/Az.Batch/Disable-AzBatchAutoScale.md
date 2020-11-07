---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955142"
---
# <span data-ttu-id="99058-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99058-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="99058-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99058-102">SYNOPSIS</span></span>
<span data-ttu-id="99058-103">Desabilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="99058-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="99058-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99058-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99058-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99058-105">DESCRIPTION</span></span>
<span data-ttu-id="99058-106">O cmdlet **Disable-AzBatchAutoScale** desabilita o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="99058-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="99058-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99058-107">EXAMPLES</span></span>

### <span data-ttu-id="99058-108">Exemplo 1: desabilitar o dimensionamento automático de um pool</span><span class="sxs-lookup"><span data-stu-id="99058-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="99058-109">Esse comando desabilita o dimensionamento automático do pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="99058-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="99058-110">OS</span><span class="sxs-lookup"><span data-stu-id="99058-110">PARAMETERS</span></span>

### <span data-ttu-id="99058-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99058-111">-BatchContext</span></span>
<span data-ttu-id="99058-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="99058-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99058-113">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="99058-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99058-114">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="99058-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99058-115">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="99058-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99058-116">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="99058-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99058-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99058-117">-DefaultProfile</span></span>
<span data-ttu-id="99058-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99058-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99058-119">-ID</span><span class="sxs-lookup"><span data-stu-id="99058-119">-Id</span></span>
<span data-ttu-id="99058-120">Especifica a ID do objeto do pool.</span><span class="sxs-lookup"><span data-stu-id="99058-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="99058-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99058-121">CommonParameters</span></span>
<span data-ttu-id="99058-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99058-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99058-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99058-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99058-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99058-124">INPUTS</span></span>

### <span data-ttu-id="99058-125">System. String</span><span class="sxs-lookup"><span data-stu-id="99058-125">System.String</span></span>

### <span data-ttu-id="99058-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99058-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99058-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99058-127">OUTPUTS</span></span>

### <span data-ttu-id="99058-128">System. void</span><span class="sxs-lookup"><span data-stu-id="99058-128">System.Void</span></span>

## <span data-ttu-id="99058-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99058-129">NOTES</span></span>

## <span data-ttu-id="99058-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99058-130">RELATED LINKS</span></span>

[<span data-ttu-id="99058-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99058-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="99058-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="99058-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="99058-133">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="99058-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


