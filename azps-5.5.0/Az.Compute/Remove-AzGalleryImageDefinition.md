---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115470"
---
# <span data-ttu-id="24eca-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="24eca-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="24eca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24eca-102">SYNOPSIS</span></span>
<span data-ttu-id="24eca-103">Excluir uma definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="24eca-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="24eca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24eca-104">SYNTAX</span></span>

### <span data-ttu-id="24eca-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24eca-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24eca-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="24eca-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24eca-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="24eca-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24eca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="24eca-108">DESCRIPTION</span></span>
<span data-ttu-id="24eca-109">Excluir uma definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="24eca-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="24eca-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24eca-110">EXAMPLES</span></span>

### <span data-ttu-id="24eca-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24eca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="24eca-112">Remover a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="24eca-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="24eca-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24eca-113">PARAMETERS</span></span>

### <span data-ttu-id="24eca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24eca-114">-AsJob</span></span>
<span data-ttu-id="24eca-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="24eca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24eca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24eca-116">-DefaultProfile</span></span>
<span data-ttu-id="24eca-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24eca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24eca-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="24eca-118">-Force</span></span>
<span data-ttu-id="24eca-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="24eca-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24eca-120">-Nomeda Galeria</span><span class="sxs-lookup"><span data-stu-id="24eca-120">-GalleryName</span></span>
<span data-ttu-id="24eca-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="24eca-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24eca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24eca-122">-InputObject</span></span>
<span data-ttu-id="24eca-123">O objeto de definição de imagem da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="24eca-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24eca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="24eca-124">-Name</span></span>
<span data-ttu-id="24eca-125">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="24eca-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24eca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24eca-126">-ResourceGroupName</span></span>
<span data-ttu-id="24eca-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24eca-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="24eca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24eca-128">-ResourceId</span></span>
<span data-ttu-id="24eca-129">A ID do recurso para a definição de imagem da galeria</span><span class="sxs-lookup"><span data-stu-id="24eca-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="24eca-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="24eca-130">-Confirm</span></span>
<span data-ttu-id="24eca-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24eca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24eca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24eca-132">-WhatIf</span></span>
<span data-ttu-id="24eca-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="24eca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24eca-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24eca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24eca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24eca-135">CommonParameters</span></span>
<span data-ttu-id="24eca-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24eca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24eca-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24eca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24eca-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="24eca-138">INPUTS</span></span>

### <span data-ttu-id="24eca-139">System.String</span><span class="sxs-lookup"><span data-stu-id="24eca-139">System.String</span></span>

### <span data-ttu-id="24eca-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="24eca-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="24eca-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="24eca-141">OUTPUTS</span></span>

### <span data-ttu-id="24eca-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="24eca-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="24eca-143">Notas</span><span class="sxs-lookup"><span data-stu-id="24eca-143">NOTES</span></span>

## <span data-ttu-id="24eca-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24eca-144">RELATED LINKS</span></span>
