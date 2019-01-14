---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: b5635e291cdc324e66c936aa16c5772507fc78e8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54055669"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ee128-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee128-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ee128-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ee128-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ee128-105">A maneira mais fácil de começar é com o [Azure Cloud Shell](/azure/cloud-shell/overview) que conecta você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ee128-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="ee128-106">Em uma instalação local, você pode entrar interativamente com seu navegador.</span><span class="sxs-lookup"><span data-stu-id="ee128-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="ee128-107">Ao escrever scripts para automação, a abordagem recomendada é usar uma [entidade de serviço](create-azure-service-principal-azureps.md) com as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="ee128-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="ee128-108">Ao restringir as permissões de logon o máximo possível para seu caso de uso, você ajuda a proteger os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee128-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="ee128-109">Após a conexão, os comandos são executados em sua assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="ee128-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="ee128-110">Para mudar sua assinatura ativa para uma sessão, use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="ee128-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="ee128-111">Para mudar a assinatura padrão usada ao fazer logon no Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="ee128-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ee128-112">Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.</span><span class="sxs-lookup"><span data-stu-id="ee128-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="ee128-113">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ee128-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ee128-114">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="ee128-114">Sign in interactively</span></span>

<span data-ttu-id="ee128-115">Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="ee128-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="ee128-116">Quando executado, esse cmdlet apresentará uma cadeia de caracteres de token.</span><span class="sxs-lookup"><span data-stu-id="ee128-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="ee128-117">Para fazer logon, copie essa cadeia de caracteres e cole-a em https://microsoft.com/devicelogin no navegador.</span><span class="sxs-lookup"><span data-stu-id="ee128-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="ee128-118">Sua sessão do PowerShell será autenticada para conectar o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee128-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="ee128-119">Entrar com credenciais</span><span class="sxs-lookup"><span data-stu-id="ee128-119">Sign in with credentials</span></span>

<span data-ttu-id="ee128-120">Você também pode entrar com um objeto `PSCredential` autorizado para conectar-se ao Azure.</span><span class="sxs-lookup"><span data-stu-id="ee128-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="ee128-121">A maneira mais fácil de obter um objeto de credencial é com o cmdlet [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential).</span><span class="sxs-lookup"><span data-stu-id="ee128-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="ee128-122">Quando executado, esse cmdlet solicitará um par de credenciais com o nome de usuário/senha.</span><span class="sxs-lookup"><span data-stu-id="ee128-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="ee128-123">Essa abordagem não funciona com contas da Microsoft ou contas que tenham a autenticação de dois fatores habilitada.</span><span class="sxs-lookup"><span data-stu-id="ee128-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="ee128-124">Entrar com uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ee128-124">Sign in with a service principal</span></span>

<span data-ttu-id="ee128-125">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="ee128-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ee128-126">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee128-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ee128-127">Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.</span><span class="sxs-lookup"><span data-stu-id="ee128-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ee128-128">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ee128-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ee128-129">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="ee128-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="ee128-130">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee128-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ee128-131">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="ee128-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ee128-132">Esse cmdlet apresentará um prompt para a ID de usuário e a senha da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee128-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="ee128-133">Entrar usando uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="ee128-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="ee128-134">As identidades gerenciadas são um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee128-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="ee128-135">Elas são entidades de serviço atribuídas aos recursos executados no Azure.</span><span class="sxs-lookup"><span data-stu-id="ee128-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="ee128-136">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="ee128-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ee128-137">As identidades gerenciadas só estão disponíveis nos recursos executados em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee128-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="ee128-138">Para saber mais sobre as identidades gerenciadas dos recursos do Azure, confira [Como usar identidades gerenciadas dos recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="ee128-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ee128-139">Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)</span><span class="sxs-lookup"><span data-stu-id="ee128-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ee128-140">Se sua conta estiver associada a mais de um locatário, entrar requer o uso do parâmetro `-TenantId` na conexão.</span><span class="sxs-lookup"><span data-stu-id="ee128-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="ee128-141">Esse parâmetro funcionará com qualquer outro método de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee128-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="ee128-142">Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.</span><span class="sxs-lookup"><span data-stu-id="ee128-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="ee128-143">Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), o valor `-TenantId` **deverá** ser uma ID de locatário.</span><span class="sxs-lookup"><span data-stu-id="ee128-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ee128-144">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="ee128-144">Sign in to another Cloud</span></span>

<span data-ttu-id="ee128-145">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="ee128-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="ee128-146">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="ee128-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ee128-147">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="ee128-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ee128-148">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ee128-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```