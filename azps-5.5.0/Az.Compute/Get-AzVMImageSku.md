---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112140"
---
# <span data-ttu-id="930b7-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="930b7-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="930b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="930b7-102">SYNOPSIS</span></span>
<span data-ttu-id="930b7-103">Obtém SKUs VMImage.</span><span class="sxs-lookup"><span data-stu-id="930b7-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="930b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="930b7-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="930b7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="930b7-105">DESCRIPTION</span></span>
<span data-ttu-id="930b7-106">O **cmdlet Get-AzVMImageSku** obtém VMImage SKUs.</span><span class="sxs-lookup"><span data-stu-id="930b7-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="930b7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="930b7-107">EXAMPLES</span></span>

### <span data-ttu-id="930b7-108">Exemplo 1: Obter SKUs VMImage</span><span class="sxs-lookup"><span data-stu-id="930b7-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="930b7-109">Esse comando obtém as SKUs do editor e da oferta especificadas.</span><span class="sxs-lookup"><span data-stu-id="930b7-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="930b7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="930b7-110">PARAMETERS</span></span>

### <span data-ttu-id="930b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930b7-111">-DefaultProfile</span></span>
<span data-ttu-id="930b7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="930b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930b7-113">-Local</span><span class="sxs-lookup"><span data-stu-id="930b7-113">-Location</span></span>
<span data-ttu-id="930b7-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="930b7-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="930b7-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="930b7-115">-Offer</span></span>
<span data-ttu-id="930b7-116">Especifica o tipo de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="930b7-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="930b7-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="930b7-117">-PublisherName</span></span>
<span data-ttu-id="930b7-118">Especifica o editor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="930b7-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="930b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930b7-119">CommonParameters</span></span>
<span data-ttu-id="930b7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930b7-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930b7-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="930b7-122">INPUTS</span></span>

### <span data-ttu-id="930b7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="930b7-123">System.String</span></span>

## <span data-ttu-id="930b7-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="930b7-124">OUTPUTS</span></span>

### <span data-ttu-id="930b7-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="930b7-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="930b7-126">Notas</span><span class="sxs-lookup"><span data-stu-id="930b7-126">NOTES</span></span>

## <span data-ttu-id="930b7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="930b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="930b7-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="930b7-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="930b7-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="930b7-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="930b7-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="930b7-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="930b7-131">Salvar-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="930b7-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


