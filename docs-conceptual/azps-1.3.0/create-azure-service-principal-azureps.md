---
title: Criar uma entidade de serviço do Azure com o Azure PowerShell
description: Saiba como criar uma entidade de serviço para seu aplicativo ou serviço com o Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153002"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="674cb-104">Criar uma entidade de serviço do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="674cb-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="674cb-105">Se você planeja gerenciar seu aplicativo ou serviço com o Azure PowerShell, execute-o em uma entidade de serviço do Azure Active Directory (AAD), em vez de suas próprias credenciais.</span><span class="sxs-lookup"><span data-stu-id="674cb-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="674cb-106">Este artigo serve de guia para você criar uma entidade de segurança com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="674cb-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="674cb-107">O que é uma entidade de serviço?</span><span class="sxs-lookup"><span data-stu-id="674cb-107">What is a service principal?</span></span>

<span data-ttu-id="674cb-108">Uma entidade de serviço do Azure é uma identidade de segurança usada por aplicativos criados pelo usuário, serviços e ferramentas de automação para acessar recursos específicos do Azure.</span><span class="sxs-lookup"><span data-stu-id="674cb-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="674cb-109">As entidades de serviço recebem permissões específicas relacionadas às suas tarefas, dando a você um melhor controle de segurança.</span><span class="sxs-lookup"><span data-stu-id="674cb-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="674cb-110">Isso é diferente de uma identidade de usuário geral, que geralmente está autorizada a fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="674cb-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="674cb-111">Verificar seu próprio nível de permissão</span><span class="sxs-lookup"><span data-stu-id="674cb-111">Verify your own permission level</span></span>

<span data-ttu-id="674cb-112">Primeiro, você deve ter permissões suficientes no Azure Active Directory e em sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="674cb-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="674cb-113">Você deve ser capaz de criar um aplicativo no Active Directory e atribuir uma função à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="674cb-114">A maneira mais fácil de verificar se a sua conta tem as permissões certas é por meio do portal.</span><span class="sxs-lookup"><span data-stu-id="674cb-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="674cb-115">Consulte [Verificar permissão necessária no portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="674cb-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="674cb-116">Criar uma entidade de serviço para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="674cb-116">Create a service principal for your app</span></span>

<span data-ttu-id="674cb-117">Após entrar na sua conta do Azure, você poderá criar a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="674cb-118">Você deve ter uma das maneiras a seguir para identificar seu aplicativo implantado:</span><span class="sxs-lookup"><span data-stu-id="674cb-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="674cb-119">O nome exclusivo do seu aplicativo implantado, como "MyDemoWebApp" nos exemplos a seguir</span><span class="sxs-lookup"><span data-stu-id="674cb-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="674cb-120">A ID do Aplicativo, o GUID exclusivo associado ao seu aplicativo, serviço ou objeto implantado</span><span class="sxs-lookup"><span data-stu-id="674cb-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="674cb-121">Obter informações sobre seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="674cb-121">Get information about your application</span></span>

<span data-ttu-id="674cb-122">O cmdlet `Get-AzADApplication` pode ser usado para obter informações sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="674cb-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="674cb-123">Criar uma entidade de serviço para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="674cb-123">Create a service principal for your application</span></span>

<span data-ttu-id="674cb-124">O cmdlet `New-AzADServicePrincipal` é usado para criar a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
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

<span data-ttu-id="674cb-125">A partir daqui, você pode também usar diretamente a propriedade `$servicePrincipal.Secret` como um argumento para `Connect-AzAccount` (confira "Entrar usando a entidade de serviço"), ou você pode converter esta `SecureString` para uma cadeia de caracteres de texto sem formatação:</span><span class="sxs-lookup"><span data-stu-id="674cb-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="674cb-126">Entrar usando a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-126">Sign in using the service principal</span></span>

<span data-ttu-id="674cb-127">Agora você pode entrar como a nova entidade de serviço para seu aplicativo usando a `appId` que você forneceu e a `password` que foi</span><span class="sxs-lookup"><span data-stu-id="674cb-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="674cb-128">gerada.</span><span class="sxs-lookup"><span data-stu-id="674cb-128">generated.</span></span> <span data-ttu-id="674cb-129">Você também precisa da ID do Locatário para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="674cb-130">Sua ID do Locatário é exibida quando você entra no Azure com suas credenciais pessoais.</span><span class="sxs-lookup"><span data-stu-id="674cb-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="674cb-131">Para entrar com uma entidade de serviço, use os comandos:</span><span class="sxs-lookup"><span data-stu-id="674cb-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="674cb-132">Após conseguir entrar, você verá um resultado do tipo:</span><span class="sxs-lookup"><span data-stu-id="674cb-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="674cb-133">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="674cb-133">Congratulations!</span></span> <span data-ttu-id="674cb-134">Você pode usar essas credenciais para executar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="674cb-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="674cb-135">Em seguida, será necessário ajustar as permissões da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="674cb-136">Gerenciamento de funções</span><span class="sxs-lookup"><span data-stu-id="674cb-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="674cb-137">O RBAC (Controle de Acesso do Azure Baseado em Função) é um modelo para definir e gerenciar funções para entidades de usuário e de serviço.</span><span class="sxs-lookup"><span data-stu-id="674cb-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="674cb-138">As funções têm conjuntos de permissões associados a elas, que determinam os recursos que uma entidade pode ler, acessar, gravar ou gerenciar.</span><span class="sxs-lookup"><span data-stu-id="674cb-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="674cb-139">Para saber mais sobre RBAC e funções, veja [RBAC: Funções internas](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="674cb-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="674cb-140">O Azure PowerShell fornece os seguintes cmdlets para gerenciar atribuições de função:</span><span class="sxs-lookup"><span data-stu-id="674cb-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="674cb-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="674cb-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="674cb-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="674cb-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="674cb-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="674cb-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="674cb-144">A função padrão para uma entidade de serviço é **Colaborador**.</span><span class="sxs-lookup"><span data-stu-id="674cb-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="674cb-145">Pode não ser a melhor opção, dependendo do escopo das interações do seu aplicativo com os serviços do Azure, dadas suas permissões amplas.</span><span class="sxs-lookup"><span data-stu-id="674cb-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="674cb-146">A função **Leitor** é mais restritiva e pode ser uma boa opção para aplicativos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="674cb-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="674cb-147">Você pode exibir detalhes sobre as permissões específicas de função ou criar conectores personalizados por meio do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="674cb-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="674cb-148">Neste exemplo, adicionamos a função **Leitor** ao nosso exemplo anterior e excluímos a função **Colaborador**:</span><span class="sxs-lookup"><span data-stu-id="674cb-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="674cb-149">Para exibir as funções atuais atribuídas:</span><span class="sxs-lookup"><span data-stu-id="674cb-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="674cb-150">Outros cmdlets do Azure PowerShell para gerenciamento de funções:</span><span class="sxs-lookup"><span data-stu-id="674cb-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="674cb-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="674cb-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="674cb-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="674cb-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="674cb-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="674cb-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="674cb-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="674cb-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="674cb-155">Alterar as credenciais da entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="674cb-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="674cb-156">É uma boa prática de segurança examinar as permissões e atualizar a senha regularmente.</span><span class="sxs-lookup"><span data-stu-id="674cb-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="674cb-157">Talvez você queira gerenciar e modificar as credenciais de segurança à medida que seu aplicativo muda.</span><span class="sxs-lookup"><span data-stu-id="674cb-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="674cb-158">Por exemplo, podemos alterar a senha da entidade de serviço criando uma nova senha e removendo a antiga.</span><span class="sxs-lookup"><span data-stu-id="674cb-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="674cb-159">Adicionar uma nova senha para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="674cb-160">Obter uma lista de credenciais para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="674cb-161">Remover a senha antiga da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="674cb-162">Verificar a lista de credenciais para a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="674cb-163">Obter informações sobre a entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="674cb-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
