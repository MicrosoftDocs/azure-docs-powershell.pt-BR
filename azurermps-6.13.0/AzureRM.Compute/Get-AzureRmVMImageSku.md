---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImageSku.md
ms.openlocfilehash: 5131a9ea24ea14114c9a4d5f5600bbe190499f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430952"
---
# <span data-ttu-id="4447d-101">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="4447d-101">Get-AzureRmVMImageSku</span></span>

## <span data-ttu-id="4447d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4447d-102">SYNOPSIS</span></span>
<span data-ttu-id="4447d-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="4447d-103">Gets VMImage SKUs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4447d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4447d-104">SYNTAX</span></span>

```
Get-AzureRmVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4447d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4447d-105">DESCRIPTION</span></span>
<span data-ttu-id="4447d-106">O cmdlet **Get-AzureRmVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="4447d-106">The **Get-AzureRmVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="4447d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4447d-107">EXAMPLES</span></span>

### <span data-ttu-id="4447d-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="4447d-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzureRmVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="4447d-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="4447d-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="4447d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4447d-110">PARAMETERS</span></span>

### <span data-ttu-id="4447d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4447d-111">-DefaultProfile</span></span>
<span data-ttu-id="4447d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4447d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4447d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4447d-113">-Location</span></span>
<span data-ttu-id="4447d-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4447d-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="4447d-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="4447d-115">-Offer</span></span>
<span data-ttu-id="4447d-116">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="4447d-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="4447d-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="4447d-117">-PublisherName</span></span>
<span data-ttu-id="4447d-118">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="4447d-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="4447d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4447d-119">CommonParameters</span></span>
<span data-ttu-id="4447d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4447d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4447d-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4447d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4447d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4447d-122">INPUTS</span></span>

### <span data-ttu-id="4447d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4447d-123">System.String</span></span>

## <span data-ttu-id="4447d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4447d-124">OUTPUTS</span></span>

### <span data-ttu-id="4447d-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="4447d-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="4447d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4447d-126">NOTES</span></span>

## <span data-ttu-id="4447d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4447d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4447d-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4447d-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="4447d-129">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="4447d-129">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="4447d-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4447d-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4447d-131">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4447d-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)

