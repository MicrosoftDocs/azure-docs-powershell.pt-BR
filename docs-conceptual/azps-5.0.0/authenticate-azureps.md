---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, entidade de serviço, ou com identidades gerenciadas para recursos do Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753375"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="d22fb-103">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d22fb-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="d22fb-104">O Azure PowerShell dá suporte a vários métodos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d22fb-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="d22fb-105">A maneira mais fácil de começar é com o [Azure Cloud Shell](/azure/cloud-shell/overview) que conecta você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d22fb-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="d22fb-106">Em uma instalação local, você pode entrar interativamente com seu navegador.</span><span class="sxs-lookup"><span data-stu-id="d22fb-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="d22fb-107">Ao escrever scripts para automação, a abordagem recomendada é usar uma [entidade de serviço](create-azure-service-principal-azureps.md) com as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="d22fb-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="d22fb-108">Ao restringir as permissões de logon o máximo possível para seu caso de uso, você ajuda a proteger os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d22fb-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="d22fb-109">Inicialmente, você está conectado à primeira assinatura que o Azure retorna se você tem acesso a mais de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d22fb-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="d22fb-110">Por padrão, os comandos são executados para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="d22fb-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="d22fb-111">Para mudar sua assinatura ativa para uma sessão, use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="d22fb-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="d22fb-112">Para alterar sua assinatura ativa e fazer com que ela persista entre as sessões no mesmo sistema, use o cmdlet [Select-AzContext](/powershell/module/az.accounts/select-azcontext).</span><span class="sxs-lookup"><span data-stu-id="d22fb-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d22fb-113">Suas credenciais são compartilhadas entre várias sessões do PowerShell, desde que você permaneça conectado.</span><span class="sxs-lookup"><span data-stu-id="d22fb-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="d22fb-114">Para obter mais informações, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d22fb-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="d22fb-115">Entrar no modo interativo</span><span class="sxs-lookup"><span data-stu-id="d22fb-115">Sign in interactively</span></span>

<span data-ttu-id="d22fb-116">Para entrar no modo interativo, use o cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="d22fb-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="d22fb-117">Quando executado do PowerShell versão 6 e superior, esse cmdlet apresenta uma cadeia de caracteres de token.</span><span class="sxs-lookup"><span data-stu-id="d22fb-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="d22fb-118">Para entrar, copie essa cadeia de caracteres e cole-a em [microsoft.com/devicelogin](https://microsoft.com/devicelogin) em um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="d22fb-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="d22fb-119">Sua sessão do PowerShell será autenticada para conectar o Azure.</span><span class="sxs-lookup"><span data-stu-id="d22fb-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="d22fb-120">Você pode especificar o parâmetro `UseDeviceAuthentication` para receber uma cadeia de caracteres de token no Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d22fb-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d22fb-121">A autorização da credencial de nome de usuário/senha foi removida no Azure PowerShell devido a alterações nas implementações de autorização do Active Directory e questões de segurança.</span><span class="sxs-lookup"><span data-stu-id="d22fb-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="d22fb-122">Caso você use autorização de credenciais para fins de automação, em vez disso, [crie uma entidade de serviço](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d22fb-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="d22fb-123">Use o cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext) para armazenar a sua ID de locatário em uma variável a ser usada nas próximas duas seções deste artigo.</span><span class="sxs-lookup"><span data-stu-id="d22fb-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="d22fb-124">Entrar com uma entidade de serviço <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="d22fb-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="d22fb-125">Entidades de serviço são contas do Azure não interativas.</span><span class="sxs-lookup"><span data-stu-id="d22fb-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="d22fb-126">Como outras contas de usuário, as suas permissões são gerenciadas com o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d22fb-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="d22fb-127">Ao conceder a uma entidade de serviço somente as permissões necessárias, você manterá os scripts de automação protegidos.</span><span class="sxs-lookup"><span data-stu-id="d22fb-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="d22fb-128">Para saber como criar uma entidade de serviço para usar com o Azure PowerShell, consulte [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d22fb-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="d22fb-129">Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="d22fb-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="d22fb-130">Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d22fb-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="d22fb-131">A forma como você entra com uma entidade de serviço depende de se ela está configurada para autenticação baseada em certificado ou em senha.</span><span class="sxs-lookup"><span data-stu-id="d22fb-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="d22fb-132">Autenticação baseada em senha</span><span class="sxs-lookup"><span data-stu-id="d22fb-132">Password-based authentication</span></span>

<span data-ttu-id="d22fb-133">Crie uma entidade de serviço a ser usada nos exemplos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="d22fb-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="d22fb-134">Para obter mais informações sobre como criar as entidades de serviço, confira [Criar uma entidade de serviço do Azure com o Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="d22fb-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="d22fb-135">Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="d22fb-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="d22fb-136">Esse cmdlet apresenta um prompt para um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="d22fb-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="d22fb-137">Use o `applicationID` da entidade de serviço para o nome de usuário e converta o `secret` em texto sem formatação para a senha.</span><span class="sxs-lookup"><span data-stu-id="d22fb-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="d22fb-138">Para cenários de automação, você precisa criar as credenciais de `applicationId` e `secret` de uma entidade de serviço:</span><span class="sxs-lookup"><span data-stu-id="d22fb-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="d22fb-139">Verifique se que você está usando boas práticas de armazenamento de senha ao automatizar as conexões de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d22fb-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="d22fb-140">Autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="d22fb-140">Certificate-based authentication</span></span>

<span data-ttu-id="d22fb-141">A autenticação baseada em certificado exige que o Azure PowerShell possa recuperar informações de um repositório de certificados local com base em uma impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="d22fb-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="d22fb-142">Ao usar uma entidade de serviço em vez de um aplicativo registrado, adicione o argumento `-ServicePrincipal` e forneça a ID do aplicativo da entidade de serviço como o valor do parâmetro `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="d22fb-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="d22fb-143">No PowerShell 5.1, o repositório de certificados pode ser gerenciado e inspecionado com o módulo [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="d22fb-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="d22fb-144">Para o PowerShell Core 6.x e posterior, o processo é mais complicado.</span><span class="sxs-lookup"><span data-stu-id="d22fb-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="d22fb-145">Os scripts a seguir mostram como importar um certificado existente no repositório de certificados acessível pelo PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d22fb-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="d22fb-146">Importar um certificado no PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d22fb-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="d22fb-147">Importar um certificado no PowerShell Core 6.x e posterior</span><span class="sxs-lookup"><span data-stu-id="d22fb-147">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="d22fb-148">Entrar usando uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="d22fb-148">Sign in using a managed identity</span></span>

<span data-ttu-id="d22fb-149">As identidades gerenciadas são um recurso do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d22fb-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="d22fb-150">Elas são entidades de serviço atribuídas aos recursos executados no Azure.</span><span class="sxs-lookup"><span data-stu-id="d22fb-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="d22fb-151">Você pode usar uma entidade de serviço de identidade gerenciada para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos.</span><span class="sxs-lookup"><span data-stu-id="d22fb-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="d22fb-152">As identidades gerenciadas só estão disponíveis nos recursos executados em uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="d22fb-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="d22fb-153">Esse exemplo se conecta usando a identidade gerenciada do ambiente de host.</span><span class="sxs-lookup"><span data-stu-id="d22fb-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="d22fb-154">Por exemplo, se executado em uma VirtualMachine com uma Identidade de Serviço Gerenciada atribuída, isso permitirá que o código entre usando essa identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="d22fb-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="d22fb-155">Entrar com um locatário diferente do padrão ou como um Provedor de Soluções na Nuvem (CSP)</span><span class="sxs-lookup"><span data-stu-id="d22fb-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="d22fb-156">Se a sua conta está associada a mais de um locatário, é preciso que o parâmetro `-Tenant` seja especificado na conexão para entrar.</span><span class="sxs-lookup"><span data-stu-id="d22fb-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="d22fb-157">Esse parâmetro funciona com qualquer método de conexão.</span><span class="sxs-lookup"><span data-stu-id="d22fb-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="d22fb-158">Ao fazer logon, esse valor de parâmetro pode ser a ID de objeto do Azure do locatário (ID do Locatário) ou o nome de domínio totalmente qualificado do locatário.</span><span class="sxs-lookup"><span data-stu-id="d22fb-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="d22fb-159">Se você for um [Provedor de Soluções na Nuvem (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), o valor `-Tenant`**deverá** ser uma ID de locatário.</span><span class="sxs-lookup"><span data-stu-id="d22fb-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="d22fb-160">Entre em outra Nuvem</span><span class="sxs-lookup"><span data-stu-id="d22fb-160">Sign in to another Cloud</span></span>

<span data-ttu-id="d22fb-161">Os serviços de nuvem do Azure oferecem ambientes que estão em conformidade com as leis de manipulação de dados regionais.</span><span class="sxs-lookup"><span data-stu-id="d22fb-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="d22fb-162">Para contas em uma nuvem regional, configure o ambiente quando você entrar com o argumento `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="d22fb-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="d22fb-163">Esse parâmetro funciona com qualquer método de conexão.</span><span class="sxs-lookup"><span data-stu-id="d22fb-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="d22fb-164">Por exemplo, se sua conta estiver em uma nuvem da China:</span><span class="sxs-lookup"><span data-stu-id="d22fb-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="d22fb-165">O seguinte comando obtém uma lista de ambientes disponíveis:</span><span class="sxs-lookup"><span data-stu-id="d22fb-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
