---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: c69474929fa91b2e4ae1c7f4e50d5961a9322f66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785794"
---
# <span data-ttu-id="e22b8-101">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e22b8-101">Get-AzureRmVMImage</span></span>

## <span data-ttu-id="e22b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e22b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e22b8-103">Obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-103">Gets all the versions of a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e22b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e22b8-104">SYNTAX</span></span>

### <span data-ttu-id="e22b8-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="e22b8-105">ListVMImage</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e22b8-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="e22b8-106">GetVMImageDetail</span></span>
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e22b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e22b8-107">DESCRIPTION</span></span>
<span data-ttu-id="e22b8-108">O cmdlet **Get-AzureRmVMImage** obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-108">The **Get-AzureRmVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="e22b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e22b8-109">EXAMPLES</span></span>

### <span data-ttu-id="e22b8-110">Exemplo 1: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="e22b8-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="e22b8-111">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="e22b8-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="e22b8-112">OS</span><span class="sxs-lookup"><span data-stu-id="e22b8-112">PARAMETERS</span></span>

### <span data-ttu-id="e22b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22b8-113">-DefaultProfile</span></span>
<span data-ttu-id="e22b8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e22b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e22b8-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="e22b8-115">-FilterExpression</span></span>
<span data-ttu-id="e22b8-116">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="e22b8-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="e22b8-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e22b8-117">-Location</span></span>
<span data-ttu-id="e22b8-118">Especifica a localização de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="e22b8-119">-Oferta</span><span class="sxs-lookup"><span data-stu-id="e22b8-119">-Offer</span></span>
<span data-ttu-id="e22b8-120">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="e22b8-121">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="e22b8-121">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e22b8-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e22b8-122">-PublisherName</span></span>
<span data-ttu-id="e22b8-123">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="e22b8-124">Para obter um editor de imagens, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="e22b8-124">To obtain an image publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e22b8-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="e22b8-125">-Skus</span></span>
<span data-ttu-id="e22b8-126">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="e22b8-127">Para obter uma SKU, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="e22b8-127">To obtain an SKU, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e22b8-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="e22b8-128">-Version</span></span>
<span data-ttu-id="e22b8-129">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="e22b8-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="e22b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22b8-130">CommonParameters</span></span>
<span data-ttu-id="e22b8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22b8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22b8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22b8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e22b8-133">INPUTS</span></span>

### <span data-ttu-id="e22b8-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e22b8-134">None</span></span>
<span data-ttu-id="e22b8-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e22b8-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e22b8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e22b8-136">OUTPUTS</span></span>

### <span data-ttu-id="e22b8-137">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="e22b8-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="e22b8-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="e22b8-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="e22b8-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e22b8-139">NOTES</span></span>

## <span data-ttu-id="e22b8-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e22b8-140">RELATED LINKS</span></span>

[<span data-ttu-id="e22b8-141">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e22b8-141">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e22b8-142">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e22b8-142">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e22b8-143">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e22b8-143">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e22b8-144">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e22b8-144">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


