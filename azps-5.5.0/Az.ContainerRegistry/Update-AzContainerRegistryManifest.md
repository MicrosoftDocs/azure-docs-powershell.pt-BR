---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 85623106a932ba9419da0c07cc4bcb6c52e5e838
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111049"
---
# <span data-ttu-id="38744-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="38744-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="38744-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38744-102">SYNOPSIS</span></span>
<span data-ttu-id="38744-103">Atualizar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="38744-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="38744-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38744-104">SYNTAX</span></span>

### <span data-ttu-id="38744-105">ByManifestParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38744-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38744-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="38744-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38744-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="38744-107">DESCRIPTION</span></span>
<span data-ttu-id="38744-108">Atualizar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="38744-108">Update ACR manifest.</span></span>
<span data-ttu-id="38744-109">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="38744-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="38744-110">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="38744-110">first.</span></span>

## <span data-ttu-id="38744-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38744-111">EXAMPLES</span></span>

### <span data-ttu-id="38744-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38744-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="38744-113">Atributos de atualização para manifesto sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 sob registro.</span><span class="sxs-lookup"><span data-stu-id="38744-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="38744-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38744-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="38744-115">Atualizar atributos para manifesto com marca mais recente no Registro.</span><span class="sxs-lookup"><span data-stu-id="38744-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="38744-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38744-116">PARAMETERS</span></span>

### <span data-ttu-id="38744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38744-117">-DefaultProfile</span></span>
<span data-ttu-id="38744-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38744-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38744-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="38744-119">-DeleteEnabled</span></span>
<span data-ttu-id="38744-120">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="38744-120">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38744-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="38744-121">-ListEnabled</span></span>
<span data-ttu-id="38744-122">Habilitar lista.</span><span class="sxs-lookup"><span data-stu-id="38744-122">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38744-123">-Manifesto</span><span class="sxs-lookup"><span data-stu-id="38744-123">-Manifest</span></span>
<span data-ttu-id="38744-124">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="38744-124">Manifest reference.</span></span>

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

### <span data-ttu-id="38744-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="38744-125">-ReadEnabled</span></span>
<span data-ttu-id="38744-126">Habilitar leitura.</span><span class="sxs-lookup"><span data-stu-id="38744-126">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38744-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="38744-127">-RegistryName</span></span>
<span data-ttu-id="38744-128">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="38744-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="38744-129">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="38744-129">-RepositoryName</span></span>
<span data-ttu-id="38744-130">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="38744-130">Repository Name.</span></span>

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

### <span data-ttu-id="38744-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="38744-131">-Tag</span></span>
<span data-ttu-id="38744-132">Tag.</span><span class="sxs-lookup"><span data-stu-id="38744-132">Tag.</span></span>

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

### <span data-ttu-id="38744-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="38744-133">-WriteEnabled</span></span>
<span data-ttu-id="38744-134">Habilitar gravação.</span><span class="sxs-lookup"><span data-stu-id="38744-134">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38744-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="38744-135">-Confirm</span></span>
<span data-ttu-id="38744-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38744-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38744-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38744-137">-WhatIf</span></span>
<span data-ttu-id="38744-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="38744-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38744-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38744-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38744-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38744-140">CommonParameters</span></span>
<span data-ttu-id="38744-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38744-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38744-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38744-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38744-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="38744-143">INPUTS</span></span>

### <span data-ttu-id="38744-144">System.String</span><span class="sxs-lookup"><span data-stu-id="38744-144">System.String</span></span>

## <span data-ttu-id="38744-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="38744-145">OUTPUTS</span></span>

### <span data-ttu-id="38744-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="38744-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="38744-147">Notas</span><span class="sxs-lookup"><span data-stu-id="38744-147">NOTES</span></span>

## <span data-ttu-id="38744-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38744-148">RELATED LINKS</span></span>
