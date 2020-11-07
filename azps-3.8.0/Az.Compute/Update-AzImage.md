---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942663"
---
# <span data-ttu-id="bf23f-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="bf23f-101">Update-AzImage</span></span>

## <span data-ttu-id="bf23f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf23f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf23f-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="bf23f-103">Updates an image.</span></span>

## <span data-ttu-id="bf23f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf23f-104">SYNTAX</span></span>

### <span data-ttu-id="bf23f-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf23f-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf23f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bf23f-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf23f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bf23f-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf23f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf23f-108">DESCRIPTION</span></span>
<span data-ttu-id="bf23f-109">O cmdlet **Update-AzImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="bf23f-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="bf23f-110">No momento, somente as marcas podem ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="bf23f-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="bf23f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf23f-111">EXAMPLES</span></span>

### <span data-ttu-id="bf23f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf23f-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="bf23f-113">Este comando atualiza o valor da marca da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="bf23f-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bf23f-114">OS</span><span class="sxs-lookup"><span data-stu-id="bf23f-114">PARAMETERS</span></span>

### <span data-ttu-id="bf23f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf23f-115">-AsJob</span></span>
<span data-ttu-id="bf23f-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bf23f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bf23f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf23f-117">-DefaultProfile</span></span>
<span data-ttu-id="bf23f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf23f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf23f-119">-Imagem</span><span class="sxs-lookup"><span data-stu-id="bf23f-119">-Image</span></span>
<span data-ttu-id="bf23f-120">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="bf23f-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf23f-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bf23f-121">-ImageName</span></span>
<span data-ttu-id="bf23f-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="bf23f-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf23f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf23f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf23f-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf23f-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf23f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf23f-125">-ResourceId</span></span>
<span data-ttu-id="bf23f-126">A ID do recurso para a imagem</span><span class="sxs-lookup"><span data-stu-id="bf23f-126">The resource Id for the image</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf23f-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="bf23f-127">-Tag</span></span>
<span data-ttu-id="bf23f-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="bf23f-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf23f-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf23f-129">-Confirm</span></span>
<span data-ttu-id="bf23f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf23f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf23f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf23f-131">-WhatIf</span></span>
<span data-ttu-id="bf23f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf23f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf23f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf23f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf23f-134">CommonParameters</span></span>
<span data-ttu-id="bf23f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf23f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf23f-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf23f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf23f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf23f-137">INPUTS</span></span>

### <span data-ttu-id="bf23f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bf23f-138">System.String</span></span>

### <span data-ttu-id="bf23f-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="bf23f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="bf23f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf23f-140">OUTPUTS</span></span>

### <span data-ttu-id="bf23f-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="bf23f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="bf23f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf23f-142">NOTES</span></span>

## <span data-ttu-id="bf23f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf23f-143">RELATED LINKS</span></span>
