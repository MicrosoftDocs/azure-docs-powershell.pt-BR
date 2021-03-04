---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 82d0d3667371485d079785dbdb2f87eb8284aa94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885743"
---
# <span data-ttu-id="c355c-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="c355c-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="c355c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c355c-102">SYNOPSIS</span></span>
<span data-ttu-id="c355c-103">Crie um novo artefato e salve-o dentro de uma definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="c355c-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="c355c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c355c-104">SYNTAX</span></span>

### <span data-ttu-id="c355c-105">CreateTemplateArtifact (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c355c-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c355c-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="c355c-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c355c-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="c355c-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c355c-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="c355c-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c355c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c355c-109">DESCRIPTION</span></span>
<span data-ttu-id="c355c-110">Crie um novo artefato.</span><span class="sxs-lookup"><span data-stu-id="c355c-110">Create a new artifact.</span></span> <span data-ttu-id="c355c-111">Há duas maneiras de criar um artefato: por meio de um JSON de artefato como um arquivo de entrada ou fornecendo parâmetros em linha para o artefato.</span><span class="sxs-lookup"><span data-stu-id="c355c-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="c355c-112">Embora o método JSON não exija o tipo do artefato a ser fornecido, o método de parâmetro em linha requer que o usuário forneça o tipo do artefato por meio do parâmetro -Type.</span><span class="sxs-lookup"><span data-stu-id="c355c-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="c355c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c355c-113">EXAMPLES</span></span>

### <span data-ttu-id="c355c-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c355c-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="c355c-115">Crie um novo artefato por meio de um arquivo JSON de artefato.</span><span class="sxs-lookup"><span data-stu-id="c355c-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="c355c-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c355c-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="c355c-117">Crie um novo artefato por meio de parâmetros em linha.</span><span class="sxs-lookup"><span data-stu-id="c355c-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="c355c-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c355c-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="c355c-119">Crie um novo artefato por meio de um arquivo ARM modelo.</span><span class="sxs-lookup"><span data-stu-id="c355c-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="c355c-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c355c-120">PARAMETERS</span></span>

### <span data-ttu-id="c355c-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="c355c-121">-ArtifactFile</span></span>
<span data-ttu-id="c355c-122">Local do arquivo de artefato no formato JSON no disco.</span><span class="sxs-lookup"><span data-stu-id="c355c-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="c355c-123">-Blueprint</span></span>
<span data-ttu-id="c355c-124">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="c355c-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c355c-125">-DefaultProfile</span></span>
<span data-ttu-id="c355c-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c355c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c355c-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="c355c-127">-DependsOn</span></span>
<span data-ttu-id="c355c-128">Lista dos nomes de artefatos que precisam ser criados antes que o artefato atual seja criado.</span><span class="sxs-lookup"><span data-stu-id="c355c-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-129">-Description</span><span class="sxs-lookup"><span data-stu-id="c355c-129">-Description</span></span>
<span data-ttu-id="c355c-130">Descrição do artefato.</span><span class="sxs-lookup"><span data-stu-id="c355c-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c355c-131">-Name</span></span>
<span data-ttu-id="c355c-132">Nome do artefato</span><span class="sxs-lookup"><span data-stu-id="c355c-132">Name of the artifact</span></span>

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

### <span data-ttu-id="c355c-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c355c-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="c355c-134">ID de definição da definição de política.</span><span class="sxs-lookup"><span data-stu-id="c355c-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="c355c-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="c355c-136">Hashtable de parâmetros para passar para o artefato de definição de política.</span><span class="sxs-lookup"><span data-stu-id="c355c-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c355c-137">-ResourceGroupName</span></span>
<span data-ttu-id="c355c-138">Nome do grupo de recursos em que o artefato estará.</span><span class="sxs-lookup"><span data-stu-id="c355c-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c355c-139">-RoleDefinitionId</span></span>
<span data-ttu-id="c355c-140">Lista de definição de função</span><span class="sxs-lookup"><span data-stu-id="c355c-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="c355c-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="c355c-142">Lista de IDs principais de definição de função.</span><span class="sxs-lookup"><span data-stu-id="c355c-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c355c-143">-TemplateFile</span></span>
<span data-ttu-id="c355c-144">Local do arquivo ARM de modelo no disco.</span><span class="sxs-lookup"><span data-stu-id="c355c-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c355c-145">-TemplateParameterFile</span></span>
<span data-ttu-id="c355c-146">Local do arquivo de parâmetro ARM modelo no disco.</span><span class="sxs-lookup"><span data-stu-id="c355c-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-147">-Type</span><span class="sxs-lookup"><span data-stu-id="c355c-147">-Type</span></span>
<span data-ttu-id="c355c-148">Tipo do artefato.</span><span class="sxs-lookup"><span data-stu-id="c355c-148">Type of the artifact.</span></span>
<span data-ttu-id="c355c-149">Há três tipos com suporte: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="c355c-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c355c-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c355c-150">-Confirm</span></span>
<span data-ttu-id="c355c-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c355c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c355c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c355c-152">-WhatIf</span></span>
<span data-ttu-id="c355c-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c355c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c355c-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c355c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c355c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c355c-155">CommonParameters</span></span>
<span data-ttu-id="c355c-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c355c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c355c-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c355c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c355c-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c355c-158">INPUTS</span></span>

### <span data-ttu-id="c355c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c355c-159">System.String</span></span>

### <span data-ttu-id="c355c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="c355c-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="c355c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c355c-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c355c-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c355c-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c355c-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c355c-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c355c-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c355c-164">System.String[]</span></span>

## <span data-ttu-id="c355c-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c355c-165">OUTPUTS</span></span>

### <span data-ttu-id="c355c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="c355c-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="c355c-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="c355c-167">NOTES</span></span>

## <span data-ttu-id="c355c-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c355c-168">RELATED LINKS</span></span>
