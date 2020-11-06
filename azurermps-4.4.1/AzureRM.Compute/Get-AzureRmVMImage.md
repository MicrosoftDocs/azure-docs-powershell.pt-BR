---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: 5588d320d63a298fab632ea55d7c3b6c2220db85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426989"
---
# <span data-ttu-id="547cb-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="547cb-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="547cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="547cb-102">SYNOPSIS</span></span>
<span data-ttu-id="547cb-103">Obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="547cb-104">SYNTAX</span></span>

### <span data-ttu-id="547cb-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="547cb-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="547cb-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="547cb-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547cb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="547cb-107">DESCRIPTION</span></span>
<span data-ttu-id="547cb-108">O cmdlet **Get-AzureRmVMImage** obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="547cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="547cb-109">EXAMPLES</span></span>

### <span data-ttu-id="547cb-110">Exemplo 1: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="547cb-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="547cb-111">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="547cb-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="547cb-112">OS</span><span class="sxs-lookup"><span data-stu-id="547cb-112">PARAMETERS</span></span>

### <span data-ttu-id="547cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547cb-113">-DefaultProfile</span></span>
<span data-ttu-id="547cb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="547cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547cb-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="547cb-115">-FilterExpression</span></span>
<span data-ttu-id="547cb-116">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="547cb-116">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-117">-Local</span><span class="sxs-lookup"><span data-stu-id="547cb-117">-Location</span></span>
<span data-ttu-id="547cb-118">Especifica a localização de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-118">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-119">-Oferta</span><span class="sxs-lookup"><span data-stu-id="547cb-119">-Offer</span></span>
<span data-ttu-id="547cb-120">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="547cb-121">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="547cb-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="547cb-122">-PublisherName</span></span>
<span data-ttu-id="547cb-123">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="547cb-124">Para obter um editor de imagens, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="547cb-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="547cb-125">-Skus</span></span>
<span data-ttu-id="547cb-126">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="547cb-127">Para obter uma SKU, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="547cb-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="547cb-128">-Version</span></span>
<span data-ttu-id="547cb-129">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="547cb-129">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="547cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547cb-130">CommonParameters</span></span>
<span data-ttu-id="547cb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547cb-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547cb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547cb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="547cb-133">INPUTS</span></span>

## <span data-ttu-id="547cb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="547cb-134">OUTPUTS</span></span>

## <span data-ttu-id="547cb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="547cb-135">NOTES</span></span>

## <span data-ttu-id="547cb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="547cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="547cb-137">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="547cb-137">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="547cb-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="547cb-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="547cb-139">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="547cb-139">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="547cb-140">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="547cb-140">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


