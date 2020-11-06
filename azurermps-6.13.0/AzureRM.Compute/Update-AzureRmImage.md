---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: 34c4eefe2792de239b2f3ae2a9348704497a4bd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602987"
---
# <span data-ttu-id="2a2ac-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="2a2ac-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="2a2ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2ac-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a2ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a2ac-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a2ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2ac-106">O cmdlet **Update-AzureRmImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="2a2ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="2a2ac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a2ac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="2a2ac-109">Este comando Remove o disco de dados da unidade lógica número 1 da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2a2ac-110">OS</span><span class="sxs-lookup"><span data-stu-id="2a2ac-110">PARAMETERS</span></span>

### <span data-ttu-id="2a2ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a2ac-111">-AsJob</span></span>
<span data-ttu-id="2a2ac-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2a2ac-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2ac-113">-DefaultProfile</span></span>
<span data-ttu-id="2a2ac-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a2ac-115">-Imagem</span><span class="sxs-lookup"><span data-stu-id="2a2ac-115">-Image</span></span>
<span data-ttu-id="2a2ac-116">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-116">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a2ac-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="2a2ac-117">-ImageName</span></span>
<span data-ttu-id="2a2ac-118">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a2ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="2a2ac-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a2ac-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a2ac-121">-Confirm</span></span>
<span data-ttu-id="2a2ac-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2ac-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2ac-123">-WhatIf</span></span>
<span data-ttu-id="2a2ac-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2ac-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2ac-126">CommonParameters</span></span>
<span data-ttu-id="2a2ac-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2ac-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2ac-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2ac-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a2ac-129">INPUTS</span></span>

### <span data-ttu-id="2a2ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2ac-130">System.String</span></span>

### <span data-ttu-id="2a2ac-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="2a2ac-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="2a2ac-132">Parâmetros: Image (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a2ac-132">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="2a2ac-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a2ac-133">OUTPUTS</span></span>

### <span data-ttu-id="2a2ac-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="2a2ac-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="2a2ac-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a2ac-135">NOTES</span></span>

## <span data-ttu-id="2a2ac-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a2ac-136">RELATED LINKS</span></span>
