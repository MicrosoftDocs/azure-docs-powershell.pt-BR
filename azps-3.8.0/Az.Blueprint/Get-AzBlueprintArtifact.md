---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d8541285cb8cef0565a06715910ff5b8cc8cc392
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777301"
---
# <span data-ttu-id="1c352-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="1c352-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="1c352-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c352-102">SYNOPSIS</span></span>
<span data-ttu-id="1c352-103">Recuperar artefatos de uma definição de plano.</span><span class="sxs-lookup"><span data-stu-id="1c352-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="1c352-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c352-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c352-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c352-105">DESCRIPTION</span></span>
<span data-ttu-id="1c352-106">Recuperar artefatos de uma definição de plano.</span><span class="sxs-lookup"><span data-stu-id="1c352-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="1c352-107">Se uma versão de definição Blueprint não for especificada, a versão de rascunho será recuperada.</span><span class="sxs-lookup"><span data-stu-id="1c352-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="1c352-108">Caso não haja nenhuma versão de rascunho, a última definição de planta publicada é retornada.</span><span class="sxs-lookup"><span data-stu-id="1c352-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="1c352-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c352-109">EXAMPLES</span></span>

### <span data-ttu-id="1c352-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c352-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="1c352-111">Recuperar artefatos de uma definição de plano..</span><span class="sxs-lookup"><span data-stu-id="1c352-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="1c352-112">OS</span><span class="sxs-lookup"><span data-stu-id="1c352-112">PARAMETERS</span></span>

### <span data-ttu-id="1c352-113">-Artefatofile</span><span class="sxs-lookup"><span data-stu-id="1c352-113">-ArtifactFile</span></span>
<span data-ttu-id="1c352-114">Localização do arquivo de artefato em formato JSON em disco.</span><span class="sxs-lookup"><span data-stu-id="1c352-114">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-115">-Plano gráfico</span><span class="sxs-lookup"><span data-stu-id="1c352-115">-Blueprint</span></span>
<span data-ttu-id="1c352-116">Objeto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="1c352-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="1c352-117">-BlueprintVersion</span></span>
<span data-ttu-id="1c352-118">Versão do plano gráfico da qual obter os artefatos.</span><span class="sxs-lookup"><span data-stu-id="1c352-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c352-119">-DefaultProfile</span></span>
<span data-ttu-id="1c352-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c352-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-121">-Depende</span><span class="sxs-lookup"><span data-stu-id="1c352-121">-DependsOn</span></span>
<span data-ttu-id="1c352-122">Lista dos nomes dos artefatos que devem ser criados antes da criação do artefato atual.</span><span class="sxs-lookup"><span data-stu-id="1c352-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1c352-123">-Description</span></span>
<span data-ttu-id="1c352-124">Descrição do artefato.</span><span class="sxs-lookup"><span data-stu-id="1c352-124">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c352-125">-Name</span></span>
<span data-ttu-id="1c352-126">Nome do artefato</span><span class="sxs-lookup"><span data-stu-id="1c352-126">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1c352-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="1c352-128">ID da definição da definição da política.</span><span class="sxs-lookup"><span data-stu-id="1c352-128">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="1c352-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="1c352-130">Hashtable dos parâmetros a serem passados para o artefato de definição de política.</span><span class="sxs-lookup"><span data-stu-id="1c352-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c352-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c352-132">Nome do grupo de recursos no qual o artefato vai estar.</span><span class="sxs-lookup"><span data-stu-id="1c352-132">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1c352-133">-RoleDefinitionId</span></span>
<span data-ttu-id="1c352-134">Lista de definições de função</span><span class="sxs-lookup"><span data-stu-id="1c352-134">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="1c352-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="1c352-136">Lista de IDs de entidade de segurança de definição de função.</span><span class="sxs-lookup"><span data-stu-id="1c352-136">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1c352-137">-TemplateFile</span></span>
<span data-ttu-id="1c352-138">Localização do arquivo de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="1c352-138">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1c352-139">-TemplateParameterFile</span></span>
<span data-ttu-id="1c352-140">Localização do arquivo de parâmetro de modelo ARM no disco.</span><span class="sxs-lookup"><span data-stu-id="1c352-140">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-141">-Digite</span><span class="sxs-lookup"><span data-stu-id="1c352-141">-Type</span></span>
<span data-ttu-id="1c352-142">Tipo do artefato.</span><span class="sxs-lookup"><span data-stu-id="1c352-142">Type of the artifact.</span></span>
<span data-ttu-id="1c352-143">Há 3 tipos com suporte: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="1c352-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c352-144">-Confirm</span></span>
<span data-ttu-id="1c352-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c352-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c352-146">-WhatIf</span></span>
<span data-ttu-id="1c352-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c352-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c352-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c352-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c352-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c352-149">CommonParameters</span></span>
<span data-ttu-id="1c352-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c352-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1c352-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c352-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c352-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c352-152">INPUTS</span></span>

### <span data-ttu-id="1c352-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1c352-153">System.String</span></span>

### <span data-ttu-id="1c352-154">Microsoft. Azure. Commands. Blueprint. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="1c352-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="1c352-155">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1c352-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1c352-156">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1c352-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1c352-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c352-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1c352-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="1c352-158">System.String[]</span></span>

## <span data-ttu-id="1c352-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c352-159">OUTPUTS</span></span>

### <span data-ttu-id="1c352-160">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="1c352-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="1c352-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c352-161">NOTES</span></span>

## <span data-ttu-id="1c352-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c352-162">RELATED LINKS</span></span>
