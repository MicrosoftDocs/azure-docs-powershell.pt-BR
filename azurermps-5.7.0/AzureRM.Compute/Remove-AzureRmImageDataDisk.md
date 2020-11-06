---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 4115cabbeeb2a7c458ce52e80eb251cb972491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427607"
---
# <span data-ttu-id="cb4c3-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb4c3-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="cb4c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4c3-103">Remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb4c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb4c3-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <Image> [-Lun] <Int32> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb4c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb4c3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb4c3-106">O cmdlet **Remove-AzureRmImageDataDisk** remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="cb4c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb4c3-107">EXAMPLES</span></span>

### <span data-ttu-id="cb4c3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb4c3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="cb4c3-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cb4c3-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb4c3-110">PARAMETERS</span></span>

### <span data-ttu-id="cb4c3-111">-Imagem</span><span class="sxs-lookup"><span data-stu-id="cb4c3-111">-Image</span></span>
<span data-ttu-id="cb4c3-112">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-112">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-113">-LUN</span><span class="sxs-lookup"><span data-stu-id="cb4c3-113">-Lun</span></span>
<span data-ttu-id="cb4c3-114">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="cb4c3-114">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb4c3-115">-Confirm</span></span>
<span data-ttu-id="cb4c3-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb4c3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb4c3-117">-WhatIf</span></span>
<span data-ttu-id="cb4c3-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb4c3-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb4c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4c3-120">CommonParameters</span></span>
<span data-ttu-id="cb4c3-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb4c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4c3-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb4c3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4c3-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb4c3-123">INPUTS</span></span>

### <span data-ttu-id="cb4c3-124">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="cb4c3-124">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="cb4c3-125">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cb4c3-125">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cb4c3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb4c3-126">OUTPUTS</span></span>

### <span data-ttu-id="cb4c3-127">Microsoft. Azure. Management. COMPUTE. Models. Image</span><span class="sxs-lookup"><span data-stu-id="cb4c3-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="cb4c3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb4c3-128">NOTES</span></span>

## <span data-ttu-id="cb4c3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb4c3-129">RELATED LINKS</span></span>

