---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 92d9f7ed3c3cc111683fb6bf0f66107b73b7e96c
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982885"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="b36c3-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b36c3-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="b36c3-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b36c3-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="b36c3-105">É a maneira mais simples para entrar interativamente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b36c3-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="b36c3-106">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="b36c3-106">Sign in interactively</span></span>

<span data-ttu-id="b36c3-107">Para entrar no modo interativo, use o cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="b36c3-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="b36c3-108">Quando executado, esse cmdlet exibirá uma caixa de diálogo solicitando seu endereço de email e a senha associados à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="b36c3-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="b36c3-109">Essa autenticação dura o tempo da sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b36c3-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b36c3-110">A partir do Azure PowerShell 6.3.0, suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado ao Windows.</span><span class="sxs-lookup"><span data-stu-id="b36c3-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="b36c3-111">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="b36c3-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="b36c3-112">Entrar com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="b36c3-112">Sign in with a service principal</span></span>

<span data-ttu-id="b36c3-113">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="b36c3-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="b36c3-114">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b36c3-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="b36c3-115">Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.</span><span class="sxs-lookup"><span data-stu-id="b36c3-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="b36c3-116">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b36c3-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="b36c3-117">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="b36c3-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="b36c3-118">Você também precisará das credenciais de entrada da entidade de serviço e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b36c3-118">You'll also need the service principal's sign-in credentials and the tenant ID associated with the service principal.</span></span> <span data-ttu-id="b36c3-119">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="b36c3-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="b36c3-120">Esse cmdlet exibirá uma caixa de diálogo para inserir a ID de usuário da entidade de serviço e a senha.</span><span class="sxs-lookup"><span data-stu-id="b36c3-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="b36c3-121">Entre usando uma Identidade de Serviço Gerenciada do Azure</span><span class="sxs-lookup"><span data-stu-id="b36c3-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="b36c3-122">Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b36c3-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="b36c3-123">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="b36c3-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="b36c3-124">As identidades gerenciadas só estão disponíveis em máquinas virtuais em execução em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="b36c3-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="b36c3-125">Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="b36c3-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="b36c3-126">Entrar como um Provedor de Soluções na Nuvem (CSP)</span><span class="sxs-lookup"><span data-stu-id="b36c3-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="b36c3-127">Entrar no [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) requer o uso de `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="b36c3-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="b36c3-128">Normalmente, esse parâmetro pode ser fornecido como uma ID de locatário ou nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="b36c3-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="b36c3-129">No entanto, para entrar no CSP, deve ser fornecido uma **ID de locatário**.</span><span class="sxs-lookup"><span data-stu-id="b36c3-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="b36c3-130">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="b36c3-130">Sign in to another Cloud</span></span>

<span data-ttu-id="b36c3-131">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com os regulamentos de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="b36c3-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="b36c3-132">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="b36c3-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="b36c3-133">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="b36c3-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="b36c3-134">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="b36c3-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="b36c3-135">Saiba mais sobre como gerenciar o acesso baseado em função do Azure</span><span class="sxs-lookup"><span data-stu-id="b36c3-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="b36c3-136">Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).</span><span class="sxs-lookup"><span data-stu-id="b36c3-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="b36c3-137">Cmdlets do Azure PowerShell para gerenciamento de função:</span><span class="sxs-lookup"><span data-stu-id="b36c3-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="b36c3-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b36c3-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="b36c3-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b36c3-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="b36c3-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b36c3-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="b36c3-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b36c3-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="b36c3-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b36c3-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="b36c3-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b36c3-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="b36c3-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b36c3-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
