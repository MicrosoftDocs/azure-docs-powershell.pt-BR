---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImageDataDisk.md
ms.openlocfilehash: 8ff2544aab072842ed851ae0c3768f57d180186d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428534"
---
# <span data-ttu-id="00231-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="00231-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="00231-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00231-102">SYNOPSIS</span></span>
<span data-ttu-id="00231-103">Remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="00231-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00231-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00231-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00231-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00231-105">DESCRIPTION</span></span>
<span data-ttu-id="00231-106">O cmdlet **Remove-AzureRmImageDataDisk** remove um disco de dados de um objeto Image.</span><span class="sxs-lookup"><span data-stu-id="00231-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="00231-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00231-107">EXAMPLES</span></span>

### <span data-ttu-id="00231-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00231-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="00231-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="00231-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="00231-110">OS</span><span class="sxs-lookup"><span data-stu-id="00231-110">PARAMETERS</span></span>

### <span data-ttu-id="00231-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00231-111">-DefaultProfile</span></span>
<span data-ttu-id="00231-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00231-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00231-113">-Imagem</span><span class="sxs-lookup"><span data-stu-id="00231-113">-Image</span></span>
<span data-ttu-id="00231-114">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="00231-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="00231-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="00231-115">-Lun</span></span>
<span data-ttu-id="00231-116">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="00231-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="00231-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00231-117">-Confirm</span></span>
<span data-ttu-id="00231-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00231-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00231-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00231-119">-WhatIf</span></span>
<span data-ttu-id="00231-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00231-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00231-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00231-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00231-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00231-122">CommonParameters</span></span>
<span data-ttu-id="00231-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00231-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00231-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00231-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00231-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00231-125">INPUTS</span></span>

### <span data-ttu-id="00231-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="00231-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="00231-127">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="00231-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="00231-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00231-128">OUTPUTS</span></span>

### <span data-ttu-id="00231-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="00231-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="00231-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00231-130">NOTES</span></span>

## <span data-ttu-id="00231-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00231-131">RELATED LINKS</span></span>