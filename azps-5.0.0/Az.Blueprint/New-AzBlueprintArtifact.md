---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116104"
---
# <span data-ttu-id="0626d-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="0626d-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="0626d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0626d-102">SYNOPSIS</span></span>
<span data-ttu-id="0626d-103">Crie um novo artefato e salve-o em uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="0626d-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="0626d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0626d-104">SYNTAX</span></span>

### <span data-ttu-id="0626d-105">CreateTemplateArtifact (padrão)</span><span class="sxs-lookup"><span data-stu-id="0626d-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626d-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="0626d-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626d-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="0626d-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0626d-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="0626d-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0626d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0626d-109">DESCRIPTION</span></span>
<span data-ttu-id="0626d-110">Crie um novo artefato.</span><span class="sxs-lookup"><span data-stu-id="0626d-110">Create a new artifact.</span></span> <span data-ttu-id="0626d-111">Há duas maneiras de criar um artefato: por meio de um artefato JSON como um arquivo de entrada ou de fornecer parâmetros embutidos para o artefato.</span><span class="sxs-lookup"><span data-stu-id="0626d-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="0626d-112">Embora o método JSON não exija o tipo do método de parâmetro embutido que deve ser fornecido, o usuário deve fornecer o tipo do parâmetro artefato por tipo.</span><span class="sxs-lookup"><span data-stu-id="0626d-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="0626d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0626d-113">EXAMPLES</span></span>

### <span data-ttu-id="0626d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0626d-114">Example 1</span></span>
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

<span data-ttu-id="0626d-115">Crie um novo artefato por meio de um arquivo JSON de artefato.</span><span class="sxs-lookup"><span data-stu-id="0626d-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="0626d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0626d-116">Example 2</span></span>
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

<span data-ttu-id="0626d-117">Crie um novo artefato por meio de parâmetros embutidos.</span><span class="sxs-lookup"><span data-stu-id="0626d-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="0626d-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0626d-118">Example 3</span></span>
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

<span data-ttu-id="0626d-119">Crie um novo artefato por meio de um arquivo de modelo ARM.</span><span class="sxs-lookup"><span data-stu-id="0626d-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="0626d-120">OS</span><span class="sxs-lookup"><span data-stu-id="0626d-120">PARAMETERS</span></span>

### <span data-ttu-id="0626d-121">-Artefatofile</span><span class="sxs-lookup"><span data-stu-id="0626d-121">-ArtifactFile</span></span>
<span data-ttu-id="0626d-122">Localização do arquivo de artefato em formato JSON em disco.</span><span class="sxs-lookup"><span data-stu-id="0626d-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="0626d-123">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="0626d-123">-Blueprint</span></span>
<span data-ttu-id="0626d-124">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="0626d-124">Blueprint object.</span></span>

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

### <span data-ttu-id="0626d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0626d-125">-DefaultProfile</span></span>
<span data-ttu-id="0626d-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0626d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0626d-127">-Depende</span><span class="sxs-lookup"><span data-stu-id="0626d-127">-DependsOn</span></span>
<span data-ttu-id="0626d-128">Lista dos nomes dos artefatos que devem ser criados antes da criação do artefato atual.</span><span class="sxs-lookup"><span data-stu-id="0626d-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="0626d-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0626d-129">-Description</span></span>
<span data-ttu-id="0626d-130">Descrição do artefato.</span><span class="sxs-lookup"><span data-stu-id="0626d-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="0626d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0626d-131">-Name</span></span>
<span data-ttu-id="0626d-132">Nome do artefato</span><span class="sxs-lookup"><span data-stu-id="0626d-132">Name of the artifact</span></span>

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

### <span data-ttu-id="0626d-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0626d-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="0626d-134">ID da definição da definição da política.</span><span class="sxs-lookup"><span data-stu-id="0626d-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="0626d-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="0626d-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="0626d-136">Hashtable dos parâmetros a serem passados para o artefato de definição de política.</span><span class="sxs-lookup"><span data-stu-id="0626d-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="0626d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0626d-137">-ResourceGroupName</span></span>
<span data-ttu-id="0626d-138">Nome do grupo de recursos no qual o artefato vai estar.</span><span class="sxs-lookup"><span data-stu-id="0626d-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="0626d-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0626d-139">-RoleDefinitionId</span></span>
<span data-ttu-id="0626d-140">Lista de definições de função</span><span class="sxs-lookup"><span data-stu-id="0626d-140">List of role definition</span></span>

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

### <span data-ttu-id="0626d-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="0626d-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="0626d-142">Lista de IDs de entidade de segurança de definição de função.</span><span class="sxs-lookup"><span data-stu-id="0626d-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="0626d-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0626d-143">-TemplateFile</span></span>
<span data-ttu-id="0626d-144">Localização do arquivo de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="0626d-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="0626d-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0626d-145">-TemplateParameterFile</span></span>
<span data-ttu-id="0626d-146">Localização do arquivo de parâmetro de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="0626d-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="0626d-147">-Digite</span><span class="sxs-lookup"><span data-stu-id="0626d-147">-Type</span></span>
<span data-ttu-id="0626d-148">Tipo do artefato.</span><span class="sxs-lookup"><span data-stu-id="0626d-148">Type of the artifact.</span></span>
<span data-ttu-id="0626d-149">Há 3 tipos com suporte: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="0626d-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="0626d-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0626d-150">-Confirm</span></span>
<span data-ttu-id="0626d-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0626d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0626d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0626d-152">-WhatIf</span></span>
<span data-ttu-id="0626d-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0626d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0626d-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0626d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0626d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0626d-155">CommonParameters</span></span>
<span data-ttu-id="0626d-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0626d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0626d-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0626d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0626d-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0626d-158">INPUTS</span></span>

### <span data-ttu-id="0626d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="0626d-159">System.String</span></span>

### <span data-ttu-id="0626d-160">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="0626d-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="0626d-161">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="0626d-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="0626d-162">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0626d-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0626d-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0626d-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0626d-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="0626d-164">System.String[]</span></span>

## <span data-ttu-id="0626d-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0626d-165">OUTPUTS</span></span>

### <span data-ttu-id="0626d-166">Microsoft. Azure. Management. Blueprint. Models. artefato</span><span class="sxs-lookup"><span data-stu-id="0626d-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="0626d-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0626d-167">NOTES</span></span>

## <span data-ttu-id="0626d-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0626d-168">RELATED LINKS</span></span>
