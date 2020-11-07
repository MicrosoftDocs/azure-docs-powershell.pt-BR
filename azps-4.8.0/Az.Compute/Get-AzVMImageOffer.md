---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955757"
---
# <span data-ttu-id="483b2-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="483b2-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="483b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="483b2-102">SYNOPSIS</span></span>
<span data-ttu-id="483b2-103">Obtém tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="483b2-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="483b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="483b2-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="483b2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="483b2-105">DESCRIPTION</span></span>
<span data-ttu-id="483b2-106">O cmdlet **Get-AzVMImageOffer** Obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="483b2-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="483b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="483b2-107">EXAMPLES</span></span>

### <span data-ttu-id="483b2-108">Exemplo 1: obter tipos de oferta para um fornecedor</span><span class="sxs-lookup"><span data-stu-id="483b2-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="483b2-109">Esse comando obtém os tipos de oferta do fornecedor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="483b2-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="483b2-110">OS</span><span class="sxs-lookup"><span data-stu-id="483b2-110">PARAMETERS</span></span>

### <span data-ttu-id="483b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483b2-111">-DefaultProfile</span></span>
<span data-ttu-id="483b2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="483b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483b2-113">-Local</span><span class="sxs-lookup"><span data-stu-id="483b2-113">-Location</span></span>
<span data-ttu-id="483b2-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="483b2-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="483b2-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="483b2-115">-PublisherName</span></span>
<span data-ttu-id="483b2-116">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="483b2-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="483b2-117">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="483b2-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="483b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483b2-118">CommonParameters</span></span>
<span data-ttu-id="483b2-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483b2-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="483b2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483b2-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="483b2-121">INPUTS</span></span>

### <span data-ttu-id="483b2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="483b2-122">System.String</span></span>

## <span data-ttu-id="483b2-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="483b2-123">OUTPUTS</span></span>

### <span data-ttu-id="483b2-124">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="483b2-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="483b2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="483b2-125">NOTES</span></span>

## <span data-ttu-id="483b2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="483b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="483b2-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="483b2-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="483b2-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="483b2-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="483b2-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="483b2-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="483b2-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="483b2-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


