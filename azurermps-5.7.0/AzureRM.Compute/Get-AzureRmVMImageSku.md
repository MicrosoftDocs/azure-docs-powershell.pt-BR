---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 7c4b59f97a6cd74da791f090b1c90be72f43a2c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610422"
---
# <span data-ttu-id="76f76-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="76f76-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="76f76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76f76-102">SYNOPSIS</span></span>
<span data-ttu-id="76f76-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="76f76-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76f76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76f76-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String> [<CommonParameters>]
```

## <span data-ttu-id="76f76-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76f76-105">DESCRIPTION</span></span>
<span data-ttu-id="76f76-106">O cmdlet **Get-AzureRmVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="76f76-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="76f76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76f76-107">EXAMPLES</span></span>

### <span data-ttu-id="76f76-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="76f76-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="76f76-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="76f76-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="76f76-110">OS</span><span class="sxs-lookup"><span data-stu-id="76f76-110">PARAMETERS</span></span>

### <span data-ttu-id="76f76-111">-Local</span><span class="sxs-lookup"><span data-stu-id="76f76-111">-Location</span></span>
<span data-ttu-id="76f76-112">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="76f76-112">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="76f76-113">-Oferta</span><span class="sxs-lookup"><span data-stu-id="76f76-113">-Offer</span></span>
<span data-ttu-id="76f76-114">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="76f76-114">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="76f76-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="76f76-115">-PublisherName</span></span>
<span data-ttu-id="76f76-116">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="76f76-116">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="76f76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f76-117">CommonParameters</span></span>
<span data-ttu-id="76f76-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f76-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f76-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76f76-120">INPUTS</span></span>

### <span data-ttu-id="76f76-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76f76-121">None</span></span>
<span data-ttu-id="76f76-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="76f76-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76f76-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76f76-123">OUTPUTS</span></span>

## <span data-ttu-id="76f76-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76f76-124">NOTES</span></span>

## <span data-ttu-id="76f76-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76f76-125">RELATED LINKS</span></span>

[<span data-ttu-id="76f76-126">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="76f76-126">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="76f76-127">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="76f76-127">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="76f76-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="76f76-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="76f76-129">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="76f76-129">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


