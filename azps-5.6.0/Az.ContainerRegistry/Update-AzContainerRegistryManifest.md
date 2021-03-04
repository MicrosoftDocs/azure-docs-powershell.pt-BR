---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885922"
---
# <span data-ttu-id="47512-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="47512-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="47512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47512-102">SYNOPSIS</span></span>
<span data-ttu-id="47512-103">Atualizar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="47512-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="47512-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47512-104">SYNTAX</span></span>

### <span data-ttu-id="47512-105">ByManifestParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47512-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47512-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="47512-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47512-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47512-107">DESCRIPTION</span></span>
<span data-ttu-id="47512-108">Atualizar manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="47512-108">Update ACR manifest.</span></span>
<span data-ttu-id="47512-109">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="47512-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="47512-110">primeiro.</span><span class="sxs-lookup"><span data-stu-id="47512-110">first.</span></span>

## <span data-ttu-id="47512-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47512-111">EXAMPLES</span></span>

### <span data-ttu-id="47512-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47512-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="47512-113">Atributos de atualização para manifesto sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 no Registro.</span><span class="sxs-lookup"><span data-stu-id="47512-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="47512-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47512-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="47512-115">Atualizar atributos para manifesto com a marca mais recente no Registro.</span><span class="sxs-lookup"><span data-stu-id="47512-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="47512-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47512-116">PARAMETERS</span></span>

### <span data-ttu-id="47512-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47512-117">-DefaultProfile</span></span>
<span data-ttu-id="47512-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47512-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47512-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="47512-119">-DeleteEnabled</span></span>
<span data-ttu-id="47512-120">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="47512-120">Delete enable.</span></span>

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

### <span data-ttu-id="47512-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="47512-121">-ListEnabled</span></span>
<span data-ttu-id="47512-122">Listar habilitada.</span><span class="sxs-lookup"><span data-stu-id="47512-122">List enable.</span></span>

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

### <span data-ttu-id="47512-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="47512-123">-Manifest</span></span>
<span data-ttu-id="47512-124">Referência de manifesto.</span><span class="sxs-lookup"><span data-stu-id="47512-124">Manifest reference.</span></span>

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

### <span data-ttu-id="47512-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="47512-125">-ReadEnabled</span></span>
<span data-ttu-id="47512-126">Ler habilitar.</span><span class="sxs-lookup"><span data-stu-id="47512-126">Read enable.</span></span>

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

### <span data-ttu-id="47512-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="47512-127">-RegistryName</span></span>
<span data-ttu-id="47512-128">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="47512-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="47512-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="47512-129">-RepositoryName</span></span>
<span data-ttu-id="47512-130">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="47512-130">Repository Name.</span></span>

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

### <span data-ttu-id="47512-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="47512-131">-Tag</span></span>
<span data-ttu-id="47512-132">Tag.</span><span class="sxs-lookup"><span data-stu-id="47512-132">Tag.</span></span>

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

### <span data-ttu-id="47512-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="47512-133">-WriteEnabled</span></span>
<span data-ttu-id="47512-134">Gravar habilitado.</span><span class="sxs-lookup"><span data-stu-id="47512-134">Write enable.</span></span>

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

### <span data-ttu-id="47512-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47512-135">-Confirm</span></span>
<span data-ttu-id="47512-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47512-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47512-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47512-137">-WhatIf</span></span>
<span data-ttu-id="47512-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47512-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47512-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47512-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47512-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47512-140">CommonParameters</span></span>
<span data-ttu-id="47512-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47512-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47512-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47512-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47512-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47512-143">INPUTS</span></span>

### <span data-ttu-id="47512-144">System.String</span><span class="sxs-lookup"><span data-stu-id="47512-144">System.String</span></span>

## <span data-ttu-id="47512-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47512-145">OUTPUTS</span></span>

### <span data-ttu-id="47512-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="47512-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="47512-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="47512-147">NOTES</span></span>

## <span data-ttu-id="47512-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47512-148">RELATED LINKS</span></span>
