---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 10302f75bcbdb24c838f7785804368fd4716da87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771081"
---
# <span data-ttu-id="21dec-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="21dec-101">Update-AzImage</span></span>

## <span data-ttu-id="21dec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21dec-102">SYNOPSIS</span></span>
<span data-ttu-id="21dec-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="21dec-103">Updates an image.</span></span>

## <span data-ttu-id="21dec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21dec-104">SYNTAX</span></span>

### <span data-ttu-id="21dec-105">ObjectParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="21dec-105">ObjectParameter (Default)</span></span>
```
Update-AzImage [-Image] <PSImage> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21dec-106">Defaultparameter</span><span class="sxs-lookup"><span data-stu-id="21dec-106">DefaultParameter</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [[-Image] <PSImage>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21dec-107">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="21dec-107">ResourceIdParameter</span></span>
```
Update-AzImage [-ResourceId] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21dec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21dec-108">DESCRIPTION</span></span>
<span data-ttu-id="21dec-109">O cmdlet **Update-AzImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="21dec-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="21dec-110">No momento, somente as marcas podem ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="21dec-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="21dec-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21dec-111">EXAMPLES</span></span>

### <span data-ttu-id="21dec-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21dec-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="21dec-113">Este comando atualiza o valor da marca da imagem existente ' Image01 ' no grupo de recursos ' ResourceGroup01 '.</span><span class="sxs-lookup"><span data-stu-id="21dec-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="21dec-114">OS</span><span class="sxs-lookup"><span data-stu-id="21dec-114">PARAMETERS</span></span>

### <span data-ttu-id="21dec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21dec-115">-AsJob</span></span>
<span data-ttu-id="21dec-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="21dec-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="21dec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21dec-117">-DefaultProfile</span></span>
<span data-ttu-id="21dec-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21dec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21dec-119">-Imagem</span><span class="sxs-lookup"><span data-stu-id="21dec-119">-Image</span></span>
<span data-ttu-id="21dec-120">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="21dec-120">Specifies a local image object.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21dec-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="21dec-121">-ImageName</span></span>
<span data-ttu-id="21dec-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="21dec-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="21dec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21dec-123">-ResourceGroupName</span></span>
<span data-ttu-id="21dec-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21dec-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21dec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21dec-125">-ResourceId</span></span>
<span data-ttu-id="21dec-126">A ID do recurso para a imagem</span><span class="sxs-lookup"><span data-stu-id="21dec-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="21dec-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="21dec-127">-Tag</span></span>
<span data-ttu-id="21dec-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="21dec-128">Resource tags</span></span>

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

### <span data-ttu-id="21dec-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21dec-129">-Confirm</span></span>
<span data-ttu-id="21dec-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21dec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21dec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21dec-131">-WhatIf</span></span>
<span data-ttu-id="21dec-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21dec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21dec-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21dec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21dec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21dec-134">CommonParameters</span></span>
<span data-ttu-id="21dec-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21dec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21dec-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21dec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21dec-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21dec-137">INPUTS</span></span>

### <span data-ttu-id="21dec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="21dec-138">System.String</span></span>

### <span data-ttu-id="21dec-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="21dec-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="21dec-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21dec-140">OUTPUTS</span></span>

### <span data-ttu-id="21dec-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="21dec-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="21dec-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21dec-142">NOTES</span></span>

## <span data-ttu-id="21dec-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21dec-143">RELATED LINKS</span></span>
