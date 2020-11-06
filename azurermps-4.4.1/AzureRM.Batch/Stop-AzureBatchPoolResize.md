---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432250"
---
# <span data-ttu-id="d9b55-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d9b55-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="d9b55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9b55-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b55-103">Interrompe uma operação de redimensionamento de pool.</span><span class="sxs-lookup"><span data-stu-id="d9b55-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9b55-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b55-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9b55-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b55-106">O cmdlet **Stop-AzureBatchPoolResize** interrompe uma operação de redimensionamento em lotes do Azure em um pool.</span><span class="sxs-lookup"><span data-stu-id="d9b55-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="d9b55-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9b55-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b55-108">Exemplo 1: parar o redimensionamento de um pool</span><span class="sxs-lookup"><span data-stu-id="d9b55-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="d9b55-109">Esse comando interrompe uma operação de redimensionamento no pool que tem a ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="d9b55-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="d9b55-110">Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.</span><span class="sxs-lookup"><span data-stu-id="d9b55-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d9b55-111">Exemplo 2: parar o redimensionamento de um pool usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d9b55-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="d9b55-112">Esse comando interrompe o redimensionamento de um pool usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9b55-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="d9b55-113">O comando obtém o pool com a ID ContosoPool06 usando o cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="d9b55-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="d9b55-114">O comando passa esse objeto de pool para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d9b55-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="d9b55-115">O comando interrompe a operação de redimensionamento nesse pool.</span><span class="sxs-lookup"><span data-stu-id="d9b55-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="d9b55-116">OS</span><span class="sxs-lookup"><span data-stu-id="d9b55-116">PARAMETERS</span></span>

### <span data-ttu-id="d9b55-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9b55-117">-BatchContext</span></span>
<span data-ttu-id="d9b55-118">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="d9b55-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9b55-119">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d9b55-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d9b55-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d9b55-120">-Id</span></span>
<span data-ttu-id="d9b55-121">Especifica a ID do pool para o qual esse cmdlet interrompe uma operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="d9b55-121">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="d9b55-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b55-122">-DefaultProfile</span></span>
<span data-ttu-id="d9b55-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b55-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b55-124">CommonParameters</span></span>
<span data-ttu-id="d9b55-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b55-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b55-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9b55-127">INPUTS</span></span>

### <span data-ttu-id="d9b55-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9b55-128">BatchAccountContext</span></span>
<span data-ttu-id="d9b55-129">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d9b55-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d9b55-130">String</span><span class="sxs-lookup"><span data-stu-id="d9b55-130">String</span></span>
<span data-ttu-id="d9b55-131">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d9b55-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d9b55-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9b55-132">OUTPUTS</span></span>

## <span data-ttu-id="d9b55-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9b55-133">NOTES</span></span>

## <span data-ttu-id="d9b55-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9b55-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9b55-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d9b55-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d9b55-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="d9b55-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="d9b55-137">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d9b55-137">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="d9b55-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="d9b55-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


