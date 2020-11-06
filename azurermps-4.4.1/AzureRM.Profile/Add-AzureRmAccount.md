---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440590"
---
# <span data-ttu-id="fc250-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fc250-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="fc250-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc250-102">SYNOPSIS</span></span>
<span data-ttu-id="fc250-103">Adiciona uma conta autenticada para usar nas solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fc250-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc250-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc250-104">SYNTAX</span></span>

### <span data-ttu-id="fc250-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc250-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc250-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc250-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc250-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc250-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc250-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc250-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc250-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc250-109">DESCRIPTION</span></span>
<span data-ttu-id="fc250-110">O cmdlet Add-AzureRmAcccount adiciona uma conta autenticada do Azure para usar para solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fc250-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="fc250-111">Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fc250-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="fc250-112">Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzureAccount ou o cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="fc250-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="fc250-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc250-113">EXAMPLES</span></span>

### <span data-ttu-id="fc250-114">Exemplo 1: adicionar uma conta que exija logon interativo</span><span class="sxs-lookup"><span data-stu-id="fc250-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="fc250-115">Esse comando adiciona uma conta do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fc250-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="fc250-116">Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.</span><span class="sxs-lookup"><span data-stu-id="fc250-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="fc250-117">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc250-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="fc250-118">Exemplo 2: adicionar uma conta que autentica com as credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="fc250-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="fc250-119">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc250-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="fc250-120">O segundo comando adiciona uma conta do Azure Resource Manager com as credenciais em $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc250-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="fc250-121">Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="fc250-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="fc250-122">Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.</span><span class="sxs-lookup"><span data-stu-id="fc250-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="fc250-123">Exemplo 3: adicionar uma conta que seja autenticada com as credenciais de entidade de segurança do serviço</span><span class="sxs-lookup"><span data-stu-id="fc250-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="fc250-124">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc250-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="fc250-125">O segundo comando adiciona uma conta do Azure Resource Manager com as credenciais armazenadas em $Credential para o locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="fc250-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="fc250-126">O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc250-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="fc250-127">Exemplo 4: adicionar uma conta para um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="fc250-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="fc250-128">Esse comando adiciona uma conta do Azure Resource Manager para executar cmdlets para o locatário e a assinatura especificados por padrão.</span><span class="sxs-lookup"><span data-stu-id="fc250-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="fc250-129">OS</span><span class="sxs-lookup"><span data-stu-id="fc250-129">PARAMETERS</span></span>

### <span data-ttu-id="fc250-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="fc250-130">-AccessToken</span></span>
<span data-ttu-id="fc250-131">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="fc250-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="fc250-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="fc250-132">-AccountId</span></span>
<span data-ttu-id="fc250-133">ID da conta para token de acesso</span><span class="sxs-lookup"><span data-stu-id="fc250-133">Account Id for access token</span></span>

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

### <span data-ttu-id="fc250-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fc250-134">-ApplicationId</span></span>
<span data-ttu-id="fc250-135">SPN</span><span class="sxs-lookup"><span data-stu-id="fc250-135">SPN</span></span>

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

### <span data-ttu-id="fc250-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="fc250-136">-CertificateThumbprint</span></span>
<span data-ttu-id="fc250-137">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="fc250-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="fc250-138">-Contextname</span><span class="sxs-lookup"><span data-stu-id="fc250-138">-ContextName</span></span>
<span data-ttu-id="fc250-139">Nome do contexto padrão deste logon.</span><span class="sxs-lookup"><span data-stu-id="fc250-139">Name of the default context from this login.</span></span>  <span data-ttu-id="fc250-140">Você poderá selecionar esse contexto por este nome após o logon.</span><span class="sxs-lookup"><span data-stu-id="fc250-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="fc250-141">-Credential</span><span class="sxs-lookup"><span data-stu-id="fc250-141">-Credential</span></span>
<span data-ttu-id="fc250-142">Especifica um objeto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="fc250-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="fc250-143">Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fc250-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="fc250-144">O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="fc250-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="fc250-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc250-145">-DefaultProfile</span></span>
<span data-ttu-id="fc250-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc250-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc250-147">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="fc250-147">-Environment</span></span>
<span data-ttu-id="fc250-148">Ambiente que contém a conta para a qual entrar</span><span class="sxs-lookup"><span data-stu-id="fc250-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="fc250-149">-Force</span><span class="sxs-lookup"><span data-stu-id="fc250-149">-Force</span></span>
<span data-ttu-id="fc250-150">Substituir o contexto existente com o mesmo nome, se houver.</span><span class="sxs-lookup"><span data-stu-id="fc250-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="fc250-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="fc250-151">-GraphAccessToken</span></span>
<span data-ttu-id="fc250-152">Serviço do AccessToken para Graph</span><span class="sxs-lookup"><span data-stu-id="fc250-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="fc250-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="fc250-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="fc250-154">AccessToken para o serviço de keyvault</span><span class="sxs-lookup"><span data-stu-id="fc250-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="fc250-155">-Escopo</span><span class="sxs-lookup"><span data-stu-id="fc250-155">-Scope</span></span>
<span data-ttu-id="fc250-156">Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="fc250-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="fc250-157">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="fc250-157">-ServicePrincipal</span></span>
<span data-ttu-id="fc250-158">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc250-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc250-159">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="fc250-159">-Subscription</span></span>
<span data-ttu-id="fc250-160">Nome ou ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="fc250-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="fc250-161">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="fc250-161">-TenantId</span></span>
<span data-ttu-id="fc250-162">Nome ou ID do locatário opcional</span><span class="sxs-lookup"><span data-stu-id="fc250-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="fc250-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc250-163">-Confirm</span></span>
<span data-ttu-id="fc250-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc250-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc250-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc250-165">-WhatIf</span></span>
<span data-ttu-id="fc250-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc250-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc250-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc250-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc250-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc250-168">CommonParameters</span></span>
<span data-ttu-id="fc250-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc250-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc250-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc250-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc250-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc250-171">INPUTS</span></span>

### <span data-ttu-id="fc250-172">String</span><span class="sxs-lookup"><span data-stu-id="fc250-172">String</span></span>
<span data-ttu-id="fc250-173">O parâmetro ' SubscriptionId ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fc250-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fc250-174">String</span><span class="sxs-lookup"><span data-stu-id="fc250-174">String</span></span>
<span data-ttu-id="fc250-175">O parâmetro ' Subscriptionname ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fc250-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fc250-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc250-176">OUTPUTS</span></span>

### <span data-ttu-id="fc250-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="fc250-177">PSAzureProfile</span></span>
<span data-ttu-id="fc250-178">Credenciais, assinatura, conta e informações de locatário para o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="fc250-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="fc250-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc250-179">NOTES</span></span>

## <span data-ttu-id="fc250-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc250-180">RELATED LINKS</span></span>

