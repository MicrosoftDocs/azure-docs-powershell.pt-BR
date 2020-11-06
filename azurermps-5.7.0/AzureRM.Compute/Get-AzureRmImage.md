---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431066"
---
# <span data-ttu-id="fc8ab-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="fc8ab-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="fc8ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8ab-103">Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc8ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc8ab-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc8ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="fc8ab-106">O cmdlet **Get-AzureRmImage** Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="fc8ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc8ab-107">EXAMPLES</span></span>

### <span data-ttu-id="fc8ab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc8ab-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="fc8ab-109">Este comando obtém as propriedades da imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fc8ab-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="fc8ab-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fc8ab-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="fc8ab-111">Esse comando obtém as propriedades de todas as imagens no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fc8ab-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="fc8ab-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fc8ab-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="fc8ab-113">Este comando obtém as propriedades de todas as imagens sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="fc8ab-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc8ab-114">PARAMETERS</span></span>

### <span data-ttu-id="fc8ab-115">-Expandir</span><span class="sxs-lookup"><span data-stu-id="fc8ab-115">-Expand</span></span>
<span data-ttu-id="fc8ab-116">Especifica a consulta de expandir expressão.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8ab-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fc8ab-117">-ImageName</span></span>
<span data-ttu-id="fc8ab-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc8ab-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8ab-121">CommonParameters</span></span>
<span data-ttu-id="fc8ab-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8ab-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8ab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8ab-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc8ab-124">INPUTS</span></span>

### <span data-ttu-id="fc8ab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8ab-125">System.String</span></span>

## <span data-ttu-id="fc8ab-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc8ab-126">OUTPUTS</span></span>

### <span data-ttu-id="fc8ab-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="fc8ab-127">System.Object</span></span>

## <span data-ttu-id="fc8ab-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc8ab-128">NOTES</span></span>

## <span data-ttu-id="fc8ab-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc8ab-129">RELATED LINKS</span></span>

