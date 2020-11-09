---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 039ae434a28da0b8f320925c4e84c57571a74273
ms.sourcegitcommit: e30c11217b1ac93493fdd509fa71ac33510a98b5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/29/2020
ms.locfileid: "94284378"
---
# <span data-ttu-id="cf96c-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cf96c-101">Connect-AzAccount</span></span>

## <span data-ttu-id="cf96c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf96c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf96c-103">Conecte-se ao Azure com uma conta autenticada para uso com cmdlets dos módulos AZ PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf96c-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="cf96c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf96c-104">SYNTAX</span></span>

### <span data-ttu-id="cf96c-105">UserWithSubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf96c-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf96c-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf96c-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf96c-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="cf96c-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf96c-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf96c-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf96c-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf96c-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf96c-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="cf96c-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf96c-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf96c-111">DESCRIPTION</span></span>

<span data-ttu-id="cf96c-112">O `Connect-AzAccount` cmdlet se conecta ao Azure com uma conta autenticada para uso com cmdlets dos módulos AZ PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf96c-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="cf96c-113">Você pode usar essa conta autenticada somente com as solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="cf96c-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="cf96c-114">Para adicionar uma conta autenticada para uso com gerenciamento de serviço, use o `Add-AzureAccount` cmdlet do módulo do PowerShell do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf96c-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="cf96c-115">Se não for encontrado contexto para o usuário atual, a lista de contexto do usuário será preenchida com um contexto para cada uma das 25 primeiras assinaturas.</span><span class="sxs-lookup"><span data-stu-id="cf96c-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="cf96c-116">A lista de contextos criados para o usuário pode ser encontrada em execução `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="cf96c-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="cf96c-117">Para ignorar essa população de contexto, especifique o parâmetro de opção **SkipContextPopulation** .</span><span class="sxs-lookup"><span data-stu-id="cf96c-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="cf96c-118">Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="cf96c-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="cf96c-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf96c-119">EXAMPLES</span></span>

### <span data-ttu-id="cf96c-120">Exemplo 1: conectar-se a uma conta do Azure</span><span class="sxs-lookup"><span data-stu-id="cf96c-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="cf96c-121">Este exemplo se conecta a uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf96c-121">This example connects to an Azure account.</span></span> <span data-ttu-id="cf96c-122">Você deve fornecer uma conta da Microsoft ou credenciais de ID organizacional.</span><span class="sxs-lookup"><span data-stu-id="cf96c-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="cf96c-123">Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf96c-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-124">Exemplo 2: (somente Windows PowerShell 5,1) conectar ao Azure usando credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="cf96c-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="cf96c-125">Esse cenário funciona somente no Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="cf96c-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="cf96c-126">O primeiro comando solicita as credenciais do usuário e as armazena na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="cf96c-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="cf96c-127">O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="cf96c-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="cf96c-128">Esta conta é autenticada com o Azure usando credenciais de ID da organização.</span><span class="sxs-lookup"><span data-stu-id="cf96c-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-129">Exemplo 3: conectar-se ao Azure usando uma conta da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="cf96c-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="cf96c-130">O primeiro comando solicita as credenciais do serviço principal e as armazena na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="cf96c-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="cf96c-131">Insira sua ID de aplicativo para o nome de usuário e o segredo da entidade de serviço como a senha quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="cf96c-132">O segundo comando conecta o locatário do Azure especificado usando as credenciais de entidade de serviço armazenadas na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="cf96c-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="cf96c-133">O parâmetro de comutação **UserPrincipal** indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf96c-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-134">Exemplo 4: usar um login interativo para se conectar a um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="cf96c-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="cf96c-135">Este exemplo se conecta a uma conta do Azure com o locatário e a assinatura especificados.</span><span class="sxs-lookup"><span data-stu-id="cf96c-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-136">Exemplo 5: conectar usando uma identidade de serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="cf96c-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="cf96c-137">Este exemplo se conecta usando o MSI (identidade de serviço gerenciado) do ambiente do host.</span><span class="sxs-lookup"><span data-stu-id="cf96c-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="cf96c-138">Por exemplo, você entra no Azure a partir de uma máquina virtual com um MSI atribuído.</span><span class="sxs-lookup"><span data-stu-id="cf96c-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-139">Exemplo 6: conectar usando a identidade de serviço gerenciado login e ClientId</span><span class="sxs-lookup"><span data-stu-id="cf96c-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="cf96c-140">Este exemplo se conecta usando a identidade de serviço gerenciado do **myUserAssignedIdentity**.</span><span class="sxs-lookup"><span data-stu-id="cf96c-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="cf96c-141">Ele adiciona a identidade atribuída ao usuário à máquina virtual e, em seguida, se conecta usando o ClientId da identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cf96c-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="cf96c-142">Para obter mais informações, consulte [Configurar identidades gerenciadas dos recursos do Azure em uma VM do Azure](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span><span class="sxs-lookup"><span data-stu-id="cf96c-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="cf96c-143">Exemplo 7: conectar usando certificados</span><span class="sxs-lookup"><span data-stu-id="cf96c-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="cf96c-144">Este exemplo se conecta a uma conta do Azure que usa a autenticação de entidade de segurança de serviço baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="cf96c-145">A entidade de segurança de serviço usada para autenticação deve ser criada com o certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="cf96c-146">Para obter mais informações sobre como criar certificados auto-assinados e atribuir permissões a ele, consulte usar o [PowerShell do Azure para criar uma entidade de serviço com um certificado](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="cf96c-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="cf96c-147">OS</span><span class="sxs-lookup"><span data-stu-id="cf96c-147">PARAMETERS</span></span>

### <span data-ttu-id="cf96c-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="cf96c-148">-AccessToken</span></span>

<span data-ttu-id="cf96c-149">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="cf96c-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="cf96c-150">Tokens de acesso são um tipo de credencial.</span><span class="sxs-lookup"><span data-stu-id="cf96c-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="cf96c-151">Você deve tomar as precauções de segurança adequadas para mantê-los confidenciais.</span><span class="sxs-lookup"><span data-stu-id="cf96c-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="cf96c-152">Tokens de acesso também são atingidos e podem impedir a conclusão de tarefas de longa execução.</span><span class="sxs-lookup"><span data-stu-id="cf96c-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="cf96c-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="cf96c-153">-AccountId</span></span>

<span data-ttu-id="cf96c-154">ID da conta do token de acesso no conjunto de parâmetros **AccessToken** .</span><span class="sxs-lookup"><span data-stu-id="cf96c-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="cf96c-155">ID da conta do serviço gerenciado no conjunto de parâmetros **ManagedService** .</span><span class="sxs-lookup"><span data-stu-id="cf96c-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="cf96c-156">Pode ser uma ID de recurso de serviço gerenciado ou a ID de cliente associada.</span><span class="sxs-lookup"><span data-stu-id="cf96c-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="cf96c-157">Para usar a identidade atribuída pelo sistema, deixe este campo em branco.</span><span class="sxs-lookup"><span data-stu-id="cf96c-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="cf96c-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cf96c-158">-ApplicationId</span></span>

<span data-ttu-id="cf96c-159">ID do aplicativo da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf96c-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="cf96c-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cf96c-160">-CertificateThumbprint</span></span>

<span data-ttu-id="cf96c-161">Hash ou impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="cf96c-162">-Contextname</span><span class="sxs-lookup"><span data-stu-id="cf96c-162">-ContextName</span></span>

<span data-ttu-id="cf96c-163">Nome do contexto padrão do Azure para este logon.</span><span class="sxs-lookup"><span data-stu-id="cf96c-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="cf96c-164">Para obter mais informações sobre contextos do Azure, consulte [objetos de contexto do PowerShell do PowerShell](/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="cf96c-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="cf96c-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="cf96c-165">-Credential</span></span>

<span data-ttu-id="cf96c-166">Especifica um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="cf96c-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="cf96c-167">Para obter mais informações sobre o objeto **PSCredential** , digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cf96c-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="cf96c-168">O objeto **PSCredential** fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="cf96c-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="cf96c-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf96c-169">-DefaultProfile</span></span>

<span data-ttu-id="cf96c-170">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf96c-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf96c-171">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="cf96c-171">-Environment</span></span>

<span data-ttu-id="cf96c-172">Ambiente que contém a conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf96c-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="cf96c-173">-Force</span><span class="sxs-lookup"><span data-stu-id="cf96c-173">-Force</span></span>

<span data-ttu-id="cf96c-174">Substitua o contexto existente com o mesmo nome sem perguntar.</span><span class="sxs-lookup"><span data-stu-id="cf96c-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="cf96c-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="cf96c-175">-GraphAccessToken</span></span>

<span data-ttu-id="cf96c-176">Serviço do AccessToken para Graph.</span><span class="sxs-lookup"><span data-stu-id="cf96c-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="cf96c-177">-Identidade</span><span class="sxs-lookup"><span data-stu-id="cf96c-177">-Identity</span></span>

<span data-ttu-id="cf96c-178">Faça logon usando uma identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="cf96c-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="cf96c-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="cf96c-180">AccessToken para o serviço de keyvault.</span><span class="sxs-lookup"><span data-stu-id="cf96c-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="cf96c-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="cf96c-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="cf96c-182">Nome do host para o serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-182">Host name for the managed service.</span></span>

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

### <span data-ttu-id="cf96c-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="cf96c-183">-ManagedServicePort</span></span>

<span data-ttu-id="cf96c-184">Número da porta do serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-184">Port number for the managed service.</span></span>

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

### <span data-ttu-id="cf96c-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="cf96c-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="cf96c-186">Token para o logon de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-186">Token for the managed service login.</span></span>

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

### <span data-ttu-id="cf96c-187">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="cf96c-187">-MaxContextPopulation</span></span>

<span data-ttu-id="cf96c-188">Número máximo de assinatura para preencher contextos após o logon.</span><span class="sxs-lookup"><span data-stu-id="cf96c-188">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="cf96c-189">O padrão é 25.</span><span class="sxs-lookup"><span data-stu-id="cf96c-189">Default is 25.</span></span> <span data-ttu-id="cf96c-190">Para preencher todas as assinaturas para contextos, defina como-1.</span><span class="sxs-lookup"><span data-stu-id="cf96c-190">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf96c-191">-Escopo</span><span class="sxs-lookup"><span data-stu-id="cf96c-191">-Scope</span></span>

<span data-ttu-id="cf96c-192">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="cf96c-192">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="cf96c-193">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="cf96c-193">-ServicePrincipal</span></span>

<span data-ttu-id="cf96c-194">Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf96c-194">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="cf96c-195">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="cf96c-195">-SkipContextPopulation</span></span>

<span data-ttu-id="cf96c-196">Ignora a população de contexto se não forem encontrados contextos.</span><span class="sxs-lookup"><span data-stu-id="cf96c-196">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="cf96c-197">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="cf96c-197">-SkipValidation</span></span>

<span data-ttu-id="cf96c-198">Ignorar validação para token de acesso.</span><span class="sxs-lookup"><span data-stu-id="cf96c-198">Skip validation for access token.</span></span>

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

### <span data-ttu-id="cf96c-199">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="cf96c-199">-Subscription</span></span>

<span data-ttu-id="cf96c-200">Nome ou ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf96c-200">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="cf96c-201">-Locatário</span><span class="sxs-lookup"><span data-stu-id="cf96c-201">-Tenant</span></span>

<span data-ttu-id="cf96c-202">Nome ou ID do locatário opcional.</span><span class="sxs-lookup"><span data-stu-id="cf96c-202">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="cf96c-203">Devido às limitações da API atual, você deve usar uma ID de locatário em vez de um nome de locatário ao se conectar com uma conta B2B (Business-to-Business).</span><span class="sxs-lookup"><span data-stu-id="cf96c-203">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="cf96c-204">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="cf96c-204">-UseDeviceAuthentication</span></span>

<span data-ttu-id="cf96c-205">Use a autenticação de código do dispositivo em vez de um controle do navegador.</span><span class="sxs-lookup"><span data-stu-id="cf96c-205">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="cf96c-206">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf96c-206">-Confirm</span></span>

<span data-ttu-id="cf96c-207">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf96c-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf96c-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf96c-208">-WhatIf</span></span>

<span data-ttu-id="cf96c-209">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-209">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf96c-210">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf96c-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf96c-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf96c-211">CommonParameters</span></span>
<span data-ttu-id="cf96c-212">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf96c-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf96c-213">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf96c-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf96c-214">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf96c-214">INPUTS</span></span>

### <span data-ttu-id="cf96c-215">System. String</span><span class="sxs-lookup"><span data-stu-id="cf96c-215">System.String</span></span>

## <span data-ttu-id="cf96c-216">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf96c-216">OUTPUTS</span></span>

### <span data-ttu-id="cf96c-217">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="cf96c-217">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="cf96c-218">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf96c-218">NOTES</span></span>

## <span data-ttu-id="cf96c-219">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf96c-219">RELATED LINKS</span></span>
