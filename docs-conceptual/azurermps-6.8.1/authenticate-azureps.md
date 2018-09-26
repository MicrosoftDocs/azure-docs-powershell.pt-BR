---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 137365e9c022d0ca88dcfd3987e856beb2432897
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300962"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="e53ed-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e53ed-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="e53ed-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e53ed-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="e53ed-105">É a maneira mais simples para entrar interativamente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e53ed-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="e53ed-106">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="e53ed-106">Sign in interactively</span></span>

<span data-ttu-id="e53ed-107">Para entrar no modo interativo, use o cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="e53ed-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="e53ed-108">Quando executado, esse cmdlet exibirá uma caixa de diálogo solicitando seu endereço de email e a senha associados à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="e53ed-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="e53ed-109">Essa autenticação dura o tempo da sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e53ed-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e53ed-110">A partir do Azure PowerShell 6.3.0, suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado ao Windows.</span><span class="sxs-lookup"><span data-stu-id="e53ed-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="e53ed-111">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e53ed-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="e53ed-112">Entrar com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="e53ed-112">Sign in with a service principal</span></span>

<span data-ttu-id="e53ed-113">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="e53ed-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="e53ed-114">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e53ed-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="e53ed-115">Ao conceder a uma entidade de serviço somente as permissões necessárias, seus scripts de automação se mantêm protegidos.</span><span class="sxs-lookup"><span data-stu-id="e53ed-115">By granting a service principle only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="e53ed-116">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e53ed-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="e53ed-117">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="e53ed-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="e53ed-118">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e53ed-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="e53ed-119">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="e53ed-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="e53ed-120">Esse cmdlet exibirá uma caixa de diálogo para inserir a ID de usuário da entidade de serviço e a senha.</span><span class="sxs-lookup"><span data-stu-id="e53ed-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="e53ed-121">Entre usando uma Identidade de Serviço Gerenciada do Azure</span><span class="sxs-lookup"><span data-stu-id="e53ed-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="e53ed-122">Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e53ed-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="e53ed-123">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="e53ed-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="e53ed-124">As identidades gerenciadas só estão disponíveis em máquinas virtuais em execução em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="e53ed-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="e53ed-125">Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="e53ed-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="e53ed-126">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="e53ed-126">Sign in to another Cloud</span></span>

<span data-ttu-id="e53ed-127">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com os regulamentos de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="e53ed-127">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="e53ed-128">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="e53ed-128">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="e53ed-129">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="e53ed-129">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="e53ed-130">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="e53ed-130">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="e53ed-131">Saiba mais sobre como gerenciar o acesso baseado em função do Azure</span><span class="sxs-lookup"><span data-stu-id="e53ed-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="e53ed-132">Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).</span><span class="sxs-lookup"><span data-stu-id="e53ed-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="e53ed-133">Cmdlets do Azure PowerShell para gerenciamento de função:</span><span class="sxs-lookup"><span data-stu-id="e53ed-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="e53ed-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e53ed-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="e53ed-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e53ed-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="e53ed-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e53ed-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="e53ed-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e53ed-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="e53ed-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e53ed-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="e53ed-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e53ed-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="e53ed-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e53ed-140">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
