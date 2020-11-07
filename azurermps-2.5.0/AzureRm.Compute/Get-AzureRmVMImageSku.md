---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
ms.openlocfilehash: 8d2253e20e87a0e6a5d97f2dd0e405412f5a9282
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786183"
---
# <span data-ttu-id="4f5a5-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4f5a5-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="4f5a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5a5-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f5a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f5a5-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f5a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f5a5-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5a5-106">O cmdlet **Get-AzureRmVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4f5a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f5a5-107">EXAMPLES</span></span>

### <span data-ttu-id="4f5a5-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="4f5a5-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4f5a5-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4f5a5-110">OS</span><span class="sxs-lookup"><span data-stu-id="4f5a5-110">PARAMETERS</span></span>

### <span data-ttu-id="4f5a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5a5-111">-DefaultProfile</span></span>
<span data-ttu-id="4f5a5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f5a5-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4f5a5-113">-Location</span></span>
<span data-ttu-id="4f5a5-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4f5a5-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="4f5a5-115">-Offer</span></span>
<span data-ttu-id="4f5a5-116">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4f5a5-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4f5a5-117">-PublisherName</span></span>
<span data-ttu-id="4f5a5-118">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4f5a5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5a5-119">CommonParameters</span></span>
<span data-ttu-id="4f5a5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5a5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f5a5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5a5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f5a5-122">INPUTS</span></span>

### <span data-ttu-id="4f5a5-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f5a5-123">None</span></span>
<span data-ttu-id="4f5a5-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4f5a5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f5a5-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f5a5-125">OUTPUTS</span></span>

### <span data-ttu-id="4f5a5-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="4f5a5-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="4f5a5-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f5a5-127">NOTES</span></span>

## <span data-ttu-id="4f5a5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f5a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="4f5a5-129">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4f5a5-129">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4f5a5-130">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4f5a5-130">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4f5a5-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4f5a5-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4f5a5-132">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4f5a5-132">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


