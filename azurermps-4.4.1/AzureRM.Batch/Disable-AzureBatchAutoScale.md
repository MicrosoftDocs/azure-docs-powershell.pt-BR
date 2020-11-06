---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431810"
---
# <span data-ttu-id="b471b-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b471b-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="b471b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b471b-102">SYNOPSIS</span></span>
<span data-ttu-id="b471b-103">Desabilita o dimensionamento automático de um pool.</span><span class="sxs-lookup"><span data-stu-id="b471b-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b471b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b471b-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b471b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b471b-105">DESCRIPTION</span></span>
<span data-ttu-id="b471b-106">O cmdlet **Disable-AzureBatchAutoScale** desabilita o dimensionamento automático do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="b471b-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="b471b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b471b-107">EXAMPLES</span></span>

### <span data-ttu-id="b471b-108">Exemplo 1: desabilitar o dimensionamento automático de um pool</span><span class="sxs-lookup"><span data-stu-id="b471b-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="b471b-109">Esse comando desabilita o dimensionamento automático do pool chamado mypool.</span><span class="sxs-lookup"><span data-stu-id="b471b-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="b471b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b471b-110">PARAMETERS</span></span>

### <span data-ttu-id="b471b-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b471b-111">-BatchContext</span></span>
<span data-ttu-id="b471b-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="b471b-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b471b-113">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b471b-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b471b-114">-ID</span><span class="sxs-lookup"><span data-stu-id="b471b-114">-Id</span></span>
<span data-ttu-id="b471b-115">Especifica a ID do objeto do pool.</span><span class="sxs-lookup"><span data-stu-id="b471b-115">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="b471b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b471b-116">-DefaultProfile</span></span>
<span data-ttu-id="b471b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b471b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b471b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b471b-118">CommonParameters</span></span>
<span data-ttu-id="b471b-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b471b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b471b-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b471b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b471b-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b471b-121">INPUTS</span></span>

### <span data-ttu-id="b471b-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b471b-122">BatchAccountContext</span></span>
<span data-ttu-id="b471b-123">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b471b-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b471b-124">String</span><span class="sxs-lookup"><span data-stu-id="b471b-124">String</span></span>
<span data-ttu-id="b471b-125">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b471b-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b471b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b471b-126">OUTPUTS</span></span>

## <span data-ttu-id="b471b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b471b-127">NOTES</span></span>

## <span data-ttu-id="b471b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b471b-128">RELATED LINKS</span></span>

[<span data-ttu-id="b471b-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b471b-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="b471b-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b471b-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="b471b-131">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b471b-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


