---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115303"
---
# <span data-ttu-id="7ccc6-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7ccc6-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="7ccc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ccc6-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccc6-103">Atribui a função RBAC especificada à entidade de segurança especificada, no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="7ccc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ccc6-104">SYNTAX</span></span>

### <span data-ttu-id="7ccc6-105">DefinitionNameSignInName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ccc6-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccc6-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccc6-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccc6-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccc6-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ccc6-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="7ccc6-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ccc6-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ccc6-111">DESCRIPTION</span></span>
<span data-ttu-id="7ccc6-112">Use o `New-AzManagedHsmRoleAssignment` comando para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="7ccc6-113">O Access é concedido atribuindo a função RBAC apropriada a ele no escopo certo.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="7ccc6-114">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7ccc6-115">Para especificar um usuário, use SignInName ou os parâmetros do ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7ccc6-116">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7ccc6-117">E para especificar um aplicativo do Azure AD, use parâmetros ApplicationId ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="7ccc6-118">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName de RP RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="7ccc6-119">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="7ccc6-120">O padrão é a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="7ccc6-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ccc6-121">EXAMPLES</span></span>

### <span data-ttu-id="7ccc6-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ccc6-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="7ccc6-123">Este exemplo atribui a função "administrador de política HSM gerenciado" ao usuário " user1@microsoft.com " no escopo superior.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="7ccc6-124">OS</span><span class="sxs-lookup"><span data-stu-id="7ccc6-124">PARAMETERS</span></span>

### <span data-ttu-id="7ccc6-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-125">-ApplicationId</span></span>
<span data-ttu-id="7ccc6-126">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-126">The app SPN.</span></span>

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

### <span data-ttu-id="7ccc6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccc6-127">-DefaultProfile</span></span>
<span data-ttu-id="7ccc6-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccc6-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7ccc6-129">-HsmName</span></span>
<span data-ttu-id="7ccc6-130">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ccc6-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-131">-ObjectId</span></span>
<span data-ttu-id="7ccc6-132">A ID do objeto de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-132">The user or group object id.</span></span>

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

### <span data-ttu-id="7ccc6-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7ccc6-133">-RoleDefinitionId</span></span>
<span data-ttu-id="7ccc6-134">ID da função à qual o principal está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="7ccc6-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7ccc6-135">-RoleDefinitionName</span></span>
<span data-ttu-id="7ccc6-136">Nome da função RBAC com a qual atribuir o objeto.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="7ccc6-137">-Escopo</span><span class="sxs-lookup"><span data-stu-id="7ccc6-137">-Scope</span></span>
<span data-ttu-id="7ccc6-138">Escopo no qual a atribuição de função ou definição se aplica, por exemplo, '/' ou '/Keys ' ou '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="7ccc6-139">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="7ccc6-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7ccc6-140">-SignInName</span></span>
<span data-ttu-id="7ccc6-141">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-141">The user SignInName.</span></span>

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

### <span data-ttu-id="7ccc6-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ccc6-142">-Confirm</span></span>
<span data-ttu-id="7ccc6-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ccc6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ccc6-144">-WhatIf</span></span>
<span data-ttu-id="7ccc6-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ccc6-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ccc6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccc6-147">CommonParameters</span></span>
<span data-ttu-id="7ccc6-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ccc6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccc6-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ccc6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccc6-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ccc6-150">INPUTS</span></span>

### <span data-ttu-id="7ccc6-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7ccc6-151">None</span></span>

## <span data-ttu-id="7ccc6-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ccc6-152">OUTPUTS</span></span>

### <span data-ttu-id="7ccc6-153">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7ccc6-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="7ccc6-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ccc6-154">NOTES</span></span>

## <span data-ttu-id="7ccc6-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ccc6-155">RELATED LINKS</span></span>
