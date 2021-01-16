---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260331"
---
# <span data-ttu-id="297bb-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="297bb-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="297bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="297bb-102">SYNOPSIS</span></span>
<span data-ttu-id="297bb-103">Exclui uma atribuição de função de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="297bb-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="297bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="297bb-104">SYNTAX</span></span>

### <span data-ttu-id="297bb-105">RemoveByWorkspaceNameAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="297bb-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297bb-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="297bb-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="297bb-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="297bb-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="297bb-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="297bb-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="297bb-115">DESCRIPTION</span></span>
<span data-ttu-id="297bb-116">O cmdlet **Remove-AzSynapseRoleAssignment** exclui permanentemente uma atribuição de função de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="297bb-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="297bb-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="297bb-117">EXAMPLES</span></span>

### <span data-ttu-id="297bb-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="297bb-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="297bb-119">Esse comando exclui uma atribuição de função de análise do Azure Synapse com uma ID de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="297bb-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="297bb-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="297bb-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="297bb-121">Esse comando exclui uma atribuição de função de análise do Azure Synapse com um nome de função e um nome de usuário principal.</span><span class="sxs-lookup"><span data-stu-id="297bb-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="297bb-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="297bb-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="297bb-123">Esse comando exclui uma atribuição de função de análise do Azure Synapse com uma ID de atribuição de função por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="297bb-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="297bb-124">OS</span><span class="sxs-lookup"><span data-stu-id="297bb-124">PARAMETERS</span></span>

### <span data-ttu-id="297bb-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="297bb-125">-AsJob</span></span>
<span data-ttu-id="297bb-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="297bb-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="297bb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297bb-127">-DefaultProfile</span></span>
<span data-ttu-id="297bb-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="297bb-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297bb-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="297bb-129">-ObjectId</span></span>
<span data-ttu-id="297bb-130">O ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="297bb-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="297bb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="297bb-131">-PassThru</span></span>
<span data-ttu-id="297bb-132">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="297bb-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="297bb-133">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="297bb-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="297bb-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="297bb-134">-RoleAssignmentId</span></span>
<span data-ttu-id="297bb-135">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="297bb-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="297bb-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="297bb-136">-RoleDefinitionId</span></span>
<span data-ttu-id="297bb-137">ID da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="297bb-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="297bb-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="297bb-138">-RoleDefinitionName</span></span>
<span data-ttu-id="297bb-139">Nome da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="297bb-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="297bb-140">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="297bb-140">-ServicePrincipalName</span></span>
<span data-ttu-id="297bb-141">O servicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="297bb-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="297bb-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="297bb-142">-SignInName</span></span>
<span data-ttu-id="297bb-143">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="297bb-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="297bb-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="297bb-144">-WorkspaceName</span></span>
<span data-ttu-id="297bb-145">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="297bb-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="297bb-146">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="297bb-146">-WorkspaceObject</span></span>
<span data-ttu-id="297bb-147">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="297bb-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="297bb-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="297bb-148">-Confirm</span></span>
<span data-ttu-id="297bb-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="297bb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297bb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297bb-150">-WhatIf</span></span>
<span data-ttu-id="297bb-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="297bb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297bb-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="297bb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297bb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297bb-153">CommonParameters</span></span>
<span data-ttu-id="297bb-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297bb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297bb-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="297bb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297bb-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="297bb-156">INPUTS</span></span>

### <span data-ttu-id="297bb-157">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="297bb-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="297bb-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="297bb-158">OUTPUTS</span></span>

### <span data-ttu-id="297bb-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="297bb-159">System.Boolean</span></span>

## <span data-ttu-id="297bb-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="297bb-160">NOTES</span></span>

## <span data-ttu-id="297bb-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="297bb-161">RELATED LINKS</span></span>
