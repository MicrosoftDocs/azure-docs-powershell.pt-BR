---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426765"
---
# <span data-ttu-id="82986-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="82986-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="82986-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82986-102">SYNOPSIS</span></span>
<span data-ttu-id="82986-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="82986-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82986-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82986-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82986-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82986-105">DESCRIPTION</span></span>
<span data-ttu-id="82986-106">O cmdlet **Update-AzureRmImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="82986-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="82986-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82986-107">EXAMPLES</span></span>

### <span data-ttu-id="82986-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82986-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="82986-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="82986-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="82986-110">OS</span><span class="sxs-lookup"><span data-stu-id="82986-110">PARAMETERS</span></span>

### <span data-ttu-id="82986-111">-Imagem</span><span class="sxs-lookup"><span data-stu-id="82986-111">-Image</span></span>
<span data-ttu-id="82986-112">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="82986-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82986-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="82986-113">-ImageName</span></span>
<span data-ttu-id="82986-114">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="82986-114">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82986-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82986-115">-ResourceGroupName</span></span>
<span data-ttu-id="82986-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="82986-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82986-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="82986-117">-Confirm</span></span>
<span data-ttu-id="82986-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82986-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82986-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82986-119">-WhatIf</span></span>
<span data-ttu-id="82986-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82986-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82986-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82986-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82986-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82986-122">CommonParameters</span></span>
<span data-ttu-id="82986-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82986-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82986-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82986-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82986-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82986-125">INPUTS</span></span>

### <span data-ttu-id="82986-126">System. String</span><span class="sxs-lookup"><span data-stu-id="82986-126">System.String</span></span>
<span data-ttu-id="82986-127">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="82986-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="82986-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82986-128">OUTPUTS</span></span>

### <span data-ttu-id="82986-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="82986-129">System.Object</span></span>

## <span data-ttu-id="82986-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82986-130">NOTES</span></span>

## <span data-ttu-id="82986-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82986-131">RELATED LINKS</span></span>

