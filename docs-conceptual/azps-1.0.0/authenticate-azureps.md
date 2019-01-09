---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786672"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="dd6cb-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd6cb-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="dd6cb-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="dd6cb-105">É a maneira mais simples para entrar interativamente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="dd6cb-106">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="dd6cb-106">Sign in interactively</span></span>

<span data-ttu-id="dd6cb-107">Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="dd6cb-108">Quando executado, esse cmdlet apresentará uma cadeia de caracteres de token.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="dd6cb-109">Para fazer logon, copie essa cadeia de caracteres e cole-a na https://microsoft.com/devicelogin em um navegador.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="dd6cb-110">Sua sessão do PowerShell, em seguida, será autenticada para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="dd6cb-111">Essa autenticação dura o tempo da sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="dd6cb-112">Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="dd6cb-113">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="dd6cb-114">Entrar com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="dd6cb-114">Sign in with a service principal</span></span>

<span data-ttu-id="dd6cb-115">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="dd6cb-116">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="dd6cb-117">Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="dd6cb-118">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="dd6cb-119">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="dd6cb-120">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="dd6cb-121">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="dd6cb-122">Esse cmdlet apresentará um prompt para a ID de usuário e a senha da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="dd6cb-123">Entre usando uma Identidade de Serviço Gerenciada do Azure</span><span class="sxs-lookup"><span data-stu-id="dd6cb-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="dd6cb-124">Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="dd6cb-125">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="dd6cb-126">As identidades gerenciadas só estão disponíveis em máquinas virtuais em execução em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="dd6cb-127">Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="dd6cb-128">Entrar como um Provedor de Soluções na Nuvem (CSP)</span><span class="sxs-lookup"><span data-stu-id="dd6cb-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="dd6cb-129">Entrar no [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) requer o uso de `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="dd6cb-130">Normalmente, esse parâmetro pode ser fornecido como uma ID de locatário ou nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="dd6cb-131">No entanto, para entrar no CSP, deve ser fornecido uma **ID de locatário**.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="dd6cb-132">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="dd6cb-132">Sign in to another Cloud</span></span>

<span data-ttu-id="dd6cb-133">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com os regulamentos de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="dd6cb-134">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="dd6cb-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="dd6cb-135">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="dd6cb-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="dd6cb-136">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="dd6cb-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="dd6cb-137">Saiba mais sobre como gerenciar o acesso baseado em função do Azure</span><span class="sxs-lookup"><span data-stu-id="dd6cb-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="dd6cb-138">Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).</span><span class="sxs-lookup"><span data-stu-id="dd6cb-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="dd6cb-139">Cmdlets do Azure PowerShell para gerenciamento de função:</span><span class="sxs-lookup"><span data-stu-id="dd6cb-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="dd6cb-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dd6cb-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="dd6cb-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dd6cb-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="dd6cb-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dd6cb-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="dd6cb-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dd6cb-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="dd6cb-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dd6cb-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="dd6cb-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dd6cb-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="dd6cb-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dd6cb-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
