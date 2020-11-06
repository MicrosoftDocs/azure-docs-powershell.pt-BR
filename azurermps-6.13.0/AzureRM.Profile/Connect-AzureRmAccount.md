---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610543"
---
# <span data-ttu-id="65c64-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="65c64-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="65c64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65c64-102">SYNOPSIS</span></span>
<span data-ttu-id="65c64-103">Conecte-se ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="65c64-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65c64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65c64-104">SYNTAX</span></span>

### <span data-ttu-id="65c64-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="65c64-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65c64-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65c64-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65c64-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65c64-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c64-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65c64-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65c64-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="65c64-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65c64-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65c64-110">DESCRIPTION</span></span>
<span data-ttu-id="65c64-111">O cmdlet Connect-AzureRmAccount se conecta ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="65c64-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="65c64-112">Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="65c64-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="65c64-113">Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzureAccount ou o cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="65c64-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="65c64-114">Se nenhum contexto for encontrado para o usuário atual, esse comando preencherá a lista de contexto do usuário com um contexto para cada uma de suas (primeiras 25) assinaturas.</span><span class="sxs-lookup"><span data-stu-id="65c64-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="65c64-115">A lista de contextos criados para o usuário pode ser encontrada executando-se "Get-AzureRmContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="65c64-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="65c64-116">Para ignorar essa população de contexto, você pode executar esse comando com o parâmetro de opção "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="65c64-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="65c64-117">Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="65c64-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="65c64-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65c64-118">EXAMPLES</span></span>

### <span data-ttu-id="65c64-119">Exemplo 1: usar um logon interativo para se conectar a uma conta do Azure</span><span class="sxs-lookup"><span data-stu-id="65c64-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="65c64-120">Este comando se conecta a uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="65c64-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="65c64-121">Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.</span><span class="sxs-lookup"><span data-stu-id="65c64-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="65c64-122">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="65c64-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="65c64-123">Exemplo 2: conectar-se a uma conta do Azure usando credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="65c64-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="65c64-124">O primeiro comando solicitará as credenciais do usuário (nome de usuário e senha) e as armazenará na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="65c64-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="65c64-125">O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="65c64-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="65c64-126">Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="65c64-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="65c64-127">Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.</span><span class="sxs-lookup"><span data-stu-id="65c64-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="65c64-128">Exemplo 3: conectar-se a uma conta da entidade de serviço do Azure</span><span class="sxs-lookup"><span data-stu-id="65c64-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="65c64-129">O primeiro comando obtém as credenciais de entidade de serviço (ID do aplicativo e segredo da entidade de serviço) e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="65c64-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="65c64-130">O segundo comando se conecta ao Azure usando as credenciais de entidade de serviço armazenadas em $Credential para o locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="65c64-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="65c64-131">O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="65c64-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="65c64-132">Exemplo 4: usar um logon interativo para se conectar a uma conta para um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="65c64-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="65c64-133">Esse comando se conecta a uma conta do Azure e configurado AzureRM PowerShell para executar cmdlets para o locatário e a assinatura especificados por padrão.</span><span class="sxs-lookup"><span data-stu-id="65c64-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="65c64-134">Exemplo 5: adicionar uma conta usando o logon de identidade de serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="65c64-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="65c64-135">Esse comando se conecta usando a identidade de serviço gerenciado do ambiente de host (por exemplo, se executado em um VirtualMachine com uma identidade de serviço gerenciado atribuída, isso permitirá que o código seja acessado usando essa identidade atribuída)</span><span class="sxs-lookup"><span data-stu-id="65c64-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="65c64-136">Exemplo 6: adicionar uma conta usando certificados</span><span class="sxs-lookup"><span data-stu-id="65c64-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="65c64-137">Esse comando se conecta a uma conta do Azure que usa a autenticação de entidade de segurança de serviço baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="65c64-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="65c64-138">A entidade de serviço usada para autenticação deve ter sido criada com o certificado fornecido.</span><span class="sxs-lookup"><span data-stu-id="65c64-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="65c64-139">OS</span><span class="sxs-lookup"><span data-stu-id="65c64-139">PARAMETERS</span></span>

### <span data-ttu-id="65c64-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="65c64-140">-AccessToken</span></span>
<span data-ttu-id="65c64-141">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="65c64-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="65c64-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="65c64-142">-AccountId</span></span>
<span data-ttu-id="65c64-143">ID da conta para token de acesso</span><span class="sxs-lookup"><span data-stu-id="65c64-143">Account Id for access token</span></span>

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

### <span data-ttu-id="65c64-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="65c64-144">-ApplicationId</span></span>
<span data-ttu-id="65c64-145">SPN</span><span class="sxs-lookup"><span data-stu-id="65c64-145">SPN</span></span>

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

### <span data-ttu-id="65c64-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="65c64-146">-CertificateThumbprint</span></span>
<span data-ttu-id="65c64-147">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="65c64-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="65c64-148">-Contextname</span><span class="sxs-lookup"><span data-stu-id="65c64-148">-ContextName</span></span>
<span data-ttu-id="65c64-149">Nome do contexto padrão deste logon.</span><span class="sxs-lookup"><span data-stu-id="65c64-149">Name of the default context from this login.</span></span>  <span data-ttu-id="65c64-150">Você poderá selecionar esse contexto por este nome após o logon.</span><span class="sxs-lookup"><span data-stu-id="65c64-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="65c64-151">-Credential</span><span class="sxs-lookup"><span data-stu-id="65c64-151">-Credential</span></span>
<span data-ttu-id="65c64-152">Especifica um objeto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="65c64-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="65c64-153">Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="65c64-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="65c64-154">O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="65c64-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c64-155">-DefaultProfile</span></span>
<span data-ttu-id="65c64-156">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65c64-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-157">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="65c64-157">-Environment</span></span>
<span data-ttu-id="65c64-158">Ambiente que contém a conta para a qual entrar</span><span class="sxs-lookup"><span data-stu-id="65c64-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="65c64-159">-Force</span><span class="sxs-lookup"><span data-stu-id="65c64-159">-Force</span></span>
<span data-ttu-id="65c64-160">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="65c64-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="65c64-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="65c64-161">-GraphAccessToken</span></span>
<span data-ttu-id="65c64-162">Serviço do AccessToken para Graph</span><span class="sxs-lookup"><span data-stu-id="65c64-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="65c64-163">-Identidade</span><span class="sxs-lookup"><span data-stu-id="65c64-163">-Identity</span></span>
<span data-ttu-id="65c64-164">Faça logon usando a identidade de serviço gerenciado no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="65c64-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="65c64-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="65c64-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="65c64-166">AccessToken para o serviço de keyvault</span><span class="sxs-lookup"><span data-stu-id="65c64-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="65c64-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="65c64-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="65c64-168">Nome do host para logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="65c64-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="65c64-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="65c64-169">-ManagedServicePort</span></span>
<span data-ttu-id="65c64-170">Número da porta para o logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="65c64-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="65c64-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="65c64-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="65c64-172">Segredo usado para alguns tipos de logon de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="65c64-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="65c64-173">-Escopo</span><span class="sxs-lookup"><span data-stu-id="65c64-173">-Scope</span></span>
<span data-ttu-id="65c64-174">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="65c64-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="65c64-175">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="65c64-175">-ServicePrincipal</span></span>
<span data-ttu-id="65c64-176">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="65c64-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="65c64-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="65c64-177">-SkipContextPopulation</span></span>
<span data-ttu-id="65c64-178">Ignora a população de contexto se não forem encontrados contextos.</span><span class="sxs-lookup"><span data-stu-id="65c64-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="65c64-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="65c64-179">-SkipValidation</span></span>
<span data-ttu-id="65c64-180">Ignorar validação para token de acesso</span><span class="sxs-lookup"><span data-stu-id="65c64-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="65c64-181">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="65c64-181">-Subscription</span></span>
<span data-ttu-id="65c64-182">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="65c64-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="65c64-183">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="65c64-183">-TenantId</span></span>
<span data-ttu-id="65c64-184">Nome de domínio opcional ou ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="65c64-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="65c64-185">O nome de domínio não funcionará em todas as situações de entrada.</span><span class="sxs-lookup"><span data-stu-id="65c64-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="65c64-186">Para o logon no provedor de soluções de nuvem (CSP), a ID do locatário é necessária.</span><span class="sxs-lookup"><span data-stu-id="65c64-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-187">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65c64-187">-Confirm</span></span>
<span data-ttu-id="65c64-188">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65c64-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c64-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c64-189">-WhatIf</span></span>
<span data-ttu-id="65c64-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65c64-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65c64-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65c64-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c64-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c64-192">CommonParameters</span></span>
<span data-ttu-id="65c64-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c64-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c64-194">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c64-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c64-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65c64-195">INPUTS</span></span>

### <span data-ttu-id="65c64-196">System. String</span><span class="sxs-lookup"><span data-stu-id="65c64-196">System.String</span></span>
<span data-ttu-id="65c64-197">Parâmetros: Subscription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65c64-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="65c64-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65c64-198">OUTPUTS</span></span>

### <span data-ttu-id="65c64-199">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="65c64-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="65c64-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65c64-200">NOTES</span></span>

## <span data-ttu-id="65c64-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65c64-201">RELATED LINKS</span></span>
