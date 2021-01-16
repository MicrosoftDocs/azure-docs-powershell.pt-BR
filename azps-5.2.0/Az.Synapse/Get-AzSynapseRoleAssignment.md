---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259240"
---
# <span data-ttu-id="75a3d-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="75a3d-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="75a3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="75a3d-103">Obtém uma atribuição de função de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="75a3d-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="75a3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75a3d-104">SYNTAX</span></span>

### <span data-ttu-id="75a3d-105">GetByWorkspaceNameAndNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75a3d-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a3d-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a3d-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a3d-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75a3d-115">DESCRIPTION</span></span>
<span data-ttu-id="75a3d-116">O cmdlet **Get-AzSynapseRoleAssignment** Obtém uma atribuição de função de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="75a3d-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="75a3d-117">Se você não especificar uma definição de função ou um nome de usuário principal, esse cmdlet obterá toda a atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="75a3d-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="75a3d-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75a3d-118">EXAMPLES</span></span>

### <span data-ttu-id="75a3d-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75a3d-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="75a3d-120">Este comando obtém todas as atribuições de função em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="75a3d-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="75a3d-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75a3d-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="75a3d-122">Esse comando obtém todas as atribuições de função em espaço de trabalho ContosoWorkspace com o nome de função ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="75a3d-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="75a3d-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="75a3d-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="75a3d-124">Esse comando obtém uma atribuição de função em espaço de trabalho ContosoWorkspace com o nome de função ContosoRole e o nome UPN Contosoname.</span><span class="sxs-lookup"><span data-stu-id="75a3d-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="75a3d-125">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="75a3d-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="75a3d-126">Esse comando obtém todas as atribuições de função em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="75a3d-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="75a3d-127">OS</span><span class="sxs-lookup"><span data-stu-id="75a3d-127">PARAMETERS</span></span>

### <span data-ttu-id="75a3d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a3d-128">-DefaultProfile</span></span>
<span data-ttu-id="75a3d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75a3d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a3d-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="75a3d-130">-ObjectId</span></span>
<span data-ttu-id="75a3d-131">O ObjectId do Azure AD do usuário, grupo ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="75a3d-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="75a3d-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="75a3d-132">-RoleAssignmentId</span></span>
<span data-ttu-id="75a3d-133">A ID da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="75a3d-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="75a3d-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="75a3d-134">-RoleDefinitionId</span></span>
<span data-ttu-id="75a3d-135">ID da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="75a3d-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="75a3d-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="75a3d-136">-RoleDefinitionName</span></span>
<span data-ttu-id="75a3d-137">Nome da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="75a3d-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="75a3d-138">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="75a3d-138">-ServicePrincipalName</span></span>
<span data-ttu-id="75a3d-139">O servicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="75a3d-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="75a3d-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="75a3d-140">-SignInName</span></span>
<span data-ttu-id="75a3d-141">O endereço de email ou o nome UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="75a3d-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="75a3d-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75a3d-142">-WorkspaceName</span></span>
<span data-ttu-id="75a3d-143">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="75a3d-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="75a3d-144">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="75a3d-144">-WorkspaceObject</span></span>
<span data-ttu-id="75a3d-145">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="75a3d-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="75a3d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a3d-146">CommonParameters</span></span>
<span data-ttu-id="75a3d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a3d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a3d-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75a3d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a3d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75a3d-149">INPUTS</span></span>

### <span data-ttu-id="75a3d-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75a3d-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="75a3d-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75a3d-151">OUTPUTS</span></span>

### <span data-ttu-id="75a3d-152">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="75a3d-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="75a3d-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75a3d-153">NOTES</span></span>

## <span data-ttu-id="75a3d-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75a3d-154">RELATED LINKS</span></span>
