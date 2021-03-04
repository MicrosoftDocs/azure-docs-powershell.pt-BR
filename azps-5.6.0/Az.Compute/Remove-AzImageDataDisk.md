---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889298"
---
# <span data-ttu-id="28412-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="28412-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="28412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28412-102">SYNOPSIS</span></span>
<span data-ttu-id="28412-103">Remove um disco de dados de um objeto image.</span><span class="sxs-lookup"><span data-stu-id="28412-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="28412-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28412-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28412-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28412-105">DESCRIPTION</span></span>
<span data-ttu-id="28412-106">O cmdlet **Remove-AzImageDataDisk** remove um disco de dados de um objeto image.</span><span class="sxs-lookup"><span data-stu-id="28412-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="28412-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28412-107">EXAMPLES</span></span>

### <span data-ttu-id="28412-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28412-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="28412-109">Este comando remove o disco de dados do número da unidade lógica 1 da imagem existente 'Image01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="28412-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="28412-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28412-110">PARAMETERS</span></span>

### <span data-ttu-id="28412-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28412-111">-DefaultProfile</span></span>
<span data-ttu-id="28412-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="28412-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28412-113">-Image</span><span class="sxs-lookup"><span data-stu-id="28412-113">-Image</span></span>
<span data-ttu-id="28412-114">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="28412-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28412-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="28412-115">-Lun</span></span>
<span data-ttu-id="28412-116">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="28412-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28412-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28412-117">-Confirm</span></span>
<span data-ttu-id="28412-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28412-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28412-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28412-119">-WhatIf</span></span>
<span data-ttu-id="28412-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28412-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28412-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28412-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28412-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28412-122">CommonParameters</span></span>
<span data-ttu-id="28412-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28412-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28412-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28412-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28412-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28412-125">INPUTS</span></span>

### <span data-ttu-id="28412-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="28412-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="28412-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="28412-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="28412-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28412-128">OUTPUTS</span></span>

### <span data-ttu-id="28412-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="28412-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="28412-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="28412-130">NOTES</span></span>

## <span data-ttu-id="28412-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28412-131">RELATED LINKS</span></span>
