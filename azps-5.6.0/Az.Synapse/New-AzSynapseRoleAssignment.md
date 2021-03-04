---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 7e216a6d2751ddd24e7d948cb6cca036c2a9b336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888395"
---
# <span data-ttu-id="af11e-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="af11e-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="af11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af11e-102">SYNOPSIS</span></span>
<span data-ttu-id="af11e-103">Cria uma atribuição de função do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="af11e-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="af11e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="af11e-104">SYNTAX</span></span>

### <span data-ttu-id="af11e-105">NewByWorkspaceNameAndNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="af11e-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af11e-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af11e-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af11e-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af11e-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af11e-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af11e-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af11e-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af11e-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af11e-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="af11e-113">DESCRIPTION</span></span>
<span data-ttu-id="af11e-114">O cmdlet **New-AzSynapseRoleAssignment** cria uma atribuição de função do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="af11e-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="af11e-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af11e-115">EXAMPLES</span></span>

### <span data-ttu-id="af11e-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af11e-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="af11e-117">Este comando atribui ContosoRole ao usuário cujo nome principal é ContosoName.</span><span class="sxs-lookup"><span data-stu-id="af11e-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="af11e-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af11e-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="af11e-119">Este comando atribui ContosoRole ao usuário cujo nome principal é ContosoName por pipeline.</span><span class="sxs-lookup"><span data-stu-id="af11e-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="af11e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="af11e-120">PARAMETERS</span></span>

### <span data-ttu-id="af11e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af11e-121">-AsJob</span></span>
<span data-ttu-id="af11e-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="af11e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af11e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af11e-123">-DefaultProfile</span></span>
<span data-ttu-id="af11e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af11e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af11e-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="af11e-125">-ObjectId</span></span>
<span data-ttu-id="af11e-126">ObjectId do Azure AD da Entidade de Usuário, Grupo ou Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="af11e-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="af11e-127">-RoleDefinitionId</span></span>
<span data-ttu-id="af11e-128">ID da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="af11e-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="af11e-129">-RoleDefinitionName</span></span>
<span data-ttu-id="af11e-130">Nome da função atribuída à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="af11e-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="af11e-131">-ServicePrincipalName</span></span>
<span data-ttu-id="af11e-132">ServicePrincipalName da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="af11e-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="af11e-133">-SignInName</span></span>
<span data-ttu-id="af11e-134">O endereço de email ou o nome principal do usuário.</span><span class="sxs-lookup"><span data-stu-id="af11e-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af11e-135">-WorkspaceName</span></span>
<span data-ttu-id="af11e-136">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="af11e-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="af11e-137">-WorkspaceObject</span></span>
<span data-ttu-id="af11e-138">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="af11e-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af11e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af11e-139">-Confirm</span></span>
<span data-ttu-id="af11e-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af11e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af11e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af11e-141">-WhatIf</span></span>
<span data-ttu-id="af11e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af11e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af11e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af11e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af11e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af11e-144">CommonParameters</span></span>
<span data-ttu-id="af11e-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af11e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af11e-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af11e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af11e-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af11e-147">INPUTS</span></span>

### <span data-ttu-id="af11e-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="af11e-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="af11e-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="af11e-149">OUTPUTS</span></span>

### <span data-ttu-id="af11e-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="af11e-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="af11e-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="af11e-151">NOTES</span></span>

## <span data-ttu-id="af11e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af11e-152">RELATED LINKS</span></span>
