---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610516"
---
# <span data-ttu-id="b3550-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b3550-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="b3550-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3550-102">SYNOPSIS</span></span>
<span data-ttu-id="b3550-103">Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b3550-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3550-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3550-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3550-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3550-105">DESCRIPTION</span></span>
<span data-ttu-id="b3550-106">O cmdlet **Get-AzureRmImage** Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b3550-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="b3550-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3550-107">EXAMPLES</span></span>

### <span data-ttu-id="b3550-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3550-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="b3550-109">Este comando obtém as propriedades da imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b3550-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3550-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b3550-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="b3550-111">Esse comando obtém as propriedades de todas as imagens no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b3550-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3550-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b3550-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="b3550-113">Este comando obtém as propriedades de todas as imagens sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b3550-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="b3550-114">OS</span><span class="sxs-lookup"><span data-stu-id="b3550-114">PARAMETERS</span></span>

### <span data-ttu-id="b3550-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3550-115">-DefaultProfile</span></span>
<span data-ttu-id="b3550-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3550-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3550-117">-Expandir</span><span class="sxs-lookup"><span data-stu-id="b3550-117">-Expand</span></span>
<span data-ttu-id="b3550-118">Especifica a consulta de expandir expressão.</span><span class="sxs-lookup"><span data-stu-id="b3550-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3550-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b3550-119">-ImageName</span></span>
<span data-ttu-id="b3550-120">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="b3550-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3550-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3550-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3550-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3550-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3550-123">CommonParameters</span></span>
<span data-ttu-id="b3550-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3550-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3550-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3550-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3550-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3550-126">INPUTS</span></span>

### <span data-ttu-id="b3550-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3550-127">System.String</span></span>

## <span data-ttu-id="b3550-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3550-128">OUTPUTS</span></span>

### <span data-ttu-id="b3550-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="b3550-129">System.Object</span></span>

## <span data-ttu-id="b3550-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3550-130">NOTES</span></span>

## <span data-ttu-id="b3550-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3550-131">RELATED LINKS</span></span>

