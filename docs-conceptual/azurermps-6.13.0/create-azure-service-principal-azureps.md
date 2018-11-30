---
title: Criar uma entidade de serviço do Azure com o Azure PowerShell
description: Saiba como criar uma entidade de serviço para seu aplicativo ou serviço com o Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2db1ada32e5a9285c27ec3f569b622c9c33a06b0
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587798"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="29929-104">Criar uma entidade de serviço do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29929-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="29929-105">Se você planeja gerenciar seu aplicativo ou serviço com o Azure PowerShell, execute-o em uma entidade de serviço do Azure Active Directory (AAD), em vez de suas próprias credenciais.</span><span class="sxs-lookup"><span data-stu-id="29929-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="29929-106">Este artigo serve de guia para você criar uma entidade de segurança com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29929-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="29929-107">Você também pode criar uma entidade de serviço por meio do Portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="29929-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="29929-108">Leia [Usar o portal para criar um aplicativo e entidade de serviço do Active Directory que pode acessar recursos](/azure/azure-resource-manager/resource-group-create-service-principal-portal) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="29929-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="29929-109">O que é uma ‘entidade de serviço’?</span><span class="sxs-lookup"><span data-stu-id="29929-109">What is a 'service principal'?</span></span>

<span data-ttu-id="29929-110">Uma entidade de serviço do Azure é uma identidade de segurança usada por aplicativos criados pelo usuário, serviços e ferramentas de automação para acessar recursos específicos do Azure.</span><span class="sxs-lookup"><span data-stu-id="29929-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="29929-111">Pense nela como uma “identidade de usuário” (nome de usuário e senha ou certificado) com uma função específica e permissões rigidamente controladas.</span><span class="sxs-lookup"><span data-stu-id="29929-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="29929-112">Uma entidade de serviço só precisa fazer coisas específicas, ao contrário de uma identidade de usuário geral.</span><span class="sxs-lookup"><span data-stu-id="29929-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="29929-113">A segurança aumenta se você só conceder a ela o nível mínimo de permissões necessárias para realizar suas tarefas de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="29929-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="29929-114">Verificar seu próprio nível de permissão</span><span class="sxs-lookup"><span data-stu-id="29929-114">Verify your own permission level</span></span>

<span data-ttu-id="29929-115">Primeiro, você deve ter permissões suficientes no Azure Active Directory e em sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="29929-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="29929-116">Você deve ser capaz de criar um aplicativo no Active Directory e atribuir uma função à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="29929-117">A maneira mais fácil de verificar se a sua conta tem as permissões certas é por meio do portal.</span><span class="sxs-lookup"><span data-stu-id="29929-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="29929-118">Consulte [Verificar permissão necessária no portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="29929-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="29929-119">Criar uma entidade de serviço para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="29929-119">Create a service principal for your app</span></span>

<span data-ttu-id="29929-120">Após entrar na sua conta do Azure, você poderá criar a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="29929-121">Você deve ter uma das maneiras a seguir para identificar seu aplicativo implantado:</span><span class="sxs-lookup"><span data-stu-id="29929-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="29929-122">O nome exclusivo do seu aplicativo implantado, como "MyDemoWebApp" nos exemplos a seguir ou</span><span class="sxs-lookup"><span data-stu-id="29929-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="29929-123">A ID do Aplicativo, o GUID exclusivo associado ao seu aplicativo, serviço ou objeto implantado</span><span class="sxs-lookup"><span data-stu-id="29929-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="29929-124">Obter informações sobre seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="29929-124">Get information about your application</span></span>

<span data-ttu-id="29929-125">O cmdlet `Get-AzureRmADApplication` pode ser usado para obter informações sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="29929-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="29929-126">Criar uma entidade de serviço para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="29929-126">Create a service principal for your application</span></span>

<span data-ttu-id="29929-127">O cmdlet `New-AzureRmADServicePrincipal` é usado para criar a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="29929-128">A partir daqui, você pode usar a propriedade $servicePrincipal.Secret diretamente em Connect-AzureRmAccount (confira “Entrar usando a entidade de serviço” presente a seguir) ou pode converter esse SecureString em uma cadeia de caracteres de texto sem formatação para uso posterior:</span><span class="sxs-lookup"><span data-stu-id="29929-128">From here, you can either directly use the $servicePrincipal.Secret property in Connect-AzureRmAccount (see "Sign in using the service principal" below), or you can convert this SecureString to a plain text string for later usage:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="29929-129">Entrar usando a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-129">Sign in using the service principal</span></span>

<span data-ttu-id="29929-130">Agora você pode entrar como a nova entidade de serviço para seu aplicativo usando a *appId* fornecida e a *senha* que foi gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="29929-130">You can now sign in as the new service principal for your app using the *appId* you provided and *password* that was automatically generated.</span></span> <span data-ttu-id="29929-131">Você também precisa da ID do Locatário para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="29929-132">Sua ID do Locatário é exibida quando você entra no Azure com suas credenciais pessoais.</span><span class="sxs-lookup"><span data-stu-id="29929-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="29929-133">Para entrar com uma entidade de serviço, use os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="29929-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="29929-134">Após conseguir entrar, você verá um resultado do tipo:</span><span class="sxs-lookup"><span data-stu-id="29929-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="29929-135">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="29929-135">Congratulations!</span></span> <span data-ttu-id="29929-136">Você pode usar essas credenciais para executar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="29929-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="29929-137">Em seguida, será necessário ajustar as permissões da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="29929-138">Gerenciamento de funções</span><span class="sxs-lookup"><span data-stu-id="29929-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="29929-139">O RBAC (Controle de Acesso do Azure Baseado em Função) é um modelo para definir e gerenciar funções para entidades de usuário e de serviço.</span><span class="sxs-lookup"><span data-stu-id="29929-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="29929-140">As funções têm conjuntos de permissões associados a elas, que determinam os recursos que uma entidade pode ler, acessar, gravar ou gerenciar.</span><span class="sxs-lookup"><span data-stu-id="29929-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="29929-141">Para saber mais sobre funções e RBAC, veja [RBAC: funções internas](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="29929-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="29929-142">O Azure PowerShell fornece os seguintes cmdlets para gerenciar atribuições de função:</span><span class="sxs-lookup"><span data-stu-id="29929-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="29929-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29929-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="29929-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29929-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="29929-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="29929-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="29929-146">A função padrão para uma entidade de serviço é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="29929-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="29929-147">Pode não ser a melhor opção, dependendo do escopo das interações do seu aplicativo com os serviços do Azure, dadas suas permissões amplas.</span><span class="sxs-lookup"><span data-stu-id="29929-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="29929-148">A função **Leitor** é mais restritiva e pode ser uma boa opção para aplicativos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="29929-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="29929-149">Você pode exibir detalhes sobre as permissões específicas de função ou criar conectores personalizados por meio do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="29929-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="29929-150">Neste exemplo, adicionamos a função **Leitor** ao nosso exemplo anterior e excluímos a função **Colaborador**:</span><span class="sxs-lookup"><span data-stu-id="29929-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="29929-151">Para exibir as funções atuais atribuídas:</span><span class="sxs-lookup"><span data-stu-id="29929-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="29929-152">Outros cmdlets do Azure PowerShell para gerenciamento de funções:</span><span class="sxs-lookup"><span data-stu-id="29929-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="29929-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="29929-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="29929-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="29929-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="29929-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="29929-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="29929-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="29929-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="29929-157">Alterar as credenciais da entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="29929-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="29929-158">É uma boa prática de segurança examinar as permissões e atualizar a senha regularmente.</span><span class="sxs-lookup"><span data-stu-id="29929-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="29929-159">Talvez você queira gerenciar e modificar as credenciais de segurança à medida que seu aplicativo muda.</span><span class="sxs-lookup"><span data-stu-id="29929-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="29929-160">Por exemplo, podemos alterar a senha da entidade de serviço criando uma nova senha e removendo a antiga.</span><span class="sxs-lookup"><span data-stu-id="29929-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="29929-161">Adicionar uma nova senha para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="29929-162">Obter uma lista de credenciais para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="29929-163">Remover a senha antiga da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="29929-164">Verificar a lista de credenciais para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="29929-165">Obter informações sobre a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="29929-165">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
