---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775274"
---
# <span data-ttu-id="04eea-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="04eea-101">Connect-AzAccount</span></span>

## <span data-ttu-id="04eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04eea-102">SYNOPSIS</span></span>
<span data-ttu-id="04eea-103">Conecte-se ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="04eea-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="04eea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04eea-104">SYNTAX</span></span>

### <span data-ttu-id="04eea-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="04eea-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04eea-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04eea-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04eea-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="04eea-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04eea-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04eea-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04eea-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04eea-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04eea-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="04eea-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04eea-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04eea-111">DESCRIPTION</span></span>
<span data-ttu-id="04eea-112">O cmdlet Connect-AzAccount se conecta ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="04eea-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="04eea-113">Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="04eea-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="04eea-114">Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzAccount ou o cmdlet Import-AzPublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="04eea-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="04eea-115">Se nenhum contexto for encontrado para o usuário atual, esse comando preencherá a lista de contexto do usuário com um contexto para cada uma de suas (primeiras 25) assinaturas.</span><span class="sxs-lookup"><span data-stu-id="04eea-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="04eea-116">A lista de contextos criados para o usuário pode ser encontrada executando-se "Get-AzContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="04eea-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="04eea-117">Para ignorar essa população de contexto, você pode executar esse comando com o parâmetro de opção "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="04eea-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="04eea-118">Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando Disconnect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="04eea-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="04eea-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04eea-119">EXAMPLES</span></span>

### <span data-ttu-id="04eea-120">Exemplo 1: usar um logon interativo para se conectar a uma conta do Azure</span><span class="sxs-lookup"><span data-stu-id="04eea-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-121">Este comando se conecta a uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="04eea-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="04eea-122">Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.</span><span class="sxs-lookup"><span data-stu-id="04eea-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="04eea-123">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="04eea-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="04eea-124">Exemplo 2: (somente Windows PowerShell 5,1) conectar-se a uma conta do Azure usando credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="04eea-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-125">Esse cenário funciona somente no Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="04eea-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="04eea-126">O primeiro comando solicitará as credenciais do usuário (nome de usuário e senha) e as armazenará na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="04eea-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="04eea-127">O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="04eea-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="04eea-128">Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="04eea-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="04eea-129">Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.</span><span class="sxs-lookup"><span data-stu-id="04eea-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="04eea-130">Exemplo 3: conectar-se a uma conta da entidade de serviço do Azure</span><span class="sxs-lookup"><span data-stu-id="04eea-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-131">O primeiro comando obtém as credenciais de entidade de serviço (ID do aplicativo e segredo da entidade de serviço) e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="04eea-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="04eea-132">O segundo comando se conecta ao Azure usando as credenciais de entidade de serviço armazenadas em $Credential para o locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="04eea-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="04eea-133">O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="04eea-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="04eea-134">Exemplo 4: usar um logon interativo para se conectar a uma conta para um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="04eea-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-135">Esse comando se conecta a uma conta do Azure e configurado AzureRM PowerShell para executar cmdlets para o locatário e a assinatura especificados por padrão.</span><span class="sxs-lookup"><span data-stu-id="04eea-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="04eea-136">Exemplo 5: adicionar uma conta usando o logon de identidade de serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="04eea-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-137">Esse comando se conecta usando a identidade de serviço gerenciado do ambiente de host (por exemplo, se executado em um VirtualMachine com uma identidade de serviço gerenciado atribuída, isso permitirá que o código seja acessado usando essa identidade atribuída)</span><span class="sxs-lookup"><span data-stu-id="04eea-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="04eea-138">Exemplo 6: adicionar uma conta usando o logon de identidade de serviço gerenciado e o ClientId</span><span class="sxs-lookup"><span data-stu-id="04eea-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-139">Esse comando se conecta usando a identidade de serviço gerenciado de "myUserAssignedIdentity" adicionando a identidade atribuída ao usuário à máquina virtual e, em seguida, conectando usando o ClientId da identidade atribuída ao usuário.</span><span class="sxs-lookup"><span data-stu-id="04eea-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="04eea-140">Mais informações sobre a configuração de identidades gerenciadas podem ser encontradas aqui: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="04eea-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="04eea-141">Exemplo 7: adicionar uma conta usando o logon de identidade de serviço gerenciado e o ClientId</span><span class="sxs-lookup"><span data-stu-id="04eea-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-142">Esse comando se conecta usando a identidade de serviço gerenciado de "myUserAssignedIdentity" adicionando a identidade atribuída ao usuário à máquina virtual e conectando usando a ID da identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="04eea-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="04eea-143">Mais informações sobre a configuração de identidades gerenciadas podem ser encontradas aqui: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="04eea-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="04eea-144">Exemplo 8: adicionar uma conta usando certificados</span><span class="sxs-lookup"><span data-stu-id="04eea-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="04eea-145">Esse comando se conecta a uma conta do Azure que usa a autenticação de entidade de segurança de serviço baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="04eea-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="04eea-146">O serviço de entidade de segurança usado para autenticação deve ter sido criado com o certificado fornecido.</span><span class="sxs-lookup"><span data-stu-id="04eea-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="04eea-147">Exemplo 9: adicionar uma conta usando a autenticação AccessToken</span><span class="sxs-lookup"><span data-stu-id="04eea-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="04eea-148">Esse comando se conecta a uma conta do Azure especificada em "AccountId" usando o AccessToken e o KeyVaultAccessToken fornecidos.</span><span class="sxs-lookup"><span data-stu-id="04eea-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="04eea-149">OS</span><span class="sxs-lookup"><span data-stu-id="04eea-149">PARAMETERS</span></span>

### <span data-ttu-id="04eea-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="04eea-150">-AccessToken</span></span>
<span data-ttu-id="04eea-151">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="04eea-151">Specifies an access token.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="04eea-152">-AccountId</span></span>
<span data-ttu-id="04eea-153">ID da conta do token de acesso no conjunto de parâmetros AccessToken.</span><span class="sxs-lookup"><span data-stu-id="04eea-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="04eea-154">ID da conta do serviço gerenciado no conjunto de parâmetros ManagedService.</span><span class="sxs-lookup"><span data-stu-id="04eea-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="04eea-155">Pode ser uma ID de recurso de serviço gerenciado ou a ID de cliente associada. Para usar a identidade SystemAssigned, deixe este campo em branco.</span><span class="sxs-lookup"><span data-stu-id="04eea-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="04eea-156">-ApplicationId</span></span>
<span data-ttu-id="04eea-157">SPN</span><span class="sxs-lookup"><span data-stu-id="04eea-157">SPN</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="04eea-158">-CertificateThumbprint</span></span>
<span data-ttu-id="04eea-159">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="04eea-159">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-160">-Contextname</span><span class="sxs-lookup"><span data-stu-id="04eea-160">-ContextName</span></span>
<span data-ttu-id="04eea-161">Nome do contexto padrão deste logon.</span><span class="sxs-lookup"><span data-stu-id="04eea-161">Name of the default context from this login.</span></span>  <span data-ttu-id="04eea-162">Você poderá selecionar esse contexto por este nome após o logon.</span><span class="sxs-lookup"><span data-stu-id="04eea-162">You will be able to select this context by this name after login.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-163">-Credential</span><span class="sxs-lookup"><span data-stu-id="04eea-163">-Credential</span></span>
<span data-ttu-id="04eea-164">Especifica um objeto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="04eea-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="04eea-165">Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="04eea-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="04eea-166">O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="04eea-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04eea-167">-DefaultProfile</span></span>
<span data-ttu-id="04eea-168">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04eea-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-169">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="04eea-169">-Environment</span></span>
<span data-ttu-id="04eea-170">Ambiente que contém a conta para a qual entrar</span><span class="sxs-lookup"><span data-stu-id="04eea-170">Environment containing the account to log into</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-171">-Force</span><span class="sxs-lookup"><span data-stu-id="04eea-171">-Force</span></span>
<span data-ttu-id="04eea-172">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="04eea-172">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="04eea-173">-GraphAccessToken</span></span>
<span data-ttu-id="04eea-174">Serviço do AccessToken para Graph</span><span class="sxs-lookup"><span data-stu-id="04eea-174">AccessToken for Graph Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-175">-Identidade</span><span class="sxs-lookup"><span data-stu-id="04eea-175">-Identity</span></span>
<span data-ttu-id="04eea-176">Faça logon usando a identidade de serviço gerenciado no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="04eea-176">Login using managed service identity in the current environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="04eea-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="04eea-178">AccessToken para o serviço de keyvault</span><span class="sxs-lookup"><span data-stu-id="04eea-178">AccessToken for KeyVault Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="04eea-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="04eea-180">Nome do host para logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="04eea-180">Host name for managed service login</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="04eea-181">-ManagedServicePort</span></span>
<span data-ttu-id="04eea-182">Número da porta para o logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="04eea-182">Port number for managed service login</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="04eea-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="04eea-184">Segredo usado para alguns tipos de logon de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="04eea-184">Secret, used for some kinds of managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-185">-Escopo</span><span class="sxs-lookup"><span data-stu-id="04eea-185">-Scope</span></span>
<span data-ttu-id="04eea-186">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="04eea-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-187">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="04eea-187">-ServicePrincipal</span></span>
<span data-ttu-id="04eea-188">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="04eea-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="04eea-189">-SkipContextPopulation</span></span>
<span data-ttu-id="04eea-190">Ignora a população de contexto se não forem encontrados contextos.</span><span class="sxs-lookup"><span data-stu-id="04eea-190">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="04eea-191">-SkipValidation</span></span>
<span data-ttu-id="04eea-192">Ignorar validação para token de acesso</span><span class="sxs-lookup"><span data-stu-id="04eea-192">Skip validation for access token</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-193">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="04eea-193">-Subscription</span></span>
<span data-ttu-id="04eea-194">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="04eea-194">Subscription Name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-195">-Locatário</span><span class="sxs-lookup"><span data-stu-id="04eea-195">-Tenant</span></span>
<span data-ttu-id="04eea-196">Nome ou ID do locatário opcional</span><span class="sxs-lookup"><span data-stu-id="04eea-196">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="04eea-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="04eea-198">Usar a autenticação de código do dispositivo em vez de um controle do navegador</span><span class="sxs-lookup"><span data-stu-id="04eea-198">Use device code authentication instead of a browser control</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-199">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04eea-199">-Confirm</span></span>
<span data-ttu-id="04eea-200">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04eea-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04eea-201">-WhatIf</span></span>
<span data-ttu-id="04eea-202">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04eea-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04eea-203">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04eea-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04eea-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04eea-204">CommonParameters</span></span>
<span data-ttu-id="04eea-205">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04eea-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04eea-206">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04eea-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04eea-207">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04eea-207">INPUTS</span></span>

### <span data-ttu-id="04eea-208">System. String</span><span class="sxs-lookup"><span data-stu-id="04eea-208">System.String</span></span>

## <span data-ttu-id="04eea-209">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04eea-209">OUTPUTS</span></span>

### <span data-ttu-id="04eea-210">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="04eea-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="04eea-211">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04eea-211">NOTES</span></span>

## <span data-ttu-id="04eea-212">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04eea-212">RELATED LINKS</span></span>
