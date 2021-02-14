---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116496"
---
# <span data-ttu-id="3feaa-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="3feaa-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="3feaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3feaa-102">SYNOPSIS</span></span>
<span data-ttu-id="3feaa-103">Excluir manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="3feaa-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="3feaa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3feaa-104">SYNTAX</span></span>

### <span data-ttu-id="3feaa-105">ByManifestParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3feaa-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3feaa-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="3feaa-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3feaa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3feaa-107">DESCRIPTION</span></span>
<span data-ttu-id="3feaa-108">Excluir manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="3feaa-108">Delete ACR manifest.</span></span>
<span data-ttu-id="3feaa-109">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="3feaa-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="3feaa-110">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="3feaa-110">first.</span></span>

## <span data-ttu-id="3feaa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3feaa-111">EXAMPLES</span></span>

### <span data-ttu-id="3feaa-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3feaa-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="3feaa-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="3feaa-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="3feaa-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3feaa-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="3feaa-115">Excluir manifesto com a marca mais recente para o teste do repositório/busybox27 em Registro</span><span class="sxs-lookup"><span data-stu-id="3feaa-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="3feaa-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3feaa-116">PARAMETERS</span></span>

### <span data-ttu-id="3feaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3feaa-117">-DefaultProfile</span></span>
<span data-ttu-id="3feaa-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3feaa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3feaa-119">-Manifesto</span><span class="sxs-lookup"><span data-stu-id="3feaa-119">-Manifest</span></span>
<span data-ttu-id="3feaa-120">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="3feaa-120">Manifest reference.</span></span>

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

### <span data-ttu-id="3feaa-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3feaa-121">-RegistryName</span></span>
<span data-ttu-id="3feaa-122">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="3feaa-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="3feaa-123">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="3feaa-123">-RepositoryName</span></span>
<span data-ttu-id="3feaa-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="3feaa-124">Repository Name.</span></span>

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

### <span data-ttu-id="3feaa-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3feaa-125">-Tag</span></span>
<span data-ttu-id="3feaa-126">Tag.</span><span class="sxs-lookup"><span data-stu-id="3feaa-126">Tag.</span></span>

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

### <span data-ttu-id="3feaa-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3feaa-127">-Confirm</span></span>
<span data-ttu-id="3feaa-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3feaa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3feaa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3feaa-129">-WhatIf</span></span>
<span data-ttu-id="3feaa-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3feaa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3feaa-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3feaa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3feaa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3feaa-132">CommonParameters</span></span>
<span data-ttu-id="3feaa-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3feaa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3feaa-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3feaa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3feaa-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="3feaa-135">INPUTS</span></span>

### <span data-ttu-id="3feaa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3feaa-136">System.String</span></span>

## <span data-ttu-id="3feaa-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="3feaa-137">OUTPUTS</span></span>

### <span data-ttu-id="3feaa-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3feaa-138">System.Boolean</span></span>

## <span data-ttu-id="3feaa-139">Notas</span><span class="sxs-lookup"><span data-stu-id="3feaa-139">NOTES</span></span>

## <span data-ttu-id="3feaa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3feaa-140">RELATED LINKS</span></span>
