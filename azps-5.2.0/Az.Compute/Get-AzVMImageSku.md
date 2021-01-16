---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260707"
---
# <span data-ttu-id="8dbd0-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8dbd0-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="8dbd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbd0-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="8dbd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dbd0-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dbd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dbd0-105">DESCRIPTION</span></span>
<span data-ttu-id="8dbd0-106">O cmdlet **Get-AzVMImageSku** tem SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="8dbd0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dbd0-107">EXAMPLES</span></span>

### <span data-ttu-id="8dbd0-108">Exemplo 1: obter SKUs da VMImage</span><span class="sxs-lookup"><span data-stu-id="8dbd0-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="8dbd0-109">Esse comando obtém as SKUs do fornecedor e da oferta especificados.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="8dbd0-110">OS</span><span class="sxs-lookup"><span data-stu-id="8dbd0-110">PARAMETERS</span></span>

### <span data-ttu-id="8dbd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbd0-111">-DefaultProfile</span></span>
<span data-ttu-id="8dbd0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dbd0-113">-Local</span><span class="sxs-lookup"><span data-stu-id="8dbd0-113">-Location</span></span>
<span data-ttu-id="8dbd0-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="8dbd0-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="8dbd0-115">-Offer</span></span>
<span data-ttu-id="8dbd0-116">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="8dbd0-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8dbd0-117">-PublisherName</span></span>
<span data-ttu-id="8dbd0-118">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="8dbd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbd0-119">CommonParameters</span></span>
<span data-ttu-id="8dbd0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dbd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbd0-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dbd0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbd0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dbd0-122">INPUTS</span></span>

### <span data-ttu-id="8dbd0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8dbd0-123">System.String</span></span>

## <span data-ttu-id="8dbd0-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dbd0-124">OUTPUTS</span></span>

### <span data-ttu-id="8dbd0-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="8dbd0-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="8dbd0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dbd0-126">NOTES</span></span>

## <span data-ttu-id="8dbd0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dbd0-127">RELATED LINKS</span></span>

[<span data-ttu-id="8dbd0-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8dbd0-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="8dbd0-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8dbd0-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8dbd0-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8dbd0-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8dbd0-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8dbd0-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


