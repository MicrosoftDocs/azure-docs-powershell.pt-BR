---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425778"
---
# <span data-ttu-id="a3283-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a3283-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="a3283-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3283-102">SYNOPSIS</span></span>
<span data-ttu-id="a3283-103">Adiciona uma conta autenticada para usar nas solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a3283-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="a3283-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3283-104">SYNTAX</span></span>

### <span data-ttu-id="a3283-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3283-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3283-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3283-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3283-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3283-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3283-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3283-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3283-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3283-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3283-113">DESCRIPTION</span></span>
<span data-ttu-id="a3283-114">O cmdlet Add-AzureRmAcccount adiciona uma conta autenticada do Azure para usar para solicitações do cmdlet do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a3283-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="a3283-115">Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a3283-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="a3283-116">Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzureAccount ou o cmdlet Import-AzurePublishSettingsFile.</span><span class="sxs-lookup"><span data-stu-id="a3283-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="a3283-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3283-117">EXAMPLES</span></span>

### <span data-ttu-id="a3283-118">Exemplo 1: adicionar uma conta que exija logon interativo</span><span class="sxs-lookup"><span data-stu-id="a3283-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a3283-119">Esse comando adiciona uma conta do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a3283-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="a3283-120">Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.</span><span class="sxs-lookup"><span data-stu-id="a3283-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="a3283-121">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3283-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="a3283-122">Exemplo 2: adicionar uma conta que autentica com as credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="a3283-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a3283-123">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="a3283-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="a3283-124">O segundo comando adiciona uma conta do Azure Resource Manager com as credenciais em $Credential.</span><span class="sxs-lookup"><span data-stu-id="a3283-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="a3283-125">Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="a3283-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="a3283-126">Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.</span><span class="sxs-lookup"><span data-stu-id="a3283-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="a3283-127">Exemplo 3: adicionar uma conta que seja autenticada com as credenciais de entidade de segurança do serviço</span><span class="sxs-lookup"><span data-stu-id="a3283-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a3283-128">O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="a3283-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="a3283-129">O segundo comando adiciona uma conta do Azure Resource Manager com as credenciais armazenadas em $Credential para o locatário especificado.</span><span class="sxs-lookup"><span data-stu-id="a3283-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="a3283-130">O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3283-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="a3283-131">Exemplo 4: adicionar uma conta para um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="a3283-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a3283-132">Esse comando adiciona uma conta do Azure Resource Manager para executar cmdlets para o locatário e a assinatura especificados por padrão.</span><span class="sxs-lookup"><span data-stu-id="a3283-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="a3283-133">OS</span><span class="sxs-lookup"><span data-stu-id="a3283-133">PARAMETERS</span></span>

### <span data-ttu-id="a3283-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="a3283-134">-AccessToken</span></span>
<span data-ttu-id="a3283-135">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="a3283-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="a3283-136">-AccountId</span></span>
<span data-ttu-id="a3283-137">ID da conta para token de acesso</span><span class="sxs-lookup"><span data-stu-id="a3283-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a3283-138">-ApplicationId</span></span>
<span data-ttu-id="a3283-139">SPN</span><span class="sxs-lookup"><span data-stu-id="a3283-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a3283-140">-CertificateThumbprint</span></span>
<span data-ttu-id="a3283-141">Hash do certificado (impressão digital)</span><span class="sxs-lookup"><span data-stu-id="a3283-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-142">-Credential</span><span class="sxs-lookup"><span data-stu-id="a3283-142">-Credential</span></span>
<span data-ttu-id="a3283-143">Especifica um objeto PSCredential.</span><span class="sxs-lookup"><span data-stu-id="a3283-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="a3283-144">Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="a3283-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="a3283-145">O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="a3283-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-146">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="a3283-146">-Environment</span></span>
<span data-ttu-id="a3283-147">Ambiente que contém a conta para a qual entrar</span><span class="sxs-lookup"><span data-stu-id="a3283-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="a3283-148">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="a3283-148">-ServicePrincipal</span></span>
<span data-ttu-id="a3283-149">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3283-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3283-150">-SubscriptionId</span></span>
<span data-ttu-id="a3283-151">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a3283-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="a3283-152">Se você não especificar esse parâmetro, a primeira assinatura da lista de assinaturas será usada.</span><span class="sxs-lookup"><span data-stu-id="a3283-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-153">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="a3283-153">-SubscriptionName</span></span>
<span data-ttu-id="a3283-154">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="a3283-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-155">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="a3283-155">-TenantId</span></span>
<span data-ttu-id="a3283-156">Nome ou ID do locatário opcional</span><span class="sxs-lookup"><span data-stu-id="a3283-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3283-157">-Confirm</span></span>
<span data-ttu-id="a3283-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3283-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3283-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3283-159">-WhatIf</span></span>
<span data-ttu-id="a3283-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3283-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3283-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3283-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3283-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3283-162">CommonParameters</span></span>
<span data-ttu-id="a3283-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3283-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3283-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3283-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3283-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3283-165">INPUTS</span></span>

## <span data-ttu-id="a3283-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3283-166">OUTPUTS</span></span>

### <span data-ttu-id="a3283-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-167">PSAzureProfile</span></span>

## <span data-ttu-id="a3283-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3283-168">NOTES</span></span>

## <span data-ttu-id="a3283-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3283-169">RELATED LINKS</span></span>

