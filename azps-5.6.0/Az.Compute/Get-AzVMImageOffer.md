---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 94556ce0b78b90ae9c418aee175f090e9209adb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893378"
---
# <span data-ttu-id="95c40-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="95c40-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="95c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c40-102">SYNOPSIS</span></span>
<span data-ttu-id="95c40-103">Obtém tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="95c40-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="95c40-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95c40-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95c40-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95c40-105">DESCRIPTION</span></span>
<span data-ttu-id="95c40-106">O cmdlet **Get-AzVMImageOffer** obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="95c40-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="95c40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95c40-107">EXAMPLES</span></span>

### <span data-ttu-id="95c40-108">Exemplo 1: Obter tipos de oferta para um editor</span><span class="sxs-lookup"><span data-stu-id="95c40-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="95c40-109">Este comando obtém os tipos de oferta para o editor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="95c40-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="95c40-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95c40-110">PARAMETERS</span></span>

### <span data-ttu-id="95c40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c40-111">-DefaultProfile</span></span>
<span data-ttu-id="95c40-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="95c40-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c40-113">-Location</span><span class="sxs-lookup"><span data-stu-id="95c40-113">-Location</span></span>
<span data-ttu-id="95c40-114">Especifica o local do VMImage.</span><span class="sxs-lookup"><span data-stu-id="95c40-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="95c40-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="95c40-115">-PublisherName</span></span>
<span data-ttu-id="95c40-116">Especifica o nome de um editor de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="95c40-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="95c40-117">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95c40-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="95c40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c40-118">CommonParameters</span></span>
<span data-ttu-id="95c40-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c40-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95c40-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c40-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95c40-121">INPUTS</span></span>

### <span data-ttu-id="95c40-122">System.String</span><span class="sxs-lookup"><span data-stu-id="95c40-122">System.String</span></span>

## <span data-ttu-id="95c40-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95c40-123">OUTPUTS</span></span>

### <span data-ttu-id="95c40-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="95c40-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="95c40-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="95c40-125">NOTES</span></span>

## <span data-ttu-id="95c40-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95c40-126">RELATED LINKS</span></span>

[<span data-ttu-id="95c40-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="95c40-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="95c40-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="95c40-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="95c40-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="95c40-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="95c40-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="95c40-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


