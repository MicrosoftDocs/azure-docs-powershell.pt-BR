---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115288"
---
# <span data-ttu-id="3c2e2-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c2e2-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="3c2e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2e2-103">Remove uma atribuição de função para a entidade de segurança especificada que é atribuída a uma função específica em um escopo específico.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="3c2e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c2e2-104">SYNTAX</span></span>

### <span data-ttu-id="3c2e2-105">DefinitionNameSignInName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c2e2-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c2e2-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2e2-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c2e2-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c2e2-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c2e2-113">DESCRIPTION</span></span>
<span data-ttu-id="3c2e2-114">Use o `Remove-AzManagedHsmRoleAssignment` cmdlet para revogar o acesso a qualquer entidade no escopo fornecido e à função dada.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="3c2e2-115">O objeto da tarefa, ou seja, a principal deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="3c2e2-116">O principal pode ser um usuário (use parâmetros SignInName ou ObjectId para identificar um usuário), grupo de segurança (use o parâmetro ObjectId para identificar um grupo) ou entidade de serviço (use parâmetros ApplicationId ou ObjectId para identificar um servicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="3c2e2-117">A função à qual a entidade de segurança é atribuída deve ser especificada usando o parâmetro RoleDefinitionName ou RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="3c2e2-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-118">EXAMPLES</span></span>

### <span data-ttu-id="3c2e2-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c2e2-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="3c2e2-120">Este exemplo revoga a função "administrador da política HSM gerenciado" do user1@microsoft.com escopo "" em "/Keys".</span><span class="sxs-lookup"><span data-stu-id="3c2e2-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="3c2e2-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c2e2-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="3c2e2-122">Este exemplo revoga todas as funções de " user1@microsoft.com " em todos os escopos.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="3c2e2-123">OS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-123">PARAMETERS</span></span>

### <span data-ttu-id="3c2e2-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-124">-ApplicationId</span></span>
<span data-ttu-id="3c2e2-125">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-125">The app SPN.</span></span>

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

### <span data-ttu-id="3c2e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2e2-126">-DefaultProfile</span></span>
<span data-ttu-id="3c2e2-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2e2-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-128">-HsmName</span></span>
<span data-ttu-id="3c2e2-129">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="3c2e2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c2e2-130">-InputObject</span></span>
<span data-ttu-id="3c2e2-131">Objeto de atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-131">Role assignment object.</span></span>

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

### <span data-ttu-id="3c2e2-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-132">-ObjectId</span></span>
<span data-ttu-id="3c2e2-133">A ID do objeto de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-133">The user or group object id.</span></span>

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

### <span data-ttu-id="3c2e2-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c2e2-134">-PassThru</span></span>
<span data-ttu-id="3c2e2-135">Retorne verdadeiro quando o HSM for restaurado.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="3c2e2-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-136">-RoleAssignmentName</span></span>
<span data-ttu-id="3c2e2-137">Nome da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="3c2e2-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3c2e2-138">-RoleDefinitionId</span></span>
<span data-ttu-id="3c2e2-139">ID da função à qual o principal está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="3c2e2-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-140">-RoleDefinitionName</span></span>
<span data-ttu-id="3c2e2-141">Nome da função RBAC com a qual atribuir o objeto.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="3c2e2-142">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3c2e2-142">-Scope</span></span>
<span data-ttu-id="3c2e2-143">Escopo no qual a atribuição de função ou definição se aplica, por exemplo, '/' ou '/Keys ' ou '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="3c2e2-144">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="3c2e2-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3c2e2-145">-SignInName</span></span>
<span data-ttu-id="3c2e2-146">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-146">The user SignInName.</span></span>

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

### <span data-ttu-id="3c2e2-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c2e2-147">-Confirm</span></span>
<span data-ttu-id="3c2e2-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c2e2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c2e2-149">-WhatIf</span></span>
<span data-ttu-id="3c2e2-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c2e2-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c2e2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2e2-152">CommonParameters</span></span>
<span data-ttu-id="3c2e2-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2e2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2e2-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c2e2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2e2-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c2e2-155">INPUTS</span></span>

### <span data-ttu-id="3c2e2-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c2e2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="3c2e2-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c2e2-157">OUTPUTS</span></span>

### <span data-ttu-id="3c2e2-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3c2e2-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="3c2e2-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c2e2-159">NOTES</span></span>

## <span data-ttu-id="3c2e2-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c2e2-160">RELATED LINKS</span></span>
