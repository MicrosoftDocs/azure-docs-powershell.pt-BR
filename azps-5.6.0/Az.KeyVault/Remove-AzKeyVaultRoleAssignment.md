---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: f93adbf99667c2854557e71af8091012ea82bb74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901475"
---
# <span data-ttu-id="11d98-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="11d98-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="11d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d98-102">SYNOPSIS</span></span>
<span data-ttu-id="11d98-103">Remove uma atribuição de função para a entidade de entidade especificada que é atribuída a uma função específica em um escopo específico.</span><span class="sxs-lookup"><span data-stu-id="11d98-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="11d98-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11d98-104">SYNTAX</span></span>

### <span data-ttu-id="11d98-105">DefinitionNameSignInName (Default)</span><span class="sxs-lookup"><span data-stu-id="11d98-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="11d98-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="11d98-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="11d98-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="11d98-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="11d98-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d98-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d98-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d98-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="11d98-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d98-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11d98-113">DESCRIPTION</span></span>
<span data-ttu-id="11d98-114">Use o `Remove-AzKeyVaultRoleAssignment` cmdlet para revogar o acesso a qualquer entidade em determinado escopo e função.</span><span class="sxs-lookup"><span data-stu-id="11d98-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="11d98-115">O objeto da atribuição, ou seja, a entidade deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="11d98-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="11d98-116">A entidade pode ser um usuário (use parâmetros SignInName ou ObjectId para identificar um usuário), grupo de segurança (use o parâmetro ObjectId para identificar um grupo) ou entidade de serviço (use parâmetros ApplicationId ou ObjectId para identificar um ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="11d98-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="11d98-117">A função à que a entidade é atribuída DEVE ser especificada usando o parâmetro RoleDefinitionName ou RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="11d98-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="11d98-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11d98-118">EXAMPLES</span></span>

### <span data-ttu-id="11d98-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11d98-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="11d98-120">Este exemplo revoga a função "Administrador de Política HSM Gerenciada" de " " no escopo user1@microsoft.com "/keys".</span><span class="sxs-lookup"><span data-stu-id="11d98-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="11d98-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="11d98-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="11d98-122">Este exemplo revoga todas as funções de " user1@microsoft.com " em todos os escopos.</span><span class="sxs-lookup"><span data-stu-id="11d98-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="11d98-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11d98-123">PARAMETERS</span></span>

### <span data-ttu-id="11d98-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11d98-124">-ApplicationId</span></span>
<span data-ttu-id="11d98-125">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11d98-125">The app SPN.</span></span>

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

### <span data-ttu-id="11d98-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d98-126">-DefaultProfile</span></span>
<span data-ttu-id="11d98-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11d98-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d98-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="11d98-128">-HsmName</span></span>
<span data-ttu-id="11d98-129">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="11d98-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="11d98-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d98-130">-InputObject</span></span>
<span data-ttu-id="11d98-131">Objeto de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="11d98-131">Role assignment object.</span></span>

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

### <span data-ttu-id="11d98-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="11d98-132">-ObjectId</span></span>
<span data-ttu-id="11d98-133">A ID do objeto user ou group.</span><span class="sxs-lookup"><span data-stu-id="11d98-133">The user or group object id.</span></span>

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

### <span data-ttu-id="11d98-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11d98-134">-PassThru</span></span>
<span data-ttu-id="11d98-135">Retorne true quando o HSM for restaurado.</span><span class="sxs-lookup"><span data-stu-id="11d98-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="11d98-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="11d98-136">-RoleAssignmentName</span></span>
<span data-ttu-id="11d98-137">Nome da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="11d98-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="11d98-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="11d98-138">-RoleDefinitionId</span></span>
<span data-ttu-id="11d98-139">ID da função à que a entidade é atribuída.</span><span class="sxs-lookup"><span data-stu-id="11d98-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="11d98-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="11d98-140">-RoleDefinitionName</span></span>
<span data-ttu-id="11d98-141">Nome da função RBAC com a que atribuir a entidade.</span><span class="sxs-lookup"><span data-stu-id="11d98-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="11d98-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="11d98-142">-Scope</span></span>
<span data-ttu-id="11d98-143">Escopo no qual a atribuição ou definição de função se aplica, por exemplo, '/' ou '/keys' ou '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="11d98-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="11d98-144">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="11d98-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="11d98-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="11d98-145">-SignInName</span></span>
<span data-ttu-id="11d98-146">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="11d98-146">The user SignInName.</span></span>

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

### <span data-ttu-id="11d98-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11d98-147">-Confirm</span></span>
<span data-ttu-id="11d98-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d98-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d98-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d98-149">-WhatIf</span></span>
<span data-ttu-id="11d98-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11d98-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d98-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11d98-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d98-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d98-152">CommonParameters</span></span>
<span data-ttu-id="11d98-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d98-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d98-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d98-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d98-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11d98-155">INPUTS</span></span>

### <span data-ttu-id="11d98-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="11d98-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="11d98-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11d98-157">OUTPUTS</span></span>

### <span data-ttu-id="11d98-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="11d98-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="11d98-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="11d98-159">NOTES</span></span>

## <span data-ttu-id="11d98-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11d98-160">RELATED LINKS</span></span>
