---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113759"
---
# <span data-ttu-id="27f9e-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="27f9e-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="27f9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="27f9e-103">Obter ou listar atribuições de função de um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="27f9e-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="27f9e-104">Use parâmetros respectivos para listar atribuições para um usuário específico ou uma definição de função.</span><span class="sxs-lookup"><span data-stu-id="27f9e-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="27f9e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27f9e-105">SYNTAX</span></span>

### <span data-ttu-id="27f9e-106">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="27f9e-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27f9e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="27f9e-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f9e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="27f9e-108">DESCRIPTION</span></span>
<span data-ttu-id="27f9e-109">Use o `Get-AzKeyVaultRoleAssignment` comando para listar todas as atribuições de função que são eficazes em um escopo.</span><span class="sxs-lookup"><span data-stu-id="27f9e-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="27f9e-110">Sem parâmetros, esse comando retorna todas as atribuições de função feitas sob o HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="27f9e-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="27f9e-111">Essa lista pode ser filtrada usando parâmetros de filtragem para principal, função e escopo.</span><span class="sxs-lookup"><span data-stu-id="27f9e-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="27f9e-112">O assunto da tarefa deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="27f9e-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="27f9e-113">Para especificar um usuário, use os parâmetros SignInName ou Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="27f9e-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="27f9e-114">Para especificar um grupo de segurança, use o parâmetro ObjectId do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="27f9e-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="27f9e-115">E para especificar um aplicativo Azure AD, use parâmetros ApplicationId ou ObjectId.</span><span class="sxs-lookup"><span data-stu-id="27f9e-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="27f9e-116">A função que está sendo atribuída deve ser especificada usando o parâmetro RoleDefinitionName ou RoleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="27f9e-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="27f9e-117">O escopo no qual o acesso está sendo concedido pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="27f9e-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="27f9e-118">Ele é padrão para "/".</span><span class="sxs-lookup"><span data-stu-id="27f9e-118">It defaults to "/".</span></span>

## <span data-ttu-id="27f9e-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27f9e-119">EXAMPLES</span></span>

### <span data-ttu-id="27f9e-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27f9e-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="27f9e-121">Este exemplo lista todas as atribuições de função de "myHsm" em todo o escopo.</span><span class="sxs-lookup"><span data-stu-id="27f9e-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="27f9e-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="27f9e-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="27f9e-123">Este exemplo lista todas as atribuições de função de "myHsm" no escopo "/keys" e filtra o resultado por nome de login do usuário.</span><span class="sxs-lookup"><span data-stu-id="27f9e-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="27f9e-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27f9e-124">PARAMETERS</span></span>

### <span data-ttu-id="27f9e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="27f9e-125">-ApplicationId</span></span>
<span data-ttu-id="27f9e-126">O SPN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27f9e-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f9e-127">-DefaultProfile</span></span>
<span data-ttu-id="27f9e-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27f9e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27f9e-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="27f9e-129">-HsmName</span></span>
<span data-ttu-id="27f9e-130">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="27f9e-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="27f9e-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="27f9e-131">-ObjectId</span></span>
<span data-ttu-id="27f9e-132">A ID do objeto de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="27f9e-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="27f9e-133">-RoleAssignmentName</span></span>
<span data-ttu-id="27f9e-134">Nome da atribuição de função.</span><span class="sxs-lookup"><span data-stu-id="27f9e-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="27f9e-135">-RoleDefinitionId</span></span>
<span data-ttu-id="27f9e-136">A ID da função à que o diretor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="27f9e-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="27f9e-137">-RoleDefinitionName</span></span>
<span data-ttu-id="27f9e-138">Nome da função RBAC para atribuir o diretor.</span><span class="sxs-lookup"><span data-stu-id="27f9e-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-139">-Escopo</span><span class="sxs-lookup"><span data-stu-id="27f9e-139">-Scope</span></span>
<span data-ttu-id="27f9e-140">Escopo no qual a atribuição ou definição da função se aplica, por exemplo, '/' ou '/keys' ou '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="27f9e-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="27f9e-141">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="27f9e-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="27f9e-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="27f9e-142">-SignInName</span></span>
<span data-ttu-id="27f9e-143">O usuário SignInName.</span><span class="sxs-lookup"><span data-stu-id="27f9e-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f9e-144">CommonParameters</span></span>
<span data-ttu-id="27f9e-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27f9e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f9e-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27f9e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f9e-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="27f9e-147">INPUTS</span></span>

### <span data-ttu-id="27f9e-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="27f9e-148">None</span></span>

## <span data-ttu-id="27f9e-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="27f9e-149">OUTPUTS</span></span>

### <span data-ttu-id="27f9e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="27f9e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="27f9e-151">Notas</span><span class="sxs-lookup"><span data-stu-id="27f9e-151">NOTES</span></span>

## <span data-ttu-id="27f9e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27f9e-152">RELATED LINKS</span></span>
