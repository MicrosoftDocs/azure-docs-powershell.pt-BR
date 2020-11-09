---
title: Usar as entidades de serviço do Azure com o Azure PowerShell
description: Saiba como criar e usar entidades de serviço com o Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: cea6b53a6780e6a3b73165a9af744b12c545013e
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365119"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="f68c8-103">Criar uma entidade de serviço do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f68c8-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="f68c8-104">Ferramentas automatizadas que usam os serviços do Azure devem sempre ter permissões restritas.</span><span class="sxs-lookup"><span data-stu-id="f68c8-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="f68c8-105">Em vez de os aplicativos entrarem como um usuário com privilégio total, o Azure oferece as entidades de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="f68c8-106">Uma entidade de serviço do Azure é uma identidade criada para uso com aplicativos, serviços hospedados e ferramentas automatizadas para acessar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f68c8-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="f68c8-107">Esse acesso é restrito pelas funções atribuídas à entidade de serviço, oferecendo a você o controle sobre quais recursos poderão ser acessados e em qual nível.</span><span class="sxs-lookup"><span data-stu-id="f68c8-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="f68c8-108">Por motivos de segurança, é sempre recomendado usar entidades de serviço com ferramentas automatizadas em vez de permitir a entrada com uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="f68c8-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="f68c8-109">Este artigo mostra as etapas para criar, obter informações e redefinir uma entidade de serviço com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f68c8-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="f68c8-110">Criar uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f68c8-110">Create a service principal</span></span>

> [!WARNING]
> <span data-ttu-id="f68c8-111">Quando você cria uma entidade de serviço usando o comando [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal), a saída inclui as credenciais que você precisa proteger.</span><span class="sxs-lookup"><span data-stu-id="f68c8-111">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="f68c8-112">Lembre-se de não incluir essas credenciais em seu código ou de verificar as credenciais em seu controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f68c8-112">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="f68c8-113">Como alternativa, considere usar [identidades gerenciadas](/azure/active-directory/managed-identities-azure-resources/overview) para evitar a necessidade de usar credenciais.</span><span class="sxs-lookup"><span data-stu-id="f68c8-113">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="f68c8-114">Por padrão, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) atribui a função [Colaborador](/azure/role-based-access-control/built-in-roles#contributor) à entidade de serviço no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f68c8-114">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="f68c8-115">Para reduzir o risco de uma entidade de serviço comprometida, atribua uma função mais específica e restrinja o escopo a um recurso ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f68c8-115">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="f68c8-116">Confira [Etapas para adicionar uma atribuição de função](/azure/role-based-access-control/role-assignments-steps) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f68c8-116">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

<span data-ttu-id="f68c8-117">Criar uma entidade de serviço com o cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="f68c8-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="f68c8-118">Ao criar uma entidade de serviço, você pode escolher o tipo de autenticação de entrada usada.</span><span class="sxs-lookup"><span data-stu-id="f68c8-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="f68c8-119">Se sua conta não tiver permissão para criar uma entidade de serviço, `New-AzADServicePrincipal` mostrará uma mensagem de erro “Privilégios insuficientes para concluir a operação”.</span><span class="sxs-lookup"><span data-stu-id="f68c8-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="f68c8-120">Entre em contato com o administrador do Azure Active Directory para criar uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="f68c8-121">Há dois tipos de autenticação disponíveis para as entidades de serviço: A autenticação baseada em senha e em certificado.</span><span class="sxs-lookup"><span data-stu-id="f68c8-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="f68c8-122">Autenticação baseada em senha</span><span class="sxs-lookup"><span data-stu-id="f68c8-122">Password-based authentication</span></span>

<span data-ttu-id="f68c8-123">Sem outros parâmetros de autenticação, usa-se a autenticação baseada em senha, com uma senha aleatória criada para você.</span><span class="sxs-lookup"><span data-stu-id="f68c8-123">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="f68c8-124">Caso queira uma autenticação baseada em senha, esse método é recomendado.</span><span class="sxs-lookup"><span data-stu-id="f68c8-124">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="f68c8-125">O objeto retornado contém o membro `Secret`, que é um `SecureString` que contém a senha gerada.</span><span class="sxs-lookup"><span data-stu-id="f68c8-125">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="f68c8-126">Armazene esse valor em algum lugar seguro para autenticar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-126">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="f68c8-127">Seu valor __não__ será exibido na saída do console.</span><span class="sxs-lookup"><span data-stu-id="f68c8-127">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="f68c8-128">Se você perder a senha, [redefina as credenciais da entidade de serviço](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="f68c8-128">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="f68c8-129">O código a seguir permitirá que você exporte o segredo:</span><span class="sxs-lookup"><span data-stu-id="f68c8-129">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="f68c8-130">Para senhas fornecidas pelo usuário, o argumento `-PasswordCredential` usa os objetos `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-130">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="f68c8-131">Esses objetos devem ter uma validade `StartDate` e `EndDate`, além de usar um texto sem formatação `Password`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-131">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="f68c8-132">Quando criar uma senha, certifique-se de seguir as [Regras e restrições de senha do Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="f68c8-132">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="f68c8-133">Não use uma senha fraca, nem reutilize uma senha.</span><span class="sxs-lookup"><span data-stu-id="f68c8-133">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="f68c8-134">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-134">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f68c8-135">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-135">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="f68c8-136">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="f68c8-136">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="f68c8-137">Autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="f68c8-137">Certificate-based authentication</span></span>

<span data-ttu-id="f68c8-138">As entidades de serviço que usam a autenticação baseada em certificado são criadas com o parâmetro `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-138">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="f68c8-139">Esse parâmetro usa uma cadeia de caracteres ASCII codificada em base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="f68c8-139">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="f68c8-140">Isso é representado por um arquivo PEM ou por um CRT ou CER com texto codificado.</span><span class="sxs-lookup"><span data-stu-id="f68c8-140">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="f68c8-141">Não há suporte para codificações binárias do certificado público.</span><span class="sxs-lookup"><span data-stu-id="f68c8-141">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="f68c8-142">Essas instruções pressupõem que você já tenha um certificado disponível.</span><span class="sxs-lookup"><span data-stu-id="f68c8-142">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="f68c8-143">Você também pode usar o parâmetro `-KeyCredential`, que usa objetos `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-143">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="f68c8-144">Esses objetos devem ter um `StartDate` e `EndDate` válidos, além do membro `CertValue` definido como uma cadeia de caracteres ASCII codificada com base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="f68c8-144">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="f68c8-145">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-145">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="f68c8-146">Os clientes que entram com a entidade de serviço também precisam acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="f68c8-146">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f68c8-147">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-147">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="f68c8-148">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="f68c8-148">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="f68c8-149">Obter uma entidade de serviço existente</span><span class="sxs-lookup"><span data-stu-id="f68c8-149">Get an existing service principal</span></span>

<span data-ttu-id="f68c8-150">Uma lista de entidades de serviço para o locatário ativo no momento pode ser recuperada com [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="f68c8-150">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="f68c8-151">Por padrão, esse comando retorna __todas__ as entidades de serviço em um locatário, ou seja, para grandes organizações, pode demorar bastante para retornar resultados.</span><span class="sxs-lookup"><span data-stu-id="f68c8-151">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="f68c8-152">Em vez disso, recomenda-se usar um dos argumentos de filtragem opcionais do lado do servidor:</span><span class="sxs-lookup"><span data-stu-id="f68c8-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="f68c8-153">`-DisplayNameBeginsWith` solicita entidades de serviço que tenham um _prefixo_ que corresponda ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="f68c8-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="f68c8-154">O nome de exibição de uma entidade de serviço é o valor definido com `-DisplayName` durante a criação.</span><span class="sxs-lookup"><span data-stu-id="f68c8-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="f68c8-155">`-DisplayName` solicita uma _correspondência exata_ de um nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="f68c8-156">Gerenciar funções da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f68c8-156">Manage service principal roles</span></span>

<span data-ttu-id="f68c8-157">O Azure PowerShell tem os seguintes cmdlets para gerenciar atribuições de função:</span><span class="sxs-lookup"><span data-stu-id="f68c8-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="f68c8-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f68c8-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="f68c8-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f68c8-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="f68c8-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f68c8-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="f68c8-161">A função padrão para uma entidade de serviço é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="f68c8-161">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="f68c8-162">Essa função tem permissões completas para ler e gravar em uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="f68c8-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="f68c8-163">A função **Leitor** é mais restritiva, com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f68c8-163">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="f68c8-164">Para obter mais informações sobre o Controle de Acesso Baseado em Função (RBAC) e funções, confira [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="f68c8-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="f68c8-165">Esse exemplo adiciona a função **Leitor** e exclui a função **Colaborador** :</span><span class="sxs-lookup"><span data-stu-id="f68c8-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="f68c8-166">Os cmdlets de atribuição de função não usam a ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f68c8-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="f68c8-167">Eles usam a ID do aplicativo associado, que é gerada no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="f68c8-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="f68c8-168">Para obter a ID do aplicativo para uma entidade de serviço, use `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="f68c8-169">Caso sua conta não tenha permissão para atribuir uma função, você verá uma mensagem de erro informando que sua conta “não tem autorização para executar a ação ‘Microsoft.Authorization/roleAssignments/write’”. Entre em contato com o administrador do Azure Active Directory para gerenciar funções.</span><span class="sxs-lookup"><span data-stu-id="f68c8-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="f68c8-170">Adicionar uma função _não_ restringe as permissões atribuídas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f68c8-170">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="f68c8-171">Ao restringir as permissões da entidade de serviço, a função __Colaborador__ deverá ser removida.</span><span class="sxs-lookup"><span data-stu-id="f68c8-171">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="f68c8-172">Para verificar as alterações, liste as funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="f68c8-172">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="f68c8-173">Entrar usando uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f68c8-173">Sign in using a service principal</span></span>

<span data-ttu-id="f68c8-174">Teste as novas credenciais e permissões da entidade de serviço iniciando a sessão.</span><span class="sxs-lookup"><span data-stu-id="f68c8-174">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="f68c8-175">Para entrar com uma entidade de serviço, você precisa do valor `applicationId` associado a ela e do locatário com base no qual ela foi criada.</span><span class="sxs-lookup"><span data-stu-id="f68c8-175">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="f68c8-176">Para entrar com uma entidade de serviço usando a senha:</span><span class="sxs-lookup"><span data-stu-id="f68c8-176">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="f68c8-177">A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="f68c8-177">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="f68c8-178">Para obter instruções sobre como importar um certificado em um armazenamento de credenciais acessível pelo PowerShell, confira [Entrar com o Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="f68c8-178">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="f68c8-179">Redefinir credenciais</span><span class="sxs-lookup"><span data-stu-id="f68c8-179">Reset credentials</span></span>

<span data-ttu-id="f68c8-180">Se você esquecer das credenciais de uma entidade de serviço, use o comando [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) para adicionar uma nova credencial.</span><span class="sxs-lookup"><span data-stu-id="f68c8-180">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="f68c8-181">Esse cmdlet usa os mesmos argumentos e tipos de credencial que `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="f68c8-181">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="f68c8-182">Sem nenhum argumento de credencial, é criado um novo `PasswordCredential` com uma senha aleatória.</span><span class="sxs-lookup"><span data-stu-id="f68c8-182">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f68c8-183">Antes de atribuir quaisquer novas credenciais, talvez seja interessante remover as credenciais existentes para evitar entrar com elas.</span><span class="sxs-lookup"><span data-stu-id="f68c8-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="f68c8-184">Para fazer isso, use o cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="f68c8-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
