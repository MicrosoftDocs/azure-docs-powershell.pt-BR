---
title: Fazer logon com o Azure PowerShell
description: Fazer logon com o Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46301098"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="f9e97-103">Fazer logon com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9e97-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="f9e97-104">O Azure PowerShell oferece suporte a vários métodos de logon.</span><span class="sxs-lookup"><span data-stu-id="f9e97-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="f9e97-105">É a maneira mais simples para começar a fazer logon interativamente na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f9e97-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="f9e97-106">Logon Interativo</span><span class="sxs-lookup"><span data-stu-id="f9e97-106">Interactive log in</span></span>

1. <span data-ttu-id="f9e97-107">Digite `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="f9e97-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="f9e97-108">Será exibida a caixa de diálogo solicitando as credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9e97-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="f9e97-109">Digite o endereço de e-mail e a senha associada à sua conta.</span><span class="sxs-lookup"><span data-stu-id="f9e97-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="f9e97-110">O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.</span><span class="sxs-lookup"><span data-stu-id="f9e97-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="f9e97-111">Fazer logon com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f9e97-111">Log in with a service principal</span></span>

<span data-ttu-id="f9e97-112">As entidades de serviço oferecem uma maneira de criar contas não interativas para manipular recursos.</span><span class="sxs-lookup"><span data-stu-id="f9e97-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="f9e97-113">As entidades de serviço são como as contas de usuário às quais você pode aplicar regras usando o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9e97-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="f9e97-114">Ao conceder as permissões mínimas necessárias para uma entidade de serviço, você pode garantir que seus scripts de automação fiquem ainda mais seguros.</span><span class="sxs-lookup"><span data-stu-id="f9e97-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="f9e97-115">Se você ainda não tiver uma entidade de serviço, [crie uma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f9e97-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="f9e97-116">Faça logon com uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9e97-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="f9e97-117">Para obter a TenantId, faça logon interativamente e obtenha a TenantId da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="f9e97-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="f9e97-118">Entrar usando identidades gerenciadas para recursos do Azure</span><span class="sxs-lookup"><span data-stu-id="f9e97-118">Log in using managed identities for Azure resources</span></span>

<span data-ttu-id="f9e97-119">Identidades gerenciadas para recursos do Azure é um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9e97-119">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="f9e97-120">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="f9e97-120">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="f9e97-121">Para saber mais informações sobre identidades gerenciadas para recursos do Azure, consulte [Como usar identidades gerenciadas para recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="f9e97-121">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="f9e97-122">Faça logon em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="f9e97-122">Log in to another Cloud</span></span>

<span data-ttu-id="f9e97-123">Os Serviços de Nuvem do Azure oferecem ambientes diferentes que estão de acordo com as regulamentações de manipulação de dados de diversos governos.</span><span class="sxs-lookup"><span data-stu-id="f9e97-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="f9e97-124">Caso sua conta do Azure esteja em uma das nuvens de governo, será necessário especificar o ambiente ao se conectar.</span><span class="sxs-lookup"><span data-stu-id="f9e97-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="f9e97-125">Por exemplo, se sua conta está na nuvem da China, faça logon usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f9e97-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="f9e97-126">Use o seguinte comando para obter uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="f9e97-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="f9e97-127">Saiba mais sobre como gerenciar o acesso baseado em função do Azure</span><span class="sxs-lookup"><span data-stu-id="f9e97-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="f9e97-128">Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).</span><span class="sxs-lookup"><span data-stu-id="f9e97-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="f9e97-129">Cmdlets do Azure PowerShell para gerenciamento de função</span><span class="sxs-lookup"><span data-stu-id="f9e97-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="f9e97-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f9e97-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="f9e97-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e97-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="f9e97-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f9e97-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="f9e97-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e97-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="f9e97-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f9e97-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="f9e97-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e97-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="f9e97-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9e97-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
