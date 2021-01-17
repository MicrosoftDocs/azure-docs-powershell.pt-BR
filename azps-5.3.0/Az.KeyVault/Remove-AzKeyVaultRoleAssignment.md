---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429814"
---
# <span data-ttu-id="448f6-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="448f6-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="448f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="448f6-102">SYNOPSIS</span></span>
<span data-ttu-id="448f6-103">Remove uma atribuição de função para a entidade de segurança especificada que é atribuída a uma função específica em um escopo específico.</span><span class="sxs-lookup"><span data-stu-id="448f6-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="448f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="448f6-104">SYNTAX</span></span>

### <span data-ttu-id="448f6-105">DefinitionNameSignInName (padrão)</span><span class="sxs-lookup"><span data-stu-id="448f6-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="448f6-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="448f6-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="448f6-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="448f6-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="448f6-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="448f6-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="448f6-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448f6-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="448f6-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448f6-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="448f6-113">DESCRIPTION</span></span>
<span data-ttu-id="448f6-114">Use o `Remove-AzKeyVaultRoleAssignment` cmdlet para revogar o acesso a qualquer entidade no escopo fornecido e à função dada.</span><span class="sxs-lookup"><span data-stu-id="448f6-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="448f6-115">O objeto da tarefa, ou seja, a principal deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="448f6-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="448f6-116">O principal pode ser um usuário (use parâmetros SignInName ou ObjectId para identificar um usuário), grupo de segurança (use o parâmetro ObjectId para identificar um grupo) ou entidade de serviço (use parâmetros ApplicationId ou ObjectId para identificar um servicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="448f6-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="448f6-117">A função à qual a entidade de segurança é atribuída deve ser especificada usando o parâmetro RoleDefinitionName ou RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="448f6-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="448f6-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="448f6-118">EXAMPLES</span></span>

### <span data-ttu-id="448f6-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="448f6-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="448f6-120">Este exemplo revoga a função "administrador da política HSM gerenciado" do user1@microsoft.com escopo "" em "/Keys".</span><span class="sxs-lookup"><span data-stu-id="448f6-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="448f6-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="448f6-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="448f6-122">Este exemplo revoga todas as funções de " user1@microsoft.com " em todos os escopos.</span><span class="sxs-lookup"><span data-stu-id="448f6-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="448f6-123">OS</span><span class="sxs-lookup"><span data-stu-id="448f6-123">PARAMETERS</span></span>

### <span data-ttu-id="448f6-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="448f6-124">-ApplicationId</span></span>
<span data-ttu-id="448f6-125">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="448f6-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448f6-126">-DefaultProfile</span></span>
<span data-ttu-id="448f6-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="448f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="448f6-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="448f6-128">-HsmName</span></span>
<span data-ttu-id="448f6-129">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="448f6-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="448f6-130">-InputObject</span></span>
<span data-ttu-id="448f6-131">Objeto de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="448f6-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="448f6-132">-ObjectId</span></span>
<span data-ttu-id="448f6-133">A ID do objeto de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="448f6-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="448f6-134">-PassThru</span></span>
<span data-ttu-id="448f6-135">Retorne verdadeiro quando o HSM for restaurado.</span><span class="sxs-lookup"><span data-stu-id="448f6-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="448f6-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="448f6-136">-RoleAssignmentName</span></span>
<span data-ttu-id="448f6-137">Nome da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="448f6-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="448f6-138">-RoleDefinitionId</span></span>
<span data-ttu-id="448f6-139">ID da função à qual o principal está atribuído.</span><span class="sxs-lookup"><span data-stu-id="448f6-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="448f6-140">-RoleDefinitionName</span></span>
<span data-ttu-id="448f6-141">Nome da função RBAC com a qual atribuir o objeto.</span><span class="sxs-lookup"><span data-stu-id="448f6-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-142">-Escopo</span><span class="sxs-lookup"><span data-stu-id="448f6-142">-Scope</span></span>
<span data-ttu-id="448f6-143">Escopo no qual a atribuição de função ou definição se aplica, por exemplo, '/' ou '/Keys ' ou '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="448f6-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="448f6-144">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="448f6-144">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="448f6-145">-SignInName</span></span>
<span data-ttu-id="448f6-146">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="448f6-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448f6-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="448f6-147">-Confirm</span></span>
<span data-ttu-id="448f6-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="448f6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448f6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448f6-149">-WhatIf</span></span>
<span data-ttu-id="448f6-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="448f6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448f6-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="448f6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448f6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448f6-152">CommonParameters</span></span>
<span data-ttu-id="448f6-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448f6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448f6-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="448f6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448f6-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="448f6-155">INPUTS</span></span>

### <span data-ttu-id="448f6-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="448f6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="448f6-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="448f6-157">OUTPUTS</span></span>

### <span data-ttu-id="448f6-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="448f6-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="448f6-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="448f6-159">NOTES</span></span>

## <span data-ttu-id="448f6-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="448f6-160">RELATED LINKS</span></span>
