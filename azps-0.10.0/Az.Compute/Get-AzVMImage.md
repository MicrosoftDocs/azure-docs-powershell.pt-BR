---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 7b7a61c6d3043fcb4687d75ac49400b88361b81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777018"
---
# <span data-ttu-id="474aa-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="474aa-101">Get-AzVMImage</span></span>

## <span data-ttu-id="474aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="474aa-102">SYNOPSIS</span></span>
<span data-ttu-id="474aa-103">Obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="474aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="474aa-104">SYNTAX</span></span>

### <span data-ttu-id="474aa-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="474aa-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="474aa-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="474aa-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="474aa-107">DESCRIPTION</span></span>
<span data-ttu-id="474aa-108">O cmdlet **Get-AzVMImage** obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="474aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="474aa-109">EXAMPLES</span></span>

### <span data-ttu-id="474aa-110">Exemplo 1: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="474aa-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

<span data-ttu-id="474aa-111">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="474aa-111">This command gets all the versions of VMImage that match the specified values.</span></span>

## <span data-ttu-id="474aa-112">OS</span><span class="sxs-lookup"><span data-stu-id="474aa-112">PARAMETERS</span></span>

### <span data-ttu-id="474aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474aa-113">-DefaultProfile</span></span>
<span data-ttu-id="474aa-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="474aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="474aa-115">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="474aa-115">-FilterExpression</span></span>
<span data-ttu-id="474aa-116">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="474aa-116">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="474aa-117">-Local</span><span class="sxs-lookup"><span data-stu-id="474aa-117">-Location</span></span>
<span data-ttu-id="474aa-118">Especifica a localização de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-118">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="474aa-119">-Oferta</span><span class="sxs-lookup"><span data-stu-id="474aa-119">-Offer</span></span>
<span data-ttu-id="474aa-120">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-120">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="474aa-121">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="474aa-121">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="474aa-122">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="474aa-122">-PublisherName</span></span>
<span data-ttu-id="474aa-123">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-123">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="474aa-124">Para obter um editor de imagens, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="474aa-124">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="474aa-125">-SKUs</span><span class="sxs-lookup"><span data-stu-id="474aa-125">-Skus</span></span>
<span data-ttu-id="474aa-126">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-126">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="474aa-127">Para obter uma SKU, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="474aa-127">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="474aa-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="474aa-128">-Version</span></span>
<span data-ttu-id="474aa-129">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="474aa-129">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="474aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474aa-130">CommonParameters</span></span>
<span data-ttu-id="474aa-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474aa-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474aa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474aa-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="474aa-133">INPUTS</span></span>

### <span data-ttu-id="474aa-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="474aa-134">None</span></span>
<span data-ttu-id="474aa-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="474aa-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="474aa-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="474aa-136">OUTPUTS</span></span>

### <span data-ttu-id="474aa-137">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="474aa-137">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="474aa-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="474aa-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="474aa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="474aa-139">NOTES</span></span>

## <span data-ttu-id="474aa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="474aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="474aa-141">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="474aa-141">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="474aa-142">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="474aa-142">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="474aa-143">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="474aa-143">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="474aa-144">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="474aa-144">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


