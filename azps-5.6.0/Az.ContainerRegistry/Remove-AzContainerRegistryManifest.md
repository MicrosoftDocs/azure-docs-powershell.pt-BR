---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886781"
---
# <span data-ttu-id="ac9a0-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="ac9a0-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="ac9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9a0-103">Exclua o manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="ac9a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac9a0-104">SYNTAX</span></span>

### <span data-ttu-id="ac9a0-105">ByManifestParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac9a0-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac9a0-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac9a0-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac9a0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac9a0-107">DESCRIPTION</span></span>
<span data-ttu-id="ac9a0-108">Exclua o manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-108">Delete ACR manifest.</span></span>
<span data-ttu-id="ac9a0-109">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="ac9a0-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="ac9a0-110">primeiro.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-110">first.</span></span>

## <span data-ttu-id="ac9a0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-111">EXAMPLES</span></span>

### <span data-ttu-id="ac9a0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac9a0-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="ac9a0-113">Excluir manifesto sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under Registry</span><span class="sxs-lookup"><span data-stu-id="ac9a0-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="ac9a0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ac9a0-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="ac9a0-115">Excluir manifesto com a marca mais recente para teste/busybox27 do repositório no Registro</span><span class="sxs-lookup"><span data-stu-id="ac9a0-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="ac9a0-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-116">PARAMETERS</span></span>

### <span data-ttu-id="ac9a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9a0-117">-DefaultProfile</span></span>
<span data-ttu-id="ac9a0-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9a0-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="ac9a0-119">-Manifest</span></span>
<span data-ttu-id="ac9a0-120">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9a0-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ac9a0-121">-RegistryName</span></span>
<span data-ttu-id="ac9a0-122">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-122">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9a0-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ac9a0-123">-RepositoryName</span></span>
<span data-ttu-id="ac9a0-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-124">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9a0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac9a0-125">-Tag</span></span>
<span data-ttu-id="ac9a0-126">Tag.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-126">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9a0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac9a0-127">-Confirm</span></span>
<span data-ttu-id="ac9a0-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9a0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9a0-129">-WhatIf</span></span>
<span data-ttu-id="ac9a0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9a0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9a0-132">CommonParameters</span></span>
<span data-ttu-id="ac9a0-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9a0-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac9a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9a0-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-135">INPUTS</span></span>

### <span data-ttu-id="ac9a0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ac9a0-136">System.String</span></span>

## <span data-ttu-id="ac9a0-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-137">OUTPUTS</span></span>

### <span data-ttu-id="ac9a0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac9a0-138">System.Boolean</span></span>

## <span data-ttu-id="ac9a0-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac9a0-139">NOTES</span></span>

## <span data-ttu-id="ac9a0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac9a0-140">RELATED LINKS</span></span>
