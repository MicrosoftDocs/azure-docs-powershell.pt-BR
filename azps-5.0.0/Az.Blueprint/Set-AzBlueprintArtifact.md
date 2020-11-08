---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116092"
---
# <span data-ttu-id="c5691-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="c5691-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="c5691-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5691-102">SYNOPSIS</span></span>
<span data-ttu-id="c5691-103">Atualize um artefato em uma definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="c5691-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="c5691-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5691-104">SYNTAX</span></span>

### <span data-ttu-id="c5691-105">UpdateTemplateArtifact (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5691-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5691-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="c5691-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5691-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="c5691-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5691-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="c5691-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5691-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5691-109">DESCRIPTION</span></span>
<span data-ttu-id="c5691-110">Atualizar um artefato.</span><span class="sxs-lookup"><span data-stu-id="c5691-110">Update an artifact.</span></span> <span data-ttu-id="c5691-111">Há duas maneiras de atualizar um artefato: por meio de um artefato JSON como um arquivo de entrada ou de fornecer parâmetros embutidos para o artefato.</span><span class="sxs-lookup"><span data-stu-id="c5691-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="c5691-112">Embora o método JSON não exija o tipo do método de parâmetro embutido que deve ser fornecido, o usuário deve fornecer o tipo do parâmetro artefato por tipo.</span><span class="sxs-lookup"><span data-stu-id="c5691-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="c5691-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5691-113">EXAMPLES</span></span>

### <span data-ttu-id="c5691-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5691-114">Example 1</span></span>
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

<span data-ttu-id="c5691-115">Atualize um artefato por meio de um arquivo JSON de artefato.</span><span class="sxs-lookup"><span data-stu-id="c5691-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="c5691-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5691-116">Example 2</span></span>
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

<span data-ttu-id="c5691-117">Atualize um artefato por meio de parâmetros embutidos.</span><span class="sxs-lookup"><span data-stu-id="c5691-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="c5691-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5691-118">Example 3</span></span>
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

<span data-ttu-id="c5691-119">Atualizar um artefato por meio de um arquivo de modelo ARM.</span><span class="sxs-lookup"><span data-stu-id="c5691-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="c5691-120">OS</span><span class="sxs-lookup"><span data-stu-id="c5691-120">PARAMETERS</span></span>

### <span data-ttu-id="c5691-121">-Artefatofile</span><span class="sxs-lookup"><span data-stu-id="c5691-121">-ArtifactFile</span></span>
<span data-ttu-id="c5691-122">Localização do arquivo de artefato em formato JSON em disco.</span><span class="sxs-lookup"><span data-stu-id="c5691-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-123">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="c5691-123">-Blueprint</span></span>
<span data-ttu-id="c5691-124">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="c5691-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5691-125">-DefaultProfile</span></span>
<span data-ttu-id="c5691-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5691-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5691-127">-Depende</span><span class="sxs-lookup"><span data-stu-id="c5691-127">-DependsOn</span></span>
<span data-ttu-id="c5691-128">Lista dos nomes dos artefatos que devem ser criados antes da criação do artefato atual.</span><span class="sxs-lookup"><span data-stu-id="c5691-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c5691-129">-Description</span></span>
<span data-ttu-id="c5691-130">Descrição do artefato.</span><span class="sxs-lookup"><span data-stu-id="c5691-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5691-131">-Name</span></span>
<span data-ttu-id="c5691-132">Nome do artefato</span><span class="sxs-lookup"><span data-stu-id="c5691-132">Name of the artifact</span></span>

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

### <span data-ttu-id="c5691-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c5691-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="c5691-134">ID da definição da definição da política.</span><span class="sxs-lookup"><span data-stu-id="c5691-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="c5691-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="c5691-136">Hashtable dos parâmetros a serem passados para o artefato de definição de política.</span><span class="sxs-lookup"><span data-stu-id="c5691-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5691-137">-ResourceGroupName</span></span>
<span data-ttu-id="c5691-138">Nome do grupo de recursos no qual o artefato vai estar.</span><span class="sxs-lookup"><span data-stu-id="c5691-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c5691-139">-RoleDefinitionId</span></span>
<span data-ttu-id="c5691-140">Lista de definições de função</span><span class="sxs-lookup"><span data-stu-id="c5691-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="c5691-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="c5691-142">Lista de IDs de entidade de segurança de definição de função.</span><span class="sxs-lookup"><span data-stu-id="c5691-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c5691-143">-TemplateFile</span></span>
<span data-ttu-id="c5691-144">Localização do arquivo de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="c5691-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c5691-145">-TemplateParameterFile</span></span>
<span data-ttu-id="c5691-146">Localização do arquivo de parâmetro de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="c5691-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-147">-Digite</span><span class="sxs-lookup"><span data-stu-id="c5691-147">-Type</span></span>
<span data-ttu-id="c5691-148">Tipo do artefato.</span><span class="sxs-lookup"><span data-stu-id="c5691-148">Type of the artifact.</span></span>
<span data-ttu-id="c5691-149">Há 3 tipos com suporte: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="c5691-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5691-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5691-150">-Confirm</span></span>
<span data-ttu-id="c5691-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5691-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5691-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5691-152">-WhatIf</span></span>
<span data-ttu-id="c5691-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5691-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5691-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5691-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5691-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5691-155">CommonParameters</span></span>
<span data-ttu-id="c5691-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5691-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5691-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5691-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5691-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5691-158">INPUTS</span></span>

### <span data-ttu-id="c5691-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c5691-159">System.String</span></span>

### <span data-ttu-id="c5691-160">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="c5691-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="c5691-161">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c5691-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c5691-162">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c5691-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c5691-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5691-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c5691-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="c5691-164">System.String[]</span></span>

## <span data-ttu-id="c5691-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5691-165">OUTPUTS</span></span>

### <span data-ttu-id="c5691-166">Microsoft. Azure. Management. Blueprint. Models. artefato</span><span class="sxs-lookup"><span data-stu-id="c5691-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="c5691-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5691-167">NOTES</span></span>

## <span data-ttu-id="c5691-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5691-168">RELATED LINKS</span></span>
