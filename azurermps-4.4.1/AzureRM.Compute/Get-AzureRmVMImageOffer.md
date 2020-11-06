---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: eb31437870a77e4af84bdcb94ffa4172d117c78d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610515"
---
# <span data-ttu-id="7cf50-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7cf50-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="7cf50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cf50-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf50-103">Obtém tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cf50-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cf50-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cf50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cf50-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf50-106">O cmdlet **Get-AzureRmVMImageOffer** Obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cf50-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="7cf50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cf50-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf50-108">Exemplo 1: obter tipos de oferta para um fornecedor</span><span class="sxs-lookup"><span data-stu-id="7cf50-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="7cf50-109">Esse comando obtém os tipos de oferta do fornecedor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="7cf50-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="7cf50-110">OS</span><span class="sxs-lookup"><span data-stu-id="7cf50-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf50-111">-DefaultProfile</span></span>
<span data-ttu-id="7cf50-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf50-113">-Local</span><span class="sxs-lookup"><span data-stu-id="7cf50-113">-Location</span></span>
<span data-ttu-id="7cf50-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cf50-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="7cf50-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7cf50-115">-PublisherName</span></span>
<span data-ttu-id="7cf50-116">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="7cf50-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="7cf50-117">Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="7cf50-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7cf50-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf50-118">CommonParameters</span></span>
<span data-ttu-id="7cf50-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf50-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf50-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf50-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf50-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cf50-121">INPUTS</span></span>

## <span data-ttu-id="7cf50-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cf50-122">OUTPUTS</span></span>

## <span data-ttu-id="7cf50-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cf50-123">NOTES</span></span>

## <span data-ttu-id="7cf50-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cf50-124">RELATED LINKS</span></span>

[<span data-ttu-id="7cf50-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7cf50-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7cf50-126">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7cf50-126">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="7cf50-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7cf50-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="7cf50-128">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7cf50-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


