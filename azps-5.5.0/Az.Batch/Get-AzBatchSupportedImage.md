---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117945"
---
# <span data-ttu-id="6616b-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="6616b-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="6616b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6616b-102">SYNOPSIS</span></span>
<span data-ttu-id="6616b-103">Obtém imagens com suporte em lote para uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="6616b-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="6616b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6616b-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6616b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6616b-105">DESCRIPTION</span></span>
<span data-ttu-id="6616b-106">O cmdlet **Get-AzBatchSupportedImage** recebe imagens de máquina virtuais com suporte que estão disponíveis em uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6616b-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="6616b-107">Especifique a conta usando o parâmetro *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="6616b-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="6616b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6616b-108">EXAMPLES</span></span>

### <span data-ttu-id="6616b-109">Exemplo 1: Obter todas as imagens com suporte disponíveis</span><span class="sxs-lookup"><span data-stu-id="6616b-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="6616b-110">O primeiro comando obtém um contexto de conta em lotes que contém teclas de acesso para sua assinatura usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="6616b-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="6616b-111">O comando armazena o contexto na $Context variável a ser usada no próximo comando.</span><span class="sxs-lookup"><span data-stu-id="6616b-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="6616b-112">O segundo comando obtém todas as imagens com suporte disponíveis para essa conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="6616b-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="6616b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6616b-113">PARAMETERS</span></span>

### <span data-ttu-id="6616b-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6616b-114">-BatchContext</span></span>
<span data-ttu-id="6616b-115">A instância BatchAccountContext a ser usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="6616b-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="6616b-116">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="6616b-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="6616b-117">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6616b-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="6616b-118">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6616b-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="6616b-119">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6616b-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6616b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6616b-120">-DefaultProfile</span></span>
<span data-ttu-id="6616b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6616b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6616b-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6616b-122">-Filter</span></span>
<span data-ttu-id="6616b-123">Especifica uma cláusula de filtro OData para imagens com suporte.</span><span class="sxs-lookup"><span data-stu-id="6616b-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="6616b-124">Se você não especificar um filtro, esse cmdlet retornará todas as imagens compatíveis com a conta Lote.</span><span class="sxs-lookup"><span data-stu-id="6616b-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6616b-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6616b-125">-MaxCount</span></span>
<span data-ttu-id="6616b-126">Especifica o número máximo de imagens com suporte a retornar.</span><span class="sxs-lookup"><span data-stu-id="6616b-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6616b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6616b-127">CommonParameters</span></span>
<span data-ttu-id="6616b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6616b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6616b-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6616b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6616b-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="6616b-130">INPUTS</span></span>

### <span data-ttu-id="6616b-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6616b-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6616b-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="6616b-132">OUTPUTS</span></span>

### <span data-ttu-id="6616b-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="6616b-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="6616b-134">Notas</span><span class="sxs-lookup"><span data-stu-id="6616b-134">NOTES</span></span>

## <span data-ttu-id="6616b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6616b-135">RELATED LINKS</span></span>

[<span data-ttu-id="6616b-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6616b-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)