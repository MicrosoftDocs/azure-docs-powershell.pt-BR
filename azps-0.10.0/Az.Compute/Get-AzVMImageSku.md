---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: fad6c42c53e475343ad518c89dbb1a918a0f1e68
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777012"
---
# <span data-ttu-id="9da71-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9da71-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="9da71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9da71-102">SYNOPSIS</span></span>
<span data-ttu-id="9da71-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="9da71-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="9da71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9da71-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9da71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9da71-105">DESCRIPTION</span></span>
<span data-ttu-id="9da71-106">O cmdlet **Get-AzVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="9da71-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="9da71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9da71-107">EXAMPLES</span></span>

### <span data-ttu-id="9da71-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="9da71-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="9da71-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="9da71-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="9da71-110">OS</span><span class="sxs-lookup"><span data-stu-id="9da71-110">PARAMETERS</span></span>

### <span data-ttu-id="9da71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da71-111">-DefaultProfile</span></span>
<span data-ttu-id="9da71-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9da71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9da71-113">-Local</span><span class="sxs-lookup"><span data-stu-id="9da71-113">-Location</span></span>
<span data-ttu-id="9da71-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="9da71-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9da71-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="9da71-115">-Offer</span></span>
<span data-ttu-id="9da71-116">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="9da71-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="9da71-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9da71-117">-PublisherName</span></span>
<span data-ttu-id="9da71-118">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="9da71-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="9da71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da71-119">CommonParameters</span></span>
<span data-ttu-id="9da71-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da71-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da71-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da71-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9da71-122">INPUTS</span></span>

### <span data-ttu-id="9da71-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9da71-123">None</span></span>
<span data-ttu-id="9da71-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9da71-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9da71-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9da71-125">OUTPUTS</span></span>

### <span data-ttu-id="9da71-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="9da71-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="9da71-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9da71-127">NOTES</span></span>

## <span data-ttu-id="9da71-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9da71-128">RELATED LINKS</span></span>

[<span data-ttu-id="9da71-129">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9da71-129">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9da71-130">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9da71-130">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9da71-131">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9da71-131">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9da71-132">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9da71-132">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


