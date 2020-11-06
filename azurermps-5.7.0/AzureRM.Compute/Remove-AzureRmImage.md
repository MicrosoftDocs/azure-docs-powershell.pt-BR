---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 054462398a0f7b3e8710928000f9c10fb42f04db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602546"
---
# <span data-ttu-id="fca6e-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="fca6e-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="fca6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fca6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fca6e-103">Remove uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fca6e-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fca6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fca6e-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca6e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fca6e-105">DESCRIPTION</span></span>
<span data-ttu-id="fca6e-106">O cmdlet **Remove-AzureRmImage** remove uma imagem..</span><span class="sxs-lookup"><span data-stu-id="fca6e-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="fca6e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fca6e-107">EXAMPLES</span></span>

### <span data-ttu-id="fca6e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fca6e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="fca6e-109">Este comando Remove a imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fca6e-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fca6e-110">OS</span><span class="sxs-lookup"><span data-stu-id="fca6e-110">PARAMETERS</span></span>

### <span data-ttu-id="fca6e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fca6e-111">-Force</span></span>
<span data-ttu-id="fca6e-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fca6e-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fca6e-113">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fca6e-113">-ImageName</span></span>
<span data-ttu-id="fca6e-114">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="fca6e-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="fca6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="fca6e-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fca6e-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fca6e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fca6e-117">-Confirm</span></span>
<span data-ttu-id="fca6e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fca6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca6e-119">-WhatIf</span></span>
<span data-ttu-id="fca6e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fca6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca6e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fca6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca6e-122">CommonParameters</span></span>
<span data-ttu-id="fca6e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca6e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca6e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca6e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fca6e-125">INPUTS</span></span>

### <span data-ttu-id="fca6e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fca6e-126">System.String</span></span>

## <span data-ttu-id="fca6e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fca6e-127">OUTPUTS</span></span>

### <span data-ttu-id="fca6e-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="fca6e-128">System.Object</span></span>

## <span data-ttu-id="fca6e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fca6e-129">NOTES</span></span>

## <span data-ttu-id="fca6e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fca6e-130">RELATED LINKS</span></span>

