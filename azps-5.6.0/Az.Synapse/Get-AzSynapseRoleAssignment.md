---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: 2171f99da156d86161773b039edeb884dee7a7e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887838"
---
# <span data-ttu-id="fe3d6-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fe3d6-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="fe3d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3d6-103">Obtém uma atribuição de função do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fe3d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe3d6-104">SYNTAX</span></span>

### <span data-ttu-id="fe3d6-105">GetByWorkspaceNameAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe3d6-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d6-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3d6-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3d6-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe3d6-115">DESCRIPTION</span></span>
<span data-ttu-id="fe3d6-116">O cmdlet **Get-AzSynapseRoleAssignment** obtém uma atribuição de função de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="fe3d6-117">Se você não especificar uma definição de função ou um nome de entidade de usuário, esse cmdlet obtém todas as atribuições de função.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="fe3d6-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-118">EXAMPLES</span></span>

### <span data-ttu-id="fe3d6-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe3d6-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fe3d6-120">Este comando obtém todas as atribuições de função em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="fe3d6-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fe3d6-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="fe3d6-122">Este comando obtém todas as atribuições de função no espaço de trabalho ContosoWorkspace com o nome da função ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="fe3d6-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fe3d6-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fe3d6-124">Este comando obtém uma atribuição de função no espaço de trabalho ContosoWorkspace com nome de função ContosoRole e nome principal do usuário ContosoName.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="fe3d6-125">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fe3d6-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="fe3d6-126">Esse comando obtém todas as atribuições de função em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="fe3d6-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-127">PARAMETERS</span></span>

### <span data-ttu-id="fe3d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3d6-128">-DefaultProfile</span></span>
<span data-ttu-id="fe3d6-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3d6-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fe3d6-130">-ObjectId</span></span>
<span data-ttu-id="fe3d6-131">ObjectId do Azure AD da Entidade de Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="fe3d6-132">-RoleAssignmentId</span></span>
<span data-ttu-id="fe3d6-133">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fe3d6-134">-RoleDefinitionId</span></span>
<span data-ttu-id="fe3d6-135">ID da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fe3d6-136">-RoleDefinitionName</span></span>
<span data-ttu-id="fe3d6-137">Nome da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fe3d6-138">-ServicePrincipalName</span></span>
<span data-ttu-id="fe3d6-139">ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fe3d6-140">-SignInName</span></span>
<span data-ttu-id="fe3d6-141">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe3d6-142">-WorkspaceName</span></span>
<span data-ttu-id="fe3d6-143">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fe3d6-144">-WorkspaceObject</span></span>
<span data-ttu-id="fe3d6-145">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3d6-146">CommonParameters</span></span>
<span data-ttu-id="fe3d6-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3d6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3d6-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe3d6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3d6-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-149">INPUTS</span></span>

### <span data-ttu-id="fe3d6-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe3d6-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fe3d6-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-151">OUTPUTS</span></span>

### <span data-ttu-id="fe3d6-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="fe3d6-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="fe3d6-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe3d6-153">NOTES</span></span>

## <span data-ttu-id="fe3d6-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe3d6-154">RELATED LINKS</span></span>
