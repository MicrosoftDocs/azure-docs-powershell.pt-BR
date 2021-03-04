---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893370"
---
# <span data-ttu-id="7a19a-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7a19a-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="7a19a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a19a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a19a-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="7a19a-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="7a19a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a19a-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a19a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a19a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a19a-106">O cmdlet **Get-AzVMImageSku** obtém VMImage SKUs.</span><span class="sxs-lookup"><span data-stu-id="7a19a-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="7a19a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a19a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a19a-108">Exemplo 1: Obter VMImage SKUs</span><span class="sxs-lookup"><span data-stu-id="7a19a-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="7a19a-109">Este comando obtém os SKUs do editor especificado e a oferta.</span><span class="sxs-lookup"><span data-stu-id="7a19a-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="7a19a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a19a-110">PARAMETERS</span></span>

### <span data-ttu-id="7a19a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a19a-111">-DefaultProfile</span></span>
<span data-ttu-id="7a19a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7a19a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a19a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7a19a-113">-Location</span></span>
<span data-ttu-id="7a19a-114">Especifica o local do VMImage.</span><span class="sxs-lookup"><span data-stu-id="7a19a-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7a19a-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="7a19a-115">-Offer</span></span>
<span data-ttu-id="7a19a-116">Especifica o tipo de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="7a19a-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="7a19a-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7a19a-117">-PublisherName</span></span>
<span data-ttu-id="7a19a-118">Especifica o editor de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="7a19a-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="7a19a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a19a-119">CommonParameters</span></span>
<span data-ttu-id="7a19a-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a19a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a19a-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a19a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a19a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a19a-122">INPUTS</span></span>

### <span data-ttu-id="7a19a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7a19a-123">System.String</span></span>

## <span data-ttu-id="7a19a-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a19a-124">OUTPUTS</span></span>

### <span data-ttu-id="7a19a-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="7a19a-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="7a19a-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a19a-126">NOTES</span></span>

## <span data-ttu-id="7a19a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a19a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7a19a-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7a19a-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="7a19a-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7a19a-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="7a19a-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7a19a-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7a19a-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7a19a-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


