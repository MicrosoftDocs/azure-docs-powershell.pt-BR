---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111067"
---
# <span data-ttu-id="f2349-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f2349-101">Update-AzImage</span></span>

## <span data-ttu-id="f2349-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2349-102">SYNOPSIS</span></span>
<span data-ttu-id="f2349-103">Atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f2349-103">Updates an image.</span></span>

## <span data-ttu-id="f2349-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2349-104">SYNTAX</span></span>

### <span data-ttu-id="f2349-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2349-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2349-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f2349-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2349-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="f2349-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2349-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2349-108">DESCRIPTION</span></span>
<span data-ttu-id="f2349-109">O cmdlet **Update-AzImage** atualiza uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f2349-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="f2349-110">Atualmente, somente as Marcas podem ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="f2349-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="f2349-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2349-111">EXAMPLES</span></span>

### <span data-ttu-id="f2349-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2349-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="f2349-113">Esse comando atualiza o valor de Marca da imagem existente 'Imagem01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="f2349-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f2349-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2349-114">PARAMETERS</span></span>

### <span data-ttu-id="f2349-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2349-115">-AsJob</span></span>
<span data-ttu-id="f2349-116">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f2349-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f2349-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2349-117">-DefaultProfile</span></span>
<span data-ttu-id="f2349-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f2349-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2349-119">-Imagem</span><span class="sxs-lookup"><span data-stu-id="f2349-119">-Image</span></span>
<span data-ttu-id="f2349-120">Especifica um objeto de imagem local.</span><span class="sxs-lookup"><span data-stu-id="f2349-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="f2349-121">-NomedaImagem</span><span class="sxs-lookup"><span data-stu-id="f2349-121">-ImageName</span></span>
<span data-ttu-id="f2349-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f2349-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f2349-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2349-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2349-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2349-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2349-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2349-125">-ResourceId</span></span>
<span data-ttu-id="f2349-126">A ID do recurso da imagem</span><span class="sxs-lookup"><span data-stu-id="f2349-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="f2349-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2349-127">-Tag</span></span>
<span data-ttu-id="f2349-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="f2349-128">Resource tags</span></span>

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

### <span data-ttu-id="f2349-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f2349-129">-Confirm</span></span>
<span data-ttu-id="f2349-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2349-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2349-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2349-131">-WhatIf</span></span>
<span data-ttu-id="f2349-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f2349-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2349-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2349-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2349-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2349-134">CommonParameters</span></span>
<span data-ttu-id="f2349-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2349-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2349-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2349-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2349-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2349-137">INPUTS</span></span>

### <span data-ttu-id="f2349-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2349-138">System.String</span></span>

### <span data-ttu-id="f2349-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f2349-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f2349-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2349-140">OUTPUTS</span></span>

### <span data-ttu-id="f2349-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f2349-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f2349-142">Notas</span><span class="sxs-lookup"><span data-stu-id="f2349-142">NOTES</span></span>

## <span data-ttu-id="f2349-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2349-143">RELATED LINKS</span></span>
