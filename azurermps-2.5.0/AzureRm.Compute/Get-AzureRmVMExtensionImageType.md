---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785803"
---
# <span data-ttu-id="6064b-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6064b-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="6064b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6064b-102">SYNOPSIS</span></span>
<span data-ttu-id="6064b-103">Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="6064b-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6064b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6064b-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6064b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6064b-105">DESCRIPTION</span></span>
<span data-ttu-id="6064b-106">O cmdlet **Get-AzureRmVMExtensionImageType** Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="6064b-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="6064b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6064b-107">EXAMPLES</span></span>

### <span data-ttu-id="6064b-108">Exemplo 1: obter um tipo de imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="6064b-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="6064b-109">Esse comando obtém o tipo de imagem de extensão do Publicador e local especificados.</span><span class="sxs-lookup"><span data-stu-id="6064b-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="6064b-110">OS</span><span class="sxs-lookup"><span data-stu-id="6064b-110">PARAMETERS</span></span>

### <span data-ttu-id="6064b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6064b-111">-DefaultProfile</span></span>
<span data-ttu-id="6064b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6064b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6064b-113">-Local</span><span class="sxs-lookup"><span data-stu-id="6064b-113">-Location</span></span>
<span data-ttu-id="6064b-114">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="6064b-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="6064b-115">Esse cmdlet obtém o tipo de uma extensão no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6064b-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6064b-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6064b-116">-PublisherName</span></span>
<span data-ttu-id="6064b-117">Especifica o nome de um fornecedor de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="6064b-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="6064b-118">Para obter um fornecedor de extensão, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="6064b-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="6064b-119">Esse cmdlet obtém o tipo de uma extensão do Publicador que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6064b-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6064b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6064b-120">CommonParameters</span></span>
<span data-ttu-id="6064b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6064b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6064b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6064b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6064b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6064b-123">INPUTS</span></span>

### <span data-ttu-id="6064b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6064b-124">None</span></span>
<span data-ttu-id="6064b-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6064b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6064b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6064b-126">OUTPUTS</span></span>

### <span data-ttu-id="6064b-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6064b-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="6064b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6064b-128">NOTES</span></span>

## <span data-ttu-id="6064b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6064b-129">RELATED LINKS</span></span>

[<span data-ttu-id="6064b-130">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6064b-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="6064b-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6064b-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


