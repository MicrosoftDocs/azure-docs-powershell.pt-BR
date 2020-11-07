---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955058"
---
# <span data-ttu-id="e86d5-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="e86d5-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="e86d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e86d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e86d5-103">Remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="e86d5-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="e86d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e86d5-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e86d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e86d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e86d5-106">O cmdlet **Remove-AzImageDataDisk** remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="e86d5-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="e86d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e86d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e86d5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e86d5-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="e86d5-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="e86d5-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e86d5-110">OS</span><span class="sxs-lookup"><span data-stu-id="e86d5-110">PARAMETERS</span></span>

### <span data-ttu-id="e86d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86d5-111">-DefaultProfile</span></span>
<span data-ttu-id="e86d5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e86d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e86d5-113">-Imagem</span><span class="sxs-lookup"><span data-stu-id="e86d5-113">-Image</span></span>
<span data-ttu-id="e86d5-114">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="e86d5-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="e86d5-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="e86d5-115">-Lun</span></span>
<span data-ttu-id="e86d5-116">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="e86d5-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="e86d5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e86d5-117">-Confirm</span></span>
<span data-ttu-id="e86d5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e86d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e86d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e86d5-119">-WhatIf</span></span>
<span data-ttu-id="e86d5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e86d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e86d5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e86d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e86d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86d5-122">CommonParameters</span></span>
<span data-ttu-id="e86d5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86d5-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e86d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86d5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e86d5-125">INPUTS</span></span>

### <span data-ttu-id="e86d5-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e86d5-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="e86d5-127">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e86d5-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e86d5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e86d5-128">OUTPUTS</span></span>

### <span data-ttu-id="e86d5-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e86d5-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e86d5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e86d5-130">NOTES</span></span>

## <span data-ttu-id="e86d5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e86d5-131">RELATED LINKS</span></span>
