---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 45accc1c3fd52720d3764a9167f6354316a0c9fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428265"
---
# <span data-ttu-id="b502c-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b502c-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="b502c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b502c-102">SYNOPSIS</span></span>
<span data-ttu-id="b502c-103">Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="b502c-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b502c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b502c-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b502c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b502c-105">DESCRIPTION</span></span>
<span data-ttu-id="b502c-106">O cmdlet **Get-AzureRmVMExtensionImageType** Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="b502c-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="b502c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b502c-107">EXAMPLES</span></span>

### <span data-ttu-id="b502c-108">Exemplo 1: obter um tipo de imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="b502c-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="b502c-109">Esse comando obtém o tipo de imagem de extensão do Publicador e local especificados.</span><span class="sxs-lookup"><span data-stu-id="b502c-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="b502c-110">OS</span><span class="sxs-lookup"><span data-stu-id="b502c-110">PARAMETERS</span></span>

### <span data-ttu-id="b502c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b502c-111">-DefaultProfile</span></span>
<span data-ttu-id="b502c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b502c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b502c-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b502c-113">-Location</span></span>
<span data-ttu-id="b502c-114">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="b502c-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="b502c-115">Esse cmdlet obtém o tipo de uma extensão no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b502c-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="b502c-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b502c-116">-PublisherName</span></span>
<span data-ttu-id="b502c-117">Especifica o nome de um fornecedor de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="b502c-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="b502c-118">Para obter um fornecedor de extensão, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="b502c-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="b502c-119">Esse cmdlet obtém o tipo de uma extensão do Publicador que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b502c-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="b502c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b502c-120">CommonParameters</span></span>
<span data-ttu-id="b502c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b502c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b502c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b502c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b502c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b502c-123">INPUTS</span></span>

## <span data-ttu-id="b502c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b502c-124">OUTPUTS</span></span>

## <span data-ttu-id="b502c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b502c-125">NOTES</span></span>

## <span data-ttu-id="b502c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b502c-126">RELATED LINKS</span></span>

[<span data-ttu-id="b502c-127">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b502c-127">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="b502c-128">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b502c-128">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


