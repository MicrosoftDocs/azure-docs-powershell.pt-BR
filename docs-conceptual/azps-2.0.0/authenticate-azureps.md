---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 897bc20721305c03a0545bc236fa91292861ef1e
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048573"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="86cdc-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="86cdc-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="86cdc-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="86cdc-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="86cdc-105">A maneira mais fácil de começar é com o [Azure Cloud Shell](/azure/cloud-shell/overview) que conecta você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="86cdc-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="86cdc-106">Em uma instalação local, você pode entrar interativamente com seu navegador.</span><span class="sxs-lookup"><span data-stu-id="86cdc-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="86cdc-107">Ao escrever scripts para automação, a abordagem recomendada é usar uma [entidade de serviço](create-azure-service-principal-azureps.md) com as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="86cdc-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="86cdc-108">Ao restringir as permissões de logon o máximo possível para seu caso de uso, você ajuda a proteger os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="86cdc-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="86cdc-109">Após a conexão, os comandos são executados em sua assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="86cdc-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="86cdc-110">Para mudar sua assinatura ativa para uma sessão, use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="86cdc-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="86cdc-111">Para mudar a assinatura padrão usada ao fazer logon no Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="86cdc-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="86cdc-112">Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.</span><span class="sxs-lookup"><span data-stu-id="86cdc-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="86cdc-113">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="86cdc-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="86cdc-114">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="86cdc-114">Sign in interactively</span></span>

<span data-ttu-id="86cdc-115">Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="86cdc-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="86cdc-116">Quando executado, esse cmdlet apresentará uma cadeia de caracteres de token.</span><span class="sxs-lookup"><span data-stu-id="86cdc-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="86cdc-117">Para fazer logon, copie essa cadeia de caracteres e cole-a em https://microsoft.com/devicelogin no navegador.</span><span class="sxs-lookup"><span data-stu-id="86cdc-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="86cdc-118">Sua sessão do PowerShell será autenticada para conectar o Azure.</span><span class="sxs-lookup"><span data-stu-id="86cdc-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="86cdc-119">A autorização da credencial de nome de usuário/senha foi removida no Azure PowerShell devido a alterações nas implementações de autorização do Active Directory e questões de segurança.</span><span class="sxs-lookup"><span data-stu-id="86cdc-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="86cdc-120">Caso você use autorização de credenciais para fins de automação, em vez disso, [crie uma entidade de serviço](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="86cdc-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="86cdc-121">Entrar com uma entidade de serviço <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="86cdc-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="86cdc-122">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="86cdc-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="86cdc-123">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="86cdc-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="86cdc-124">Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.</span><span class="sxs-lookup"><span data-stu-id="86cdc-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="86cdc-125">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="86cdc-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="86cdc-126">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="86cdc-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="86cdc-127">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="86cdc-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="86cdc-128">A forma como você entra com uma entidade de serviço dependerá de se ela está configurada para autenticação baseada em certificado ou em senha.</span><span class="sxs-lookup"><span data-stu-id="86cdc-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="86cdc-129">Autenticação baseada em senha</span><span class="sxs-lookup"><span data-stu-id="86cdc-129">Password-based authentication</span></span>

<span data-ttu-id="86cdc-130">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="86cdc-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="86cdc-131">Esse cmdlet apresentará um prompt para nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="86cdc-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="86cdc-132">Use a ID da entidade de serviço para o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="86cdc-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="86cdc-133">Para cenários de automação, você precisa criar as credenciais usando um nome de usuário e uma cadeia de caracteres segura:</span><span class="sxs-lookup"><span data-stu-id="86cdc-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="86cdc-134">Verifique se que você está usando boas práticas de armazenamento de senha ao automatizar as conexões de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="86cdc-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="86cdc-135">Autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="86cdc-135">Certificate-based authentication</span></span>

<span data-ttu-id="86cdc-136">A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="86cdc-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="86cdc-137">No PowerShell 5, o repositório de certificados pode ser gerenciado e inspecionado com o módulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="86cdc-137">In PowerShell 5, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="86cdc-138">No PowerShell 6, o processo é mais complicado.</span><span class="sxs-lookup"><span data-stu-id="86cdc-138">For PowerShell 6, the process is more complicated.</span></span> <span data-ttu-id="86cdc-139">Os scripts a seguir mostram como importar um certificado existente no repositório de certificados acessível pelo PowerShell.</span><span class="sxs-lookup"><span data-stu-id="86cdc-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-5"></a><span data-ttu-id="86cdc-140">Importar um certificado no PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="86cdc-140">Import a certificate in PowerShell 5</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-6"></a><span data-ttu-id="86cdc-141">Importar um certificado no PowerShell 6</span><span class="sxs-lookup"><span data-stu-id="86cdc-141">Import a certificate in PowerShell 6</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="86cdc-142">Entrar usando uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="86cdc-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="86cdc-143">As identidades gerenciadas são um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="86cdc-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="86cdc-144">Elas são entidades de serviço atribuídas aos recursos executados no Azure.</span><span class="sxs-lookup"><span data-stu-id="86cdc-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="86cdc-145">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="86cdc-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="86cdc-146">As identidades gerenciadas só estão disponíveis nos recursos executados em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="86cdc-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="86cdc-147">Para saber mais sobre as identidades gerenciadas dos recursos do Azure, confira [Como usar identidades gerenciadas dos recursos do Azure em uma VM do Azure para adquirir um token de acesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="86cdc-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="86cdc-148">Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)</span><span class="sxs-lookup"><span data-stu-id="86cdc-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="86cdc-149">Se sua conta estiver associada a mais de um locatário, entrar requer o uso do parâmetro `-TenantId` na conexão.</span><span class="sxs-lookup"><span data-stu-id="86cdc-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="86cdc-150">Esse parâmetro funcionará com qualquer outro método de entrada.</span><span class="sxs-lookup"><span data-stu-id="86cdc-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="86cdc-151">Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.</span><span class="sxs-lookup"><span data-stu-id="86cdc-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="86cdc-152">Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), o valor `-TenantId` **deverá** ser uma ID de locatário.</span><span class="sxs-lookup"><span data-stu-id="86cdc-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="86cdc-153">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="86cdc-153">Sign in to another Cloud</span></span>

<span data-ttu-id="86cdc-154">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="86cdc-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="86cdc-155">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="86cdc-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="86cdc-156">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="86cdc-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="86cdc-157">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="86cdc-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```