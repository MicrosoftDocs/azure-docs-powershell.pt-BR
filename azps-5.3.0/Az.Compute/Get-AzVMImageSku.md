---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430221"
---
# <span data-ttu-id="7f264-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7f264-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="7f264-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f264-102">SYNOPSIS</span></span>
<span data-ttu-id="7f264-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="7f264-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="7f264-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f264-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f264-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f264-105">DESCRIPTION</span></span>
<span data-ttu-id="7f264-106">O cmdlet **Get-AzVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="7f264-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="7f264-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f264-107">EXAMPLES</span></span>

### <span data-ttu-id="7f264-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="7f264-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="7f264-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="7f264-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="7f264-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f264-110">PARAMETERS</span></span>

### <span data-ttu-id="7f264-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f264-111">-DefaultProfile</span></span>
<span data-ttu-id="7f264-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f264-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f264-113">-Local</span><span class="sxs-lookup"><span data-stu-id="7f264-113">-Location</span></span>
<span data-ttu-id="7f264-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="7f264-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7f264-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="7f264-115">-Offer</span></span>
<span data-ttu-id="7f264-116">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="7f264-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="7f264-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7f264-117">-PublisherName</span></span>
<span data-ttu-id="7f264-118">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="7f264-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="7f264-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f264-119">CommonParameters</span></span>
<span data-ttu-id="7f264-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f264-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f264-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f264-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f264-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f264-122">INPUTS</span></span>

### <span data-ttu-id="7f264-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7f264-123">System.String</span></span>

## <span data-ttu-id="7f264-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f264-124">OUTPUTS</span></span>

### <span data-ttu-id="7f264-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="7f264-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="7f264-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f264-126">NOTES</span></span>

## <span data-ttu-id="7f264-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f264-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f264-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7f264-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="7f264-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7f264-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="7f264-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7f264-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7f264-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7f264-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


