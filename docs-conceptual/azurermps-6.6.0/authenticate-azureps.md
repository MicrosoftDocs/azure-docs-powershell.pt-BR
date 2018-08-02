---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, a entidade de serviço, ou com o MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368136"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="4e1dd-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e1dd-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="4e1dd-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="4e1dd-105">É a maneira mais simples para entrar interativamente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="4e1dd-106">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="4e1dd-106">Sign in interactively</span></span>

<span data-ttu-id="4e1dd-107">Para entrar no modo interativo, use o cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="4e1dd-108">Quando executado, esse cmdlet exibirá uma caixa de diálogo solicitando seu endereço de email e a senha associados à sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="4e1dd-109">Quando você autenticar, essas informações são salvas para a sessão atual do PowerShell, a caixa de diálogo é fechada e você tem acesso a todos os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e1dd-110">A partir do Azure PowerShell 6.3.0, suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado ao Windows.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="4e1dd-111">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="4e1dd-112">Entrar com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="4e1dd-112">Sign in with a service principal</span></span>

<span data-ttu-id="4e1dd-113">As entidades de serviço oferecem uma maneira de criar contas não interativas para manipular recursos.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="4e1dd-114">As entidades de serviço são como as contas de usuário às quais você pode aplicar regras usando o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="4e1dd-115">Ao conceder as permissões mínimas necessárias para uma entidade de serviço, você pode garantir que seus scripts de automação fiquem ainda mais seguros.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="4e1dd-116">Se precisar criar uma entidade de serviço para usar com o Azure PowerShell, confira [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="4e1dd-117">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="4e1dd-118">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="4e1dd-119">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="4e1dd-120">Esse cmdlet exibirá uma caixa de diálogo para inserir a ID de usuário da entidade de serviço e a senha.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="4e1dd-121">Entre usando uma Identidade de Serviço Gerenciada da VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4e1dd-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="4e1dd-122">A Identidade do Serviço Gerenciado (MSI) é a versão prévia de um recurso para o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="4e1dd-123">Você pode usar uma entidade de serviço do MSI para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="4e1dd-124">A MSI só está disponível em máquinas virtuais em execução em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="4e1dd-125">Para obter mais informações sobre o MSI, consulte [Como usar uma Identidade de Serviço Gerenciado (MSI) da VM do Azure para conexão e aquisição de token](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="4e1dd-126">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="4e1dd-126">Sign in to another Cloud</span></span>

<span data-ttu-id="4e1dd-127">Os serviços de nuvem do Azure oferecem ambientes diferentes que estão de acordo com as regulamentações de manipulação de dados de diversas regiões.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="4e1dd-128">Caso sua conta do Azure esteja em uma nuvem associada a uma dessas regiões, será necessário especificar o ambiente ao se conectar.</span><span class="sxs-lookup"><span data-stu-id="4e1dd-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="4e1dd-129">Por exemplo, se sua conta está na nuvem da China, faça logon usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="4e1dd-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="4e1dd-130">Use o seguinte comando para obter uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="4e1dd-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="4e1dd-131">Saiba mais sobre como gerenciar o acesso baseado em função do Azure</span><span class="sxs-lookup"><span data-stu-id="4e1dd-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="4e1dd-132">Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).</span><span class="sxs-lookup"><span data-stu-id="4e1dd-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="4e1dd-133">Cmdlets do Azure PowerShell para gerenciamento de função:</span><span class="sxs-lookup"><span data-stu-id="4e1dd-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="4e1dd-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4e1dd-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="4e1dd-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4e1dd-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="4e1dd-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4e1dd-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="4e1dd-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4e1dd-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="4e1dd-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4e1dd-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="4e1dd-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4e1dd-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="4e1dd-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4e1dd-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
