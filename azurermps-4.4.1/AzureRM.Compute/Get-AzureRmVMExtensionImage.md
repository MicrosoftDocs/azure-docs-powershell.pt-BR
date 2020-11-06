---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 7010808e1879566d3b0fc78f82d0e9f82bdd626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603399"
---
# <span data-ttu-id="b83a8-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b83a8-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="b83a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b83a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b83a8-103">Obtém todas as versões para uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="b83a8-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b83a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b83a8-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b83a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b83a8-105">DESCRIPTION</span></span>
<span data-ttu-id="b83a8-106">O cmdlet **Get-AzureRmVMExtensionImage** obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="b83a8-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="b83a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b83a8-107">EXAMPLES</span></span>

### <span data-ttu-id="b83a8-108">Exemplo 1: obter as versões de uma imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="b83a8-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="b83a8-109">Esse comando obtém todas as versões da imagem de extensão para o local, o editor e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="b83a8-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="b83a8-110">OS</span><span class="sxs-lookup"><span data-stu-id="b83a8-110">PARAMETERS</span></span>

### <span data-ttu-id="b83a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83a8-111">-DefaultProfile</span></span>
<span data-ttu-id="b83a8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b83a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83a8-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b83a8-113">-FilterExpression</span></span>
<span data-ttu-id="b83a8-114">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="b83a8-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b83a8-115">-Local</span><span class="sxs-lookup"><span data-stu-id="b83a8-115">-Location</span></span>
<span data-ttu-id="b83a8-116">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="b83a8-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="b83a8-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b83a8-117">-PublisherName</span></span>
<span data-ttu-id="b83a8-118">Especifica o nome de um fornecedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="b83a8-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="b83a8-119">Para obter um fornecedor de extensão, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="b83a8-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b83a8-120">-Digite</span><span class="sxs-lookup"><span data-stu-id="b83a8-120">-Type</span></span>
<span data-ttu-id="b83a8-121">Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="b83a8-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="b83a8-122">Para obter um tipo de extensão, use o cmdlet Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="b83a8-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="b83a8-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="b83a8-123">-Version</span></span>
<span data-ttu-id="b83a8-124">Especifica a versão da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b83a8-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b83a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83a8-125">CommonParameters</span></span>
<span data-ttu-id="b83a8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83a8-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83a8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83a8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b83a8-128">INPUTS</span></span>

## <span data-ttu-id="b83a8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b83a8-129">OUTPUTS</span></span>

## <span data-ttu-id="b83a8-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b83a8-130">NOTES</span></span>

## <span data-ttu-id="b83a8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b83a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b83a8-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b83a8-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="b83a8-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b83a8-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="b83a8-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b83a8-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


