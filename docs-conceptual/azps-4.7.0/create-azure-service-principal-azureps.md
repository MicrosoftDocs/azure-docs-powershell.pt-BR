---
title: Usar as entidades de serviço do Azure com o Azure PowerShell
description: Saiba como criar e usar entidades de serviço com o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3c876454560e4ad421e6d32a8ca8b30a651fd8af
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90927902"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="d5cfa-103">Criar uma entidade de serviço do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5cfa-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="d5cfa-104">Ferramentas automatizadas que usam os serviços do Azure devem sempre ter permissões restritas.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="d5cfa-105">Em vez de os aplicativos entrarem como um usuário com privilégio total, o Azure oferece as entidades de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="d5cfa-106">Uma entidade de serviço do Azure é uma identidade criada para uso com aplicativos, serviços hospedados e ferramentas automatizadas para acessar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="d5cfa-107">Esse acesso é restrito pelas funções atribuídas à entidade de serviço, oferecendo a você o controle sobre quais recursos poderão ser acessados e em qual nível.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="d5cfa-108">Por motivos de segurança, é sempre recomendado usar entidades de serviço com ferramentas automatizadas em vez de permitir a entrada com uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="d5cfa-109">Este artigo mostra as etapas para criar, obter informações e redefinir uma entidade de serviço com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="d5cfa-110">Criar uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="d5cfa-110">Create a service principal</span></span>

<span data-ttu-id="d5cfa-111">Criar uma entidade de serviço com o cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="d5cfa-112">Ao criar uma entidade de serviço, você pode escolher o tipo de autenticação de entrada usada.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cfa-113">Se a sua conta não tiver permissão para criar uma entidade de serviço, `New-AzADServicePrincipal` retornará a mensagem de erro "Privilégios insuficientes para concluir a operação".</span><span class="sxs-lookup"><span data-stu-id="d5cfa-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="d5cfa-114">Entre em contato com o administrador do Azure Active Directory para criar uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="d5cfa-115">Há dois tipos de autenticação disponíveis para as entidades de serviço: A autenticação baseada em senha e em certificado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="d5cfa-116">Autenticação baseada em senha</span><span class="sxs-lookup"><span data-stu-id="d5cfa-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-117">A função padrão de uma entidade de serviço de autenticação baseada em senha é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="d5cfa-118">Essa função tem permissões completas para ler e gravar em uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="d5cfa-119">Para obter informações sobre como gerenciar atribuições de função, confira [Gerenciar funções de entidade de serviço](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="d5cfa-120">Sem outros parâmetros de autenticação, usa-se a autenticação baseada em senha, com uma senha aleatória criada para você.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="d5cfa-121">Caso queira uma autenticação baseada em senha, esse método é recomendado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="d5cfa-122">O objeto retornado contém o membro `Secret`, que é um `SecureString` que contém a senha gerada.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="d5cfa-123">Armazene esse valor em algum lugar seguro para autenticar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="d5cfa-124">Seu valor _não_ será exibido na saída do console.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="d5cfa-125">Se você perder a senha, [redefina as credenciais da entidade de serviço](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="d5cfa-126">O código a seguir permitirá que você exporte o segredo:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="d5cfa-127">Para senhas fornecidas pelo usuário, o argumento `-PasswordCredential` usa os objetos `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="d5cfa-128">Esses objetos devem ter uma validade `StartDate` e `EndDate`, além de usar um texto sem formatação `Password`.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="d5cfa-129">Quando criar uma senha, certifique-se de seguir as [Regras e restrições de senha do Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="d5cfa-130">Não use uma senha fraca, nem reutilize uma senha.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="d5cfa-131">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-132">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="d5cfa-133">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte _imediatamente após_ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="d5cfa-134">Autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="d5cfa-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-135">Não há nenhuma função padrão atribuída ao criar uma entidade de serviço de autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="d5cfa-136">Para obter informações sobre como gerenciar atribuições de função, confira [Gerenciar funções de entidade de serviço](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="d5cfa-137">As entidades de serviço que usam a autenticação baseada em certificado são criadas com o parâmetro `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="d5cfa-138">Esse parâmetro usa uma cadeia de caracteres ASCII codificada em base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="d5cfa-139">Isso é representado por um arquivo PEM ou por um CRT ou CER com texto codificado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="d5cfa-140">Não há suporte para codificações binárias do certificado público.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="d5cfa-141">Essas instruções pressupõem que você já tenha um certificado disponível.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="d5cfa-142">Você também pode usar o parâmetro `-KeyCredential`, que usa objetos `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="d5cfa-143">Esses objetos devem ter um `StartDate` e `EndDate` válidos, além do membro `CertValue` definido como uma cadeia de caracteres ASCII codificada com base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="d5cfa-144">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="d5cfa-145">Os clientes que entram com a entidade de serviço também precisam acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-146">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="d5cfa-147">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte _imediatamente após_ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="d5cfa-148">Obter uma entidade de serviço existente</span><span class="sxs-lookup"><span data-stu-id="d5cfa-148">Get an existing service principal</span></span>

<span data-ttu-id="d5cfa-149">Uma lista de entidades de serviço do locatário ativo pode ser recuperada com [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="d5cfa-150">Por padrão, esse comando retorna _todas_ as entidades de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="d5cfa-151">Para grandes organizações, pode levar muito tempo para retornar resultados.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="d5cfa-152">Em vez disso, recomenda-se usar um dos argumentos de filtragem opcionais do lado do servidor:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="d5cfa-153">`-DisplayNameBeginsWith` solicita entidades de serviço que tenham um _prefixo_ que corresponda ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="d5cfa-154">O nome de exibição de uma entidade de serviço é o valor definido com `-DisplayName` durante a criação.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="d5cfa-155">`-DisplayName` solicita uma _correspondência exata_ de um nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="d5cfa-156">Gerenciar funções da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="d5cfa-156">Manage service principal roles</span></span>

<span data-ttu-id="d5cfa-157">O Azure PowerShell tem os seguintes cmdlets para gerenciar atribuições de função:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="d5cfa-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d5cfa-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="d5cfa-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d5cfa-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="d5cfa-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d5cfa-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="d5cfa-161">A função padrão de uma entidade de serviço de autenticação baseada em senha é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="d5cfa-162">Essa função tem permissões completas para ler e gravar em uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="d5cfa-163">A função **Leitor** é mais restritiva, com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="d5cfa-164">Para obter mais informações sobre o Controle de Acesso Baseado em Função (RBAC) e funções, confira [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="d5cfa-165">Esse exemplo adiciona a função **Leitor** e exclui a função **Colaborador**:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-166">Os cmdlets de atribuição de função não usam a ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="d5cfa-167">Eles usam a ID do aplicativo associado, que é gerada no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="d5cfa-168">Para obter a ID do aplicativo para uma entidade de serviço, use `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cfa-169">Caso sua conta não tenha permissão para atribuir uma função, você verá uma mensagem de erro informando que a sua conta "não tem autorização para executar a ação 'Microsoft.Authorization/roleAssignments/write'".</span><span class="sxs-lookup"><span data-stu-id="d5cfa-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="d5cfa-170">Entre em contato com o administrador do Azure Active Directory para gerenciar funções.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="d5cfa-171">Adicionar uma função _não_ restringe as permissões atribuídas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="d5cfa-172">Ao restringir as permissões da entidade de serviço, a função **Colaborador** deverá ser removida.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="d5cfa-173">Para verificar as alterações, liste as funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="d5cfa-174">Entrar usando uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="d5cfa-174">Sign in using a service principal</span></span>

<span data-ttu-id="d5cfa-175">Teste as novas credenciais e permissões da entidade de serviço iniciando a sessão.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="d5cfa-176">Para entrar com uma entidade de serviço, você precisa do valor `applicationId` associado a ela e do locatário com base no qual ela foi criada.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="d5cfa-177">Para entrar com uma entidade de serviço usando a senha:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="d5cfa-178">A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="d5cfa-179">Para obter instruções sobre como importar um certificado em um armazenamento de credenciais acessível pelo PowerShell, confira [Entrar com o Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="d5cfa-180">Redefinir credenciais</span><span class="sxs-lookup"><span data-stu-id="d5cfa-180">Reset credentials</span></span>

<span data-ttu-id="d5cfa-181">Se você esquecer as credenciais de uma entidade de serviço, use o comando [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) para adicionar uma nova credencial com uma senha aleatória.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="d5cfa-182">Esse cmdlet não dá suporte a credenciais definidas pelo usuário ao redefinir a senha.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cfa-183">Antes de atribuir quaisquer novas credenciais, talvez seja interessante remover as credenciais existentes para evitar entrar com elas.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="d5cfa-184">Para fazer isso, use o cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="d5cfa-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="d5cfa-185">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="d5cfa-185">Troubleshooting</span></span>

<span data-ttu-id="d5cfa-186">Se você receber o erro: _"New-AzADServicePrincipal: Outro objeto com o mesmo valor para a propriedade identifierUris já existe."_ Verifique se não existe uma entidade de serviço com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="d5cfa-187">Se a entidade de serviço existente não for mais necessária, você poderá removê-la usando o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="d5cfa-188">Esse erro também pode ocorrer quando você criou uma entidade de serviço anteriormente para um aplicativo do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="d5cfa-189">Se você remover a entidade de serviço, o aplicativo ainda estará disponível.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="d5cfa-190">Esse aplicativo impede que você crie outra entidade de serviço com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="d5cfa-191">Você pode usar o seguinte exemplo para verificar se não existe um aplicativo do Azure Active Directory com o mesmo nome:</span><span class="sxs-lookup"><span data-stu-id="d5cfa-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="d5cfa-192">Se um aplicativo com o mesmo nome existir e não for mais necessário, ele poderá ser removido usando o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="d5cfa-193">Caso contrário, escolha um nome alternativo para a entidade de serviço que você está tentando criar.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>