---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282120"
---
# <span data-ttu-id="686fe-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="686fe-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="686fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="686fe-102">SYNOPSIS</span></span>
<span data-ttu-id="686fe-103">Obtém uma atribuição de função de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="686fe-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="686fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="686fe-104">SYNTAX</span></span>

### <span data-ttu-id="686fe-105">GetByWorkspaceNameAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="686fe-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="686fe-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="686fe-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="686fe-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="686fe-115">DESCRIPTION</span></span>
<span data-ttu-id="686fe-116">O cmdlet **Get-AzSynapseRoleAssignment** Obtém uma atribuição de função de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="686fe-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="686fe-117">Se você não especificar uma definição de função ou um nome de usuário principal, esse cmdlet obterá toda a atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="686fe-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="686fe-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="686fe-118">EXAMPLES</span></span>

### <span data-ttu-id="686fe-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="686fe-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="686fe-120">Este comando obtém todas as atribuições de função em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="686fe-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="686fe-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="686fe-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="686fe-122">Esse comando obtém todas as atribuições de função em espaço de trabalho ContosoWorkspace com o nome de função ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="686fe-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="686fe-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="686fe-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="686fe-124">Esse comando obtém uma atribuição de função em espaço de trabalho ContosoWorkspace com o nome de função ContosoRole e o nome UPN Contosoname.</span><span class="sxs-lookup"><span data-stu-id="686fe-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="686fe-125">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="686fe-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="686fe-126">Esse comando obtém todas as atribuições de função em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="686fe-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="686fe-127">OS</span><span class="sxs-lookup"><span data-stu-id="686fe-127">PARAMETERS</span></span>

### <span data-ttu-id="686fe-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686fe-128">-DefaultProfile</span></span>
<span data-ttu-id="686fe-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="686fe-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="686fe-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="686fe-130">-ObjectId</span></span>
<span data-ttu-id="686fe-131">O ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="686fe-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="686fe-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="686fe-132">-RoleAssignmentId</span></span>
<span data-ttu-id="686fe-133">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="686fe-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="686fe-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="686fe-134">-RoleDefinitionId</span></span>
<span data-ttu-id="686fe-135">ID da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="686fe-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="686fe-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="686fe-136">-RoleDefinitionName</span></span>
<span data-ttu-id="686fe-137">Nome da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="686fe-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="686fe-138">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="686fe-138">-ServicePrincipalName</span></span>
<span data-ttu-id="686fe-139">O servicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="686fe-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="686fe-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="686fe-140">-SignInName</span></span>
<span data-ttu-id="686fe-141">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="686fe-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="686fe-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="686fe-142">-WorkspaceName</span></span>
<span data-ttu-id="686fe-143">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="686fe-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="686fe-144">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="686fe-144">-WorkspaceObject</span></span>
<span data-ttu-id="686fe-145">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="686fe-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="686fe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686fe-146">CommonParameters</span></span>
<span data-ttu-id="686fe-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686fe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686fe-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="686fe-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686fe-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="686fe-149">INPUTS</span></span>

### <span data-ttu-id="686fe-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="686fe-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="686fe-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="686fe-151">OUTPUTS</span></span>

### <span data-ttu-id="686fe-152">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="686fe-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="686fe-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="686fe-153">NOTES</span></span>

## <span data-ttu-id="686fe-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="686fe-154">RELATED LINKS</span></span>
