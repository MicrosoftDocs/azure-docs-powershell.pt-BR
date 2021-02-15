---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112399"
---
# <span data-ttu-id="10b2d-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="10b2d-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="10b2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="10b2d-103">Exclui uma atribuição de função Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="10b2d-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="10b2d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10b2d-104">SYNTAX</span></span>

### <span data-ttu-id="10b2d-105">RemoveByWorkspaceNameAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10b2d-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b2d-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10b2d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10b2d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10b2d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b2d-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b2d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b2d-115">DESCRIPTION</span></span>
<span data-ttu-id="10b2d-116">O cmdlet **Remove-AzSynapseRoleAssignment** exclui permanentemente uma atribuição de função Do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="10b2d-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="10b2d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10b2d-117">EXAMPLES</span></span>

### <span data-ttu-id="10b2d-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10b2d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="10b2d-119">Esse comando exclui uma atribuição de função Análise Synapse do Azure com uma ID de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="10b2d-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="10b2d-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10b2d-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="10b2d-121">Esse comando exclui uma atribuição de função do Azure Synapse Analytics com um nome de função e um nome de entidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="10b2d-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="10b2d-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="10b2d-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="10b2d-123">Esse comando exclui uma atribuição de função do Azure Synapse Analytics com uma ID de atribuição de função por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="10b2d-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="10b2d-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10b2d-124">PARAMETERS</span></span>

### <span data-ttu-id="10b2d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10b2d-125">-AsJob</span></span>
<span data-ttu-id="10b2d-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="10b2d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10b2d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b2d-127">-DefaultProfile</span></span>
<span data-ttu-id="10b2d-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10b2d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10b2d-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="10b2d-129">-ObjectId</span></span>
<span data-ttu-id="10b2d-130">O ObjectId do Azure AD do Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="10b2d-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="10b2d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10b2d-131">-PassThru</span></span>
<span data-ttu-id="10b2d-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="10b2d-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="10b2d-133">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="10b2d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="10b2d-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="10b2d-134">-RoleAssignmentId</span></span>
<span data-ttu-id="10b2d-135">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="10b2d-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="10b2d-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="10b2d-136">-RoleDefinitionId</span></span>
<span data-ttu-id="10b2d-137">ID da Função atribuída ao diretor.</span><span class="sxs-lookup"><span data-stu-id="10b2d-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="10b2d-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="10b2d-138">-RoleDefinitionName</span></span>
<span data-ttu-id="10b2d-139">Nome da Função atribuída ao diretor.</span><span class="sxs-lookup"><span data-stu-id="10b2d-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="10b2d-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="10b2d-140">-ServicePrincipalName</span></span>
<span data-ttu-id="10b2d-141">O ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="10b2d-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="10b2d-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="10b2d-142">-SignInName</span></span>
<span data-ttu-id="10b2d-143">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="10b2d-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="10b2d-144">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="10b2d-144">-WorkspaceName</span></span>
<span data-ttu-id="10b2d-145">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="10b2d-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="10b2d-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="10b2d-146">-WorkspaceObject</span></span>
<span data-ttu-id="10b2d-147">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="10b2d-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="10b2d-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10b2d-148">-Confirm</span></span>
<span data-ttu-id="10b2d-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b2d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b2d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b2d-150">-WhatIf</span></span>
<span data-ttu-id="10b2d-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10b2d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b2d-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10b2d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b2d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b2d-153">CommonParameters</span></span>
<span data-ttu-id="10b2d-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b2d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b2d-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10b2d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b2d-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="10b2d-156">INPUTS</span></span>

### <span data-ttu-id="10b2d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10b2d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="10b2d-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="10b2d-158">OUTPUTS</span></span>

### <span data-ttu-id="10b2d-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10b2d-159">System.Boolean</span></span>

## <span data-ttu-id="10b2d-160">Notas</span><span class="sxs-lookup"><span data-stu-id="10b2d-160">NOTES</span></span>

## <span data-ttu-id="10b2d-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10b2d-161">RELATED LINKS</span></span>
