---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
ms.openlocfilehash: 2711b5398f3d10f894214473f6ff68045748af22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430366"
---
# <span data-ttu-id="2637e-101">Remove-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="2637e-101">Remove-AzureRmGallery</span></span>

## <span data-ttu-id="2637e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2637e-102">SYNOPSIS</span></span>
<span data-ttu-id="2637e-103">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="2637e-103">Delete a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2637e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2637e-104">SYNTAX</span></span>

### <span data-ttu-id="2637e-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2637e-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2637e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2637e-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2637e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2637e-107">ObjectParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2637e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2637e-108">DESCRIPTION</span></span>
<span data-ttu-id="2637e-109">Excluir uma galeria.</span><span class="sxs-lookup"><span data-stu-id="2637e-109">Delete a gallery.</span></span>

## <span data-ttu-id="2637e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2637e-110">EXAMPLES</span></span>

### <span data-ttu-id="2637e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2637e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="2637e-112">Excluir a Galeria fornecida.</span><span class="sxs-lookup"><span data-stu-id="2637e-112">Delete the given gallery.</span></span>

## <span data-ttu-id="2637e-113">OS</span><span class="sxs-lookup"><span data-stu-id="2637e-113">PARAMETERS</span></span>

### <span data-ttu-id="2637e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2637e-114">-AsJob</span></span>
<span data-ttu-id="2637e-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2637e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2637e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2637e-116">-DefaultProfile</span></span>
<span data-ttu-id="2637e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2637e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2637e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2637e-118">-Force</span></span>
<span data-ttu-id="2637e-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2637e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2637e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2637e-120">-InputObject</span></span>
<span data-ttu-id="2637e-121">O objeto da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="2637e-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="2637e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2637e-122">-Name</span></span>
<span data-ttu-id="2637e-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="2637e-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="2637e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2637e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2637e-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2637e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="2637e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2637e-126">-ResourceId</span></span>
<span data-ttu-id="2637e-127">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="2637e-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="2637e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2637e-128">-Confirm</span></span>
<span data-ttu-id="2637e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2637e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2637e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2637e-130">-WhatIf</span></span>
<span data-ttu-id="2637e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2637e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2637e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2637e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2637e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2637e-133">CommonParameters</span></span>
<span data-ttu-id="2637e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2637e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2637e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2637e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2637e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2637e-136">INPUTS</span></span>

### <span data-ttu-id="2637e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2637e-137">System.String</span></span>

### <span data-ttu-id="2637e-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="2637e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="2637e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2637e-139">OUTPUTS</span></span>

### <span data-ttu-id="2637e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2637e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2637e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2637e-141">NOTES</span></span>

## <span data-ttu-id="2637e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2637e-142">RELATED LINKS</span></span>
