---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127085"
---
# <span data-ttu-id="a7d62-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="a7d62-101">Remove-AzGallery</span></span>

## <span data-ttu-id="a7d62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7d62-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d62-103">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="a7d62-103">Delete a gallery.</span></span>

## <span data-ttu-id="a7d62-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d62-104">SYNTAX</span></span>

### <span data-ttu-id="a7d62-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7d62-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7d62-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a7d62-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7d62-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="a7d62-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d62-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7d62-108">DESCRIPTION</span></span>
<span data-ttu-id="a7d62-109">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="a7d62-109">Delete a gallery.</span></span>

## <span data-ttu-id="a7d62-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7d62-110">EXAMPLES</span></span>

### <span data-ttu-id="a7d62-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7d62-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="a7d62-112">Exclua a galeria determinada.</span><span class="sxs-lookup"><span data-stu-id="a7d62-112">Delete the given gallery.</span></span>

## <span data-ttu-id="a7d62-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d62-113">PARAMETERS</span></span>

### <span data-ttu-id="a7d62-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7d62-114">-AsJob</span></span>
<span data-ttu-id="a7d62-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7d62-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7d62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d62-116">-DefaultProfile</span></span>
<span data-ttu-id="a7d62-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d62-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a7d62-118">-Force</span></span>
<span data-ttu-id="a7d62-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7d62-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7d62-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7d62-120">-InputObject</span></span>
<span data-ttu-id="a7d62-121">O objeto da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="a7d62-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d62-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7d62-122">-Name</span></span>
<span data-ttu-id="a7d62-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7d62-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d62-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7d62-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7d62-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7d62-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7d62-126">-ResourceId</span></span>
<span data-ttu-id="a7d62-127">A ID do recurso da galeria</span><span class="sxs-lookup"><span data-stu-id="a7d62-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="a7d62-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a7d62-128">-Confirm</span></span>
<span data-ttu-id="a7d62-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d62-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d62-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d62-130">-WhatIf</span></span>
<span data-ttu-id="a7d62-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a7d62-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7d62-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7d62-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d62-133">CommonParameters</span></span>
<span data-ttu-id="a7d62-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d62-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d62-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d62-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7d62-136">INPUTS</span></span>

### <span data-ttu-id="a7d62-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d62-137">System.String</span></span>

### <span data-ttu-id="a7d62-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="a7d62-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="a7d62-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7d62-139">OUTPUTS</span></span>

### <span data-ttu-id="a7d62-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a7d62-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a7d62-141">Notas</span><span class="sxs-lookup"><span data-stu-id="a7d62-141">NOTES</span></span>

## <span data-ttu-id="a7d62-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7d62-142">RELATED LINKS</span></span>
