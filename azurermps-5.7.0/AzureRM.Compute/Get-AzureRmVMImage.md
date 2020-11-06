---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427623"
---
# <span data-ttu-id="40cbb-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="40cbb-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="40cbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="40cbb-103">Obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40cbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40cbb-104">SYNTAX</span></span>

### <span data-ttu-id="40cbb-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="40cbb-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### <span data-ttu-id="40cbb-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="40cbb-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## <span data-ttu-id="40cbb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="40cbb-108">O cmdlet **Get-AzureRmVMImage** obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="40cbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="40cbb-110">Exemplo 1: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="40cbb-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="40cbb-111">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="40cbb-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="40cbb-112">OS</span><span class="sxs-lookup"><span data-stu-id="40cbb-112">PARAMETERS</span></span>

### <span data-ttu-id="40cbb-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="40cbb-113">-FilterExpression</span></span>
<span data-ttu-id="40cbb-114">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="40cbb-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-115">-Local</span><span class="sxs-lookup"><span data-stu-id="40cbb-115">-Location</span></span>
<span data-ttu-id="40cbb-116">Especifica a localização de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-116">Specifies the location of a VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-117">-Oferta</span><span class="sxs-lookup"><span data-stu-id="40cbb-117">-Offer</span></span>
<span data-ttu-id="40cbb-118">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-118">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="40cbb-119">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="40cbb-119">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-120">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="40cbb-120">-PublisherName</span></span>
<span data-ttu-id="40cbb-121">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-121">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="40cbb-122">Para obter um editor de imagens, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="40cbb-122">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-123">-SKUs</span><span class="sxs-lookup"><span data-stu-id="40cbb-123">-Skus</span></span>
<span data-ttu-id="40cbb-124">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-124">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="40cbb-125">Para obter uma SKU, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="40cbb-125">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-126">-Versão</span><span class="sxs-lookup"><span data-stu-id="40cbb-126">-Version</span></span>
<span data-ttu-id="40cbb-127">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="40cbb-127">Specifies the version of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cbb-128">CommonParameters</span></span>
<span data-ttu-id="40cbb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cbb-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40cbb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cbb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40cbb-131">INPUTS</span></span>

### <span data-ttu-id="40cbb-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40cbb-132">None</span></span>
<span data-ttu-id="40cbb-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="40cbb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40cbb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40cbb-134">OUTPUTS</span></span>

## <span data-ttu-id="40cbb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40cbb-135">NOTES</span></span>

## <span data-ttu-id="40cbb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40cbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="40cbb-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="40cbb-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="40cbb-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="40cbb-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="40cbb-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="40cbb-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="40cbb-140">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="40cbb-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


