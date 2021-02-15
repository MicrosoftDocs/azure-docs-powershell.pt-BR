---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113754"
---
# <span data-ttu-id="a01b7-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a01b7-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a01b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a01b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a01b7-103">Atribui a função RBAC especificada ao principal especificado, no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="a01b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a01b7-104">SYNTAX</span></span>

### <span data-ttu-id="a01b7-105">DefinitionNameSignInName (Default)</span><span class="sxs-lookup"><span data-stu-id="a01b7-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b7-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="a01b7-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b7-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="a01b7-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b7-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="a01b7-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b7-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="a01b7-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b7-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="a01b7-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01b7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a01b7-111">DESCRIPTION</span></span>
<span data-ttu-id="a01b7-112">Use o `New-AzKeyVaultRoleAssignment` comando para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="a01b7-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="a01b7-113">O Acesso é concedido atribuindo a função RBAC apropriada a eles no escopo certo.</span><span class="sxs-lookup"><span data-stu-id="a01b7-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="a01b7-114">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="a01b7-115">Para especificar um usuário, use os parâmetros SignInName ou Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a01b7-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="a01b7-116">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a01b7-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="a01b7-117">E para especificar um aplicativo Azure AD, use parâmetros ApplicationId ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="a01b7-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="a01b7-118">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName pr RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="a01b7-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="a01b7-119">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="a01b7-120">Ele é padrão para a assinatura selecionada.</span><span class="sxs-lookup"><span data-stu-id="a01b7-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="a01b7-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a01b7-121">EXAMPLES</span></span>

### <span data-ttu-id="a01b7-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a01b7-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="a01b7-123">Este exemplo atribui a função "Administrador de Política HSM Gerenciada" ao user1@microsoft.com usuário" no escopo superior.</span><span class="sxs-lookup"><span data-stu-id="a01b7-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="a01b7-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a01b7-124">PARAMETERS</span></span>

### <span data-ttu-id="a01b7-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a01b7-125">-ApplicationId</span></span>
<span data-ttu-id="a01b7-126">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a01b7-126">The app SPN.</span></span>

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

### <span data-ttu-id="a01b7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01b7-127">-DefaultProfile</span></span>
<span data-ttu-id="a01b7-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a01b7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a01b7-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a01b7-129">-HsmName</span></span>
<span data-ttu-id="a01b7-130">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="a01b7-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="a01b7-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a01b7-131">-ObjectId</span></span>
<span data-ttu-id="a01b7-132">A ID do objeto de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="a01b7-132">The user or group object id.</span></span>

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

### <span data-ttu-id="a01b7-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a01b7-133">-RoleDefinitionId</span></span>
<span data-ttu-id="a01b7-134">A ID da função à que o diretor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a01b7-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="a01b7-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a01b7-135">-RoleDefinitionName</span></span>
<span data-ttu-id="a01b7-136">Nome da função RBAC para atribuir o diretor.</span><span class="sxs-lookup"><span data-stu-id="a01b7-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="a01b7-137">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a01b7-137">-Scope</span></span>
<span data-ttu-id="a01b7-138">Escopo no qual a atribuição ou definição da função se aplica, por exemplo, '/' ou '/keys' ou '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="a01b7-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="a01b7-139">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="a01b7-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="a01b7-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a01b7-140">-SignInName</span></span>
<span data-ttu-id="a01b7-141">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="a01b7-141">The user SignInName.</span></span>

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

### <span data-ttu-id="a01b7-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a01b7-142">-Confirm</span></span>
<span data-ttu-id="a01b7-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a01b7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a01b7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01b7-144">-WhatIf</span></span>
<span data-ttu-id="a01b7-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01b7-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a01b7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a01b7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01b7-147">CommonParameters</span></span>
<span data-ttu-id="a01b7-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01b7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01b7-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a01b7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01b7-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="a01b7-150">INPUTS</span></span>

### <span data-ttu-id="a01b7-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a01b7-151">None</span></span>

## <span data-ttu-id="a01b7-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="a01b7-152">OUTPUTS</span></span>

### <span data-ttu-id="a01b7-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a01b7-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a01b7-154">Notas</span><span class="sxs-lookup"><span data-stu-id="a01b7-154">NOTES</span></span>

## <span data-ttu-id="a01b7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a01b7-155">RELATED LINKS</span></span>
