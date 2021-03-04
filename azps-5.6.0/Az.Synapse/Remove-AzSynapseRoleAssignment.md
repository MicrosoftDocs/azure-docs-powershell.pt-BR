---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 4fbc25b919b7fbb3caa972f4e64467dee1df7116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892682"
---
# <span data-ttu-id="8a774-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8a774-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="8a774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a774-102">SYNOPSIS</span></span>
<span data-ttu-id="8a774-103">Exclui uma atribuição de função do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a774-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="8a774-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8a774-104">SYNTAX</span></span>

### <span data-ttu-id="8a774-105">RemoveByWorkspaceNameAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a774-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a774-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a774-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a774-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a774-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a774-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a774-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8a774-115">DESCRIPTION</span></span>
<span data-ttu-id="8a774-116">O cmdlet **Remove-AzSynapseRoleAssignment** exclui permanentemente uma atribuição de função do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a774-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="8a774-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a774-117">EXAMPLES</span></span>

### <span data-ttu-id="8a774-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a774-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="8a774-119">Este comando exclui uma atribuição de função do Azure Synapse Analytics com uma ID de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="8a774-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="8a774-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a774-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="8a774-121">Este comando exclui uma atribuição de função do Azure Synapse Analytics com um nome de função e um nome de entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="8a774-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="8a774-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8a774-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="8a774-123">Este comando exclui uma atribuição de função do Azure Synapse Analytics com uma ID de atribuição de função por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a774-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="8a774-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8a774-124">PARAMETERS</span></span>

### <span data-ttu-id="8a774-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a774-125">-AsJob</span></span>
<span data-ttu-id="8a774-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a774-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a774-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a774-127">-DefaultProfile</span></span>
<span data-ttu-id="8a774-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a774-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a774-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8a774-129">-ObjectId</span></span>
<span data-ttu-id="8a774-130">ObjectId do Azure AD da Entidade de Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="8a774-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a774-131">-PassThru</span></span>
<span data-ttu-id="8a774-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8a774-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8a774-133">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="8a774-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8a774-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="8a774-134">-RoleAssignmentId</span></span>
<span data-ttu-id="8a774-135">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="8a774-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8a774-136">-RoleDefinitionId</span></span>
<span data-ttu-id="8a774-137">ID da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="8a774-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8a774-138">-RoleDefinitionName</span></span>
<span data-ttu-id="8a774-139">Nome da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="8a774-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a774-140">-ServicePrincipalName</span></span>
<span data-ttu-id="8a774-141">ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a774-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="8a774-142">-SignInName</span></span>
<span data-ttu-id="8a774-143">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a774-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a774-144">-WorkspaceName</span></span>
<span data-ttu-id="8a774-145">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a774-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8a774-146">-WorkspaceObject</span></span>
<span data-ttu-id="8a774-147">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a774-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a774-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a774-148">-Confirm</span></span>
<span data-ttu-id="8a774-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a774-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a774-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a774-150">-WhatIf</span></span>
<span data-ttu-id="8a774-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a774-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a774-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a774-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a774-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a774-153">CommonParameters</span></span>
<span data-ttu-id="8a774-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a774-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a774-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a774-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a774-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a774-156">INPUTS</span></span>

### <span data-ttu-id="8a774-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8a774-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8a774-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8a774-158">OUTPUTS</span></span>

### <span data-ttu-id="8a774-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a774-159">System.Boolean</span></span>

## <span data-ttu-id="8a774-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="8a774-160">NOTES</span></span>

## <span data-ttu-id="8a774-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a774-161">RELATED LINKS</span></span>
