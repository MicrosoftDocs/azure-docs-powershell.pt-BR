---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441483"
---
# <span data-ttu-id="38ba5-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38ba5-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="38ba5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="38ba5-103">Desabilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="38ba5-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38ba5-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38ba5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="38ba5-106">O cmdlet **Disable-AzureBatchAutoScale** desabilita o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="38ba5-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="38ba5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="38ba5-108">Exemplo 1: desabilitar o dimensionamento automático de um pool</span><span class="sxs-lookup"><span data-stu-id="38ba5-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="38ba5-109">Esse comando desabilita o dimensionamento automático do pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="38ba5-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="38ba5-110">OS</span><span class="sxs-lookup"><span data-stu-id="38ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="38ba5-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="38ba5-111">-BatchContext</span></span>
<span data-ttu-id="38ba5-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="38ba5-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38ba5-113">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="38ba5-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="38ba5-114">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="38ba5-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="38ba5-115">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="38ba5-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="38ba5-116">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="38ba5-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="38ba5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ba5-117">-DefaultProfile</span></span>
<span data-ttu-id="38ba5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38ba5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38ba5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="38ba5-119">-Id</span></span>
<span data-ttu-id="38ba5-120">Especifica a ID do objeto do pool.</span><span class="sxs-lookup"><span data-stu-id="38ba5-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ba5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ba5-121">CommonParameters</span></span>
<span data-ttu-id="38ba5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ba5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ba5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ba5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ba5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38ba5-124">INPUTS</span></span>

### <span data-ttu-id="38ba5-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="38ba5-125">BatchAccountContext</span></span>
<span data-ttu-id="38ba5-126">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="38ba5-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="38ba5-127">String</span><span class="sxs-lookup"><span data-stu-id="38ba5-127">String</span></span>
<span data-ttu-id="38ba5-128">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="38ba5-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="38ba5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38ba5-129">OUTPUTS</span></span>

## <span data-ttu-id="38ba5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38ba5-130">NOTES</span></span>

## <span data-ttu-id="38ba5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38ba5-131">RELATED LINKS</span></span>

[<span data-ttu-id="38ba5-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38ba5-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="38ba5-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="38ba5-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="38ba5-134">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="38ba5-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


