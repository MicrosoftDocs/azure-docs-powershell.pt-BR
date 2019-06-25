---
title: Usar as entidades de serviço do Azure com o Azure PowerShell
description: Saiba como criar e usar entidades de serviço com o Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: abb85d3d3f6a20697510447cda2c02b2703ef921
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2019
ms.locfileid: "67345369"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="ccd0f-103">Criar uma entidade de serviço do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ccd0f-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="ccd0f-104">Ferramentas automatizadas que usam os serviços do Azure devem sempre ter permissões restritas.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="ccd0f-105">Em vez de os aplicativos entrarem como um usuário com privilégio total, o Azure oferece as entidades de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="ccd0f-106">Uma entidade de serviço do Azure é uma identidade criada para uso com aplicativos, serviços hospedados e ferramentas automatizadas para acessar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="ccd0f-107">Esse acesso é restrito pelas funções atribuídas à entidade de serviço, oferecendo a você o controle sobre quais recursos poderão ser acessados e em qual nível.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="ccd0f-108">Por motivos de segurança, é sempre recomendado usar entidades de serviço com ferramentas automatizadas em vez de permitir a entrada com uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="ccd0f-109">Este artigo mostra as etapas para criar, obter informações e redefinir uma entidade de serviço com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="ccd0f-110">Criar uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ccd0f-110">Create a service principal</span></span>

<span data-ttu-id="ccd0f-111">Criar uma entidade de serviço com o cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="ccd0f-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="ccd0f-112">Ao criar uma entidade de serviço, você pode escolher o tipo de autenticação de entrada usada.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="ccd0f-113">Se sua conta não tiver permissão para criar uma entidade de serviço, `New-AzADServicePrincipal` mostrará uma mensagem de erro “Privilégios insuficientes para concluir a operação”.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="ccd0f-114">Entre em contato com o administrador do Azure Active Directory para criar uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="ccd0f-115">Há dois tipos de autenticação disponíveis para as entidades de serviço: A autenticação baseada em senha e em certificado.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="ccd0f-116">Autenticação baseada em senha</span><span class="sxs-lookup"><span data-stu-id="ccd0f-116">Password-based authentication</span></span>

<span data-ttu-id="ccd0f-117">Sem outros parâmetros de autenticação, usa-se a autenticação baseada em senha, com uma senha aleatória criada para você.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="ccd0f-118">Caso queira uma autenticação baseada em senha, esse método é recomendado.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="ccd0f-119">O objeto retornado contém o membro `Secret`, que é um `SecureString` que contém a senha gerada.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="ccd0f-120">Armazene esse valor em algum lugar seguro para autenticar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="ccd0f-121">Seu valor __não__ será exibido na saída do console.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="ccd0f-122">Se você perder a senha, [redefina as credenciais da entidade de serviço](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="ccd0f-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span> 

<span data-ttu-id="ccd0f-123">Para senhas fornecidas pelo usuário, o argumento `-PasswordCredential` usa os objetos `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-123">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="ccd0f-124">Esses objetos devem ter uma validade `StartDate` e `EndDate`, além de usar um texto sem formatação `Password`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-124">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="ccd0f-125">Quando criar uma senha, certifique-se de seguir as [Regras e restrições de senha do Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="ccd0f-125">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="ccd0f-126">Não use uma senha fraca, nem reutilize uma senha.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-126">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="ccd0f-127">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-127">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ccd0f-128">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-128">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="ccd0f-129">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-129">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="ccd0f-130">Autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="ccd0f-130">Certificate-based authentication</span></span>

<span data-ttu-id="ccd0f-131">As entidades de serviço que usam a autenticação baseada em certificado são criadas com o parâmetro `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-131">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="ccd0f-132">Esse parâmetro usa uma cadeia de caracteres ASCII codificada em base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-132">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="ccd0f-133">Isso é representado por um arquivo PEM ou por um CRT ou CER com texto codificado.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-133">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="ccd0f-134">Não há suporte para codificações binárias do certificado público.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-134">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="ccd0f-135">Essas instruções pressupõem que você já tenha um certificado disponível.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-135">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="ccd0f-136">Você também pode usar o parâmetro `-KeyCredential`, que usa objetos `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-136">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="ccd0f-137">Esses objetos devem ter um `StartDate` e `EndDate` válidos, além do membro `CertValue` definido como uma cadeia de caracteres ASCII codificada com base64 do certificado público.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-137">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="ccd0f-138">O objeto retornado por `New-AzADServicePrincipal` contém os membros `Id` e `DisplayName`, os quais podem ser usados para entrar com a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-138">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="ccd0f-139">Os clientes que entram com a entidade de serviço também precisam acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-139">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ccd0f-140">Para entrar com uma entidade de serviço é preciso ter a ID do locatário que serviu de base para a criação da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-140">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="ccd0f-141">Para obter o locatário ativo de quando a entidade de serviço foi criada, execute o comando seguinte __imediatamente após__ a criação da entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-141">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="ccd0f-142">Obter uma entidade de serviço existente</span><span class="sxs-lookup"><span data-stu-id="ccd0f-142">Get an existing service principal</span></span>

<span data-ttu-id="ccd0f-143">Uma lista de entidades de serviço para o locatário ativo no momento pode ser recuperada com [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="ccd0f-143">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="ccd0f-144">Por padrão, esse comando retorna __todas__ as entidades de serviço em um locatário, ou seja, para grandes organizações, pode demorar bastante para retornar resultados.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-144">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="ccd0f-145">Em vez disso, recomenda-se usar um dos argumentos de filtragem opcionais do lado do servidor:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-145">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="ccd0f-146">`-DisplayNameBeginsWith` solicita entidades de serviço que tenham um _prefixo_ que corresponda ao valor fornecido.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-146">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="ccd0f-147">O nome de exibição de uma entidade de serviço é o valor definido com `-DisplayName` durante a criação.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-147">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="ccd0f-148">`-DisplayName` solicita uma _correspondência exata_ de um nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-148">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="ccd0f-149">Gerenciar funções da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ccd0f-149">Manage service principal roles</span></span>

<span data-ttu-id="ccd0f-150">O Azure PowerShell tem os seguintes cmdlets para gerenciar atribuições de função:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-150">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="ccd0f-151">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ccd0f-151">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="ccd0f-152">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ccd0f-152">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="ccd0f-153">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ccd0f-153">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="ccd0f-154">A função padrão para uma entidade de serviço é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-154">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="ccd0f-155">Essa função tem permissões completas para ler e gravar em uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-155">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="ccd0f-156">A função **Leitor** é mais restritiva, com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-156">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="ccd0f-157">Para obter mais informações sobre o Controle de Acesso Baseado em Função (RBAC) e funções, confira [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="ccd0f-157">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="ccd0f-158">Esse exemplo adiciona a função **Leitor** e exclui a função **Colaborador**:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-158">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="ccd0f-159">Os cmdlets de atribuição de função não usam a ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-159">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="ccd0f-160">Eles usam a ID do aplicativo associado, que é gerada no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-160">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="ccd0f-161">Para obter a ID do aplicativo para uma entidade de serviço, use `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-161">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd0f-162">Caso sua conta não tenha permissão para atribuir uma função, você verá uma mensagem de erro informando que sua conta “não tem autorização para executar a ação ‘Microsoft.Authorization/roleAssignments/write’”. Entre em contato com o administrador do Azure Active Directory para gerenciar funções.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-162">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="ccd0f-163">Adicionar uma função _não_ restringe as permissões atribuídas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-163">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="ccd0f-164">Ao restringir as permissões da entidade de serviço, a função __Colaborador__ deverá ser removida.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-164">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="ccd0f-165">Para verificar as alterações, liste as funções atribuídas:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-165">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="ccd0f-166">Entrar usando uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ccd0f-166">Sign in using a service principal</span></span>

<span data-ttu-id="ccd0f-167">Teste as novas credenciais e permissões da entidade de serviço iniciando a sessão.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-167">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="ccd0f-168">Para entrar com uma entidade de serviço, você precisa do valor `applicationId` associado a ela e do locatário com base no qual ela foi criada.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-168">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="ccd0f-169">Para entrar com uma entidade de serviço usando a senha:</span><span class="sxs-lookup"><span data-stu-id="ccd0f-169">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="ccd0f-170">A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-170">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="ccd0f-171">Para obter instruções sobre como importar um certificado em um armazenamento de credenciais acessível pelo PowerShell, confira [Entrar com o Azure PowerShell](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="ccd0f-171">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="ccd0f-172">Redefinir credenciais</span><span class="sxs-lookup"><span data-stu-id="ccd0f-172">Reset credentials</span></span>

<span data-ttu-id="ccd0f-173">Se você esquecer das credenciais de uma entidade de serviço, use o comando [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) para adicionar uma nova credencial.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-173">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="ccd0f-174">Esse cmdlet usa os mesmos argumentos e tipos de credencial que `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-174">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="ccd0f-175">Sem nenhum argumento de credencial, é criado um novo `PasswordCredential` com uma senha aleatória.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-175">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccd0f-176">Antes de atribuir quaisquer novas credenciais, talvez seja interessante remover as credenciais existentes para evitar entrar com elas.</span><span class="sxs-lookup"><span data-stu-id="ccd0f-176">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="ccd0f-177">Para fazer isso, use o cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="ccd0f-177">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
