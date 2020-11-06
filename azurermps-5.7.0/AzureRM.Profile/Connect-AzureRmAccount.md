---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426660"
---
# <span data-ttu-id="2945e-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="2945e-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="2945e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2945e-102">SYNOPSIS</span></span>
<span data-ttu-id="2945e-103">Conecte-se ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2945e-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2945e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2945e-104">SYNTAX</span></span>

### <span data-ttu-id="2945e-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="2945e-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2945e-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2945e-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2945e-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2945e-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2945e-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2945e-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2945e-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="2945e-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2945e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2945e-110">DESCRIPTION</span></span>
<span data-ttu-id="2945e-111">O cmdlet Connect-AzureRmAccount se conecta ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2945e-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="2945e-112">Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2945e-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="2945e-113">Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzureAccount ou o cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="2945e-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="2945e-114">Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando Disconnect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="2945e-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="2945e-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2945e-115">EXAMPLES</span></span>

### <span data-ttu-id="2945e-116">Exemplo 1: usar um logon interativo para se conectar a uma conta do Azure</span><span class="sxs-lookup"><span data-stu-id="2945e-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2945e-117">Este comando se conecta a uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="2945e-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="2945e-118">Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.</span><span class="sxs-lookup"><span data-stu-id="2945e-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="2945e-119">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2945e-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="2945e-120">Exemplo 2: conectar-se a uma conta do Azure usando credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="2945e-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2945e-121">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="2945e-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="2945e-122">O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="2945e-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="2945e-123">Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="2945e-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="2945e-124">Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.</span><span class="sxs-lookup"><span data-stu-id="2945e-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="2945e-125">Exemplo 3: conectar-se a uma conta da entidade de serviço do Azure</span><span class="sxs-lookup"><span data-stu-id="2945e-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2945e-126">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="2945e-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="2945e-127">O segundo comando se conecta ao Azure usando as credenciais de entidade de serviço armazenadas em $Credential para o locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="2945e-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="2945e-128">O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2945e-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="2945e-129">Exemplo 4: usar um logon interativo para se conectar a uma conta para um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="2945e-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2945e-130">Esse comando se conecta a uma conta do Azure e configurado AzureRM PowerShell para executar cmdlets para o locatário e a assinatura especificados por padrão.</span><span class="sxs-lookup"><span data-stu-id="2945e-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="2945e-131">Exemplo 5: adicionar uma conta usando o logon de identidade de serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="2945e-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2945e-132">Esse comando conecta-se usando a identidade de serviço gerenciado do ambiente de host (por exemplo, se executado em um VirtualMachine com uma identidade de serviço gerenciado atribuída, isso permitirá que o código seja acessado usando essa identidade atribuída)</span><span class="sxs-lookup"><span data-stu-id="2945e-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="2945e-133">OS</span><span class="sxs-lookup"><span data-stu-id="2945e-133">PARAMETERS</span></span>

### <span data-ttu-id="2945e-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2945e-134">-AccessToken</span></span>
<span data-ttu-id="2945e-135">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="2945e-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2945e-136">-AccountId</span></span>
<span data-ttu-id="2945e-137">ID da conta para token de acesso</span><span class="sxs-lookup"><span data-stu-id="2945e-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2945e-138">-ApplicationId</span></span>
<span data-ttu-id="2945e-139">SPN</span><span class="sxs-lookup"><span data-stu-id="2945e-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2945e-140">-CertificateThumbprint</span></span>
<span data-ttu-id="2945e-141">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="2945e-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-142">-Contextname</span><span class="sxs-lookup"><span data-stu-id="2945e-142">-ContextName</span></span>
<span data-ttu-id="2945e-143">Nome do contexto padrão deste logon.</span><span class="sxs-lookup"><span data-stu-id="2945e-143">Name of the default context from this login.</span></span>  <span data-ttu-id="2945e-144">Você poderá selecionar esse contexto por este nome após o logon.</span><span class="sxs-lookup"><span data-stu-id="2945e-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-145">-Credential</span><span class="sxs-lookup"><span data-stu-id="2945e-145">-Credential</span></span>
<span data-ttu-id="2945e-146">Especifica um objeto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="2945e-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="2945e-147">Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="2945e-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="2945e-148">O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="2945e-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2945e-149">-DefaultProfile</span></span>
<span data-ttu-id="2945e-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2945e-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-151">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="2945e-151">-Environment</span></span>
<span data-ttu-id="2945e-152">Ambiente que contém a conta para a qual entrar</span><span class="sxs-lookup"><span data-stu-id="2945e-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-153">-Force</span><span class="sxs-lookup"><span data-stu-id="2945e-153">-Force</span></span>
<span data-ttu-id="2945e-154">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="2945e-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="2945e-155">-GraphAccessToken</span></span>
<span data-ttu-id="2945e-156">Serviço do AccessToken para Graph</span><span class="sxs-lookup"><span data-stu-id="2945e-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-157">-Identidade</span><span class="sxs-lookup"><span data-stu-id="2945e-157">-Identity</span></span>
<span data-ttu-id="2945e-158">Faça logon usando a identidade de serviço gerenciado no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="2945e-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="2945e-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="2945e-160">AccessToken para o serviço de keyvault</span><span class="sxs-lookup"><span data-stu-id="2945e-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="2945e-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="2945e-162">Nome do host para logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="2945e-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="2945e-163">-ManagedServicePort</span></span>
<span data-ttu-id="2945e-164">Número da porta para o logon no serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="2945e-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-165">-Escopo</span><span class="sxs-lookup"><span data-stu-id="2945e-165">-Scope</span></span>
<span data-ttu-id="2945e-166">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="2945e-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-167">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="2945e-167">-ServicePrincipal</span></span>
<span data-ttu-id="2945e-168">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2945e-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="2945e-169">-SkipValidation</span></span>
<span data-ttu-id="2945e-170">Ignorar validação para token de acesso</span><span class="sxs-lookup"><span data-stu-id="2945e-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-171">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="2945e-171">-Subscription</span></span>
<span data-ttu-id="2945e-172">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="2945e-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-173">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="2945e-173">-TenantId</span></span>
<span data-ttu-id="2945e-174">Nome ou ID do locatário opcional</span><span class="sxs-lookup"><span data-stu-id="2945e-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2945e-175">-Confirm</span></span>
<span data-ttu-id="2945e-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2945e-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2945e-177">-WhatIf</span></span>
<span data-ttu-id="2945e-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2945e-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2945e-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2945e-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2945e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2945e-180">CommonParameters</span></span>
<span data-ttu-id="2945e-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2945e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2945e-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2945e-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2945e-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2945e-183">INPUTS</span></span>

### <span data-ttu-id="2945e-184">String</span><span class="sxs-lookup"><span data-stu-id="2945e-184">String</span></span>
<span data-ttu-id="2945e-185">O parâmetro ' SubscriptionId ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2945e-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2945e-186">String</span><span class="sxs-lookup"><span data-stu-id="2945e-186">String</span></span>
<span data-ttu-id="2945e-187">O parâmetro ' Subscriptionname ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2945e-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2945e-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2945e-188">OUTPUTS</span></span>

### <span data-ttu-id="2945e-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="2945e-189">PSAzureProfile</span></span>
<span data-ttu-id="2945e-190">Credenciais, assinatura, conta e informações de locatário para o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="2945e-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="2945e-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2945e-191">NOTES</span></span>

## <span data-ttu-id="2945e-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2945e-192">RELATED LINKS</span></span>

