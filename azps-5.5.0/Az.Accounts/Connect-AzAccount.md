---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111261"
---
# <span data-ttu-id="15bba-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="15bba-101">Connect-AzAccount</span></span>

## <span data-ttu-id="15bba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15bba-102">SYNOPSIS</span></span>
<span data-ttu-id="15bba-103">Conecte-se ao Azure com uma conta autenticada para uso com cmdlets dos módulos do PowerShell do Az.</span><span class="sxs-lookup"><span data-stu-id="15bba-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="15bba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15bba-104">SYNTAX</span></span>

### <span data-ttu-id="15bba-105">UserWithSubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="15bba-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15bba-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15bba-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15bba-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="15bba-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15bba-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15bba-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15bba-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15bba-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15bba-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="15bba-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15bba-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="15bba-111">DESCRIPTION</span></span>

<span data-ttu-id="15bba-112">O cmdlet conecta-se ao Azure com uma conta autenticada para uso com `Connect-AzAccount` cmdlets dos módulos do PowerShell do Az.</span><span class="sxs-lookup"><span data-stu-id="15bba-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="15bba-113">Você só pode usar essa conta autenticada com solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="15bba-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="15bba-114">Para adicionar uma conta autenticada para uso com o Gerenciamento de Serviços, use o `Add-AzureAccount` cmdlet do módulo do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="15bba-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="15bba-115">Se nenhum contexto for encontrado para o usuário atual, a lista de contexto do usuário será preenchida com um contexto para cada uma das 25 primeiras assinaturas.</span><span class="sxs-lookup"><span data-stu-id="15bba-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="15bba-116">A lista de contextos criados para o usuário pode ser encontrada em `Get-AzContext -ListAvailable` execução.</span><span class="sxs-lookup"><span data-stu-id="15bba-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="15bba-117">Para ignorar essa população de contexto, especifique o parâmetro de opção **SkipContextPopulation.**</span><span class="sxs-lookup"><span data-stu-id="15bba-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="15bba-118">Depois de executar este cmdlet, você pode se desconectar de uma conta do Azure `Disconnect-AzAccount` usando.</span><span class="sxs-lookup"><span data-stu-id="15bba-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="15bba-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15bba-119">EXAMPLES</span></span>

### <span data-ttu-id="15bba-120">Exemplo 1: Conectar-se a uma conta do Azure</span><span class="sxs-lookup"><span data-stu-id="15bba-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="15bba-121">Este exemplo se conecta a uma conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="15bba-121">This example connects to an Azure account.</span></span> <span data-ttu-id="15bba-122">Você deve fornecer uma conta da Microsoft ou credenciais de ID organizacional.</span><span class="sxs-lookup"><span data-stu-id="15bba-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="15bba-123">Se a autenticação multifa factore estiver habilitada para suas credenciais, você deverá entrar usando a opção interativa ou usar a autenticação de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15bba-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="15bba-124">Exemplo 2: (Somente Windows PowerShell 5.1) Conecte-se ao Azure usando credenciais de ID organizacional</span><span class="sxs-lookup"><span data-stu-id="15bba-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="15bba-125">Esse cenário funciona somente no Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="15bba-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="15bba-126">O primeiro comando solicita credenciais de usuário e as armazena na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="15bba-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="15bba-127">O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas `$Credential` em .</span><span class="sxs-lookup"><span data-stu-id="15bba-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="15bba-128">Essa conta é autenticada com o Azure usando credenciais de ID organizacional.</span><span class="sxs-lookup"><span data-stu-id="15bba-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="15bba-129">Exemplo 3: Conectar-se ao Azure usando uma conta de entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="15bba-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="15bba-130">O primeiro comando solicita credenciais de entidade de serviço e as armazena na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="15bba-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="15bba-131">Insira sua ID do aplicativo para o nome de usuário e o segredo da entidade de serviço como a senha quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="15bba-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="15bba-132">O segundo comando conecta o locatário especificado do Azure usando as credenciais de entidade de serviço armazenadas na `$Credential` variável.</span><span class="sxs-lookup"><span data-stu-id="15bba-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="15bba-133">O **parâmetro de opção ServicePrincipal** indica que a conta é autenticada como uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15bba-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="15bba-134">Exemplo 4: Usar um logon interativo para se conectar a um locatário e uma assinatura específicos</span><span class="sxs-lookup"><span data-stu-id="15bba-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="15bba-135">Este exemplo se conecta a uma conta do Azure com o locatário e a assinatura especificados.</span><span class="sxs-lookup"><span data-stu-id="15bba-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="15bba-136">Exemplo 5: Conectar usando uma Identidade de Serviço Gerenciado</span><span class="sxs-lookup"><span data-stu-id="15bba-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="15bba-137">Este exemplo se conecta usando a MSI (Identidade de Serviço Gerenciado) do ambiente de host.</span><span class="sxs-lookup"><span data-stu-id="15bba-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="15bba-138">Por exemplo, você entra no Azure a partir de uma máquina virtual que tem um MSI atribuído.</span><span class="sxs-lookup"><span data-stu-id="15bba-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="15bba-139">Exemplo 6: Conectar usando o logon da Identidade de Serviço Gerenciado e o ClientId</span><span class="sxs-lookup"><span data-stu-id="15bba-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="15bba-140">Este exemplo se conecta usando a Identidade de Serviço Gerenciado **do myUserAssignedIdentity.**</span><span class="sxs-lookup"><span data-stu-id="15bba-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="15bba-141">Ele adiciona a identidade atribuída pelo usuário à máquina virtual e se conecta usando a ClientId da identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="15bba-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="15bba-142">Para obter mais informações, consulte Configurar identidades gerenciadas para recursos [do Azure em um VM do Azure.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="15bba-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="15bba-143">Exemplo 7: Conectar usando certificados</span><span class="sxs-lookup"><span data-stu-id="15bba-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="15bba-144">Este exemplo se conecta a uma conta do Azure usando a autenticação de entidade de serviço baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="15bba-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="15bba-145">A entidade de serviço usada para autenticação deve ser criada com o certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="15bba-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="15bba-146">Para obter mais informações sobre como criar certificados auto-assinados e atribuir permissões a eles, consulte Usar o PowerShell do [Azure](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) para criar uma entidade de serviço com um certificado</span><span class="sxs-lookup"><span data-stu-id="15bba-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="15bba-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15bba-147">PARAMETERS</span></span>

### <span data-ttu-id="15bba-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="15bba-148">-AccessToken</span></span>

<span data-ttu-id="15bba-149">Especifica um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="15bba-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="15bba-150">Os tokens do Access são um tipo de credencial.</span><span class="sxs-lookup"><span data-stu-id="15bba-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="15bba-151">Você deve tomar as precauções de segurança apropriadas para mantê-las confidenciais.</span><span class="sxs-lookup"><span data-stu-id="15bba-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="15bba-152">Os tokens do Access também têm tempo de tempo e podem impedir a conclusão de tarefas em execução longas.</span><span class="sxs-lookup"><span data-stu-id="15bba-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="15bba-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="15bba-153">-AccountId</span></span>

<span data-ttu-id="15bba-154">ID da conta para token de acesso **no conjunto de parâmetros accessToken.**</span><span class="sxs-lookup"><span data-stu-id="15bba-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="15bba-155">ID da conta do serviço gerenciado no **conjunto de parâmetros ManagedService.**</span><span class="sxs-lookup"><span data-stu-id="15bba-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="15bba-156">Pode ser uma ID de recurso de serviço gerenciado ou a ID do cliente associada.</span><span class="sxs-lookup"><span data-stu-id="15bba-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="15bba-157">Para usar a identidade atribuída ao sistema, deixe esse campo em branco.</span><span class="sxs-lookup"><span data-stu-id="15bba-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="15bba-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="15bba-158">-ApplicationId</span></span>

<span data-ttu-id="15bba-159">ID do aplicativo da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15bba-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="15bba-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="15bba-160">-CertificateThumbprint</span></span>

<span data-ttu-id="15bba-161">Hash de certificado ou impressão de miniatura.</span><span class="sxs-lookup"><span data-stu-id="15bba-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="15bba-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="15bba-162">-ContextName</span></span>

<span data-ttu-id="15bba-163">Nome do contexto padrão do Azure para este logon.</span><span class="sxs-lookup"><span data-stu-id="15bba-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="15bba-164">Para obter mais informações sobre contextos do Azure, consulte objetos de contexto do [Azure PowerShell.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="15bba-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="15bba-165">-Credencial</span><span class="sxs-lookup"><span data-stu-id="15bba-165">-Credential</span></span>

<span data-ttu-id="15bba-166">Especifica um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="15bba-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="15bba-167">Para obter mais informações sobre o **objeto PSCredential,** digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="15bba-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="15bba-168">O **objeto PSCredential** fornece a ID de usuário e a senha para credenciais de ID organizacional, ou a ID do aplicativo e as credenciais da entidade de serviço secreta.</span><span class="sxs-lookup"><span data-stu-id="15bba-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="15bba-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bba-169">-DefaultProfile</span></span>

<span data-ttu-id="15bba-170">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15bba-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15bba-171">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="15bba-171">-Environment</span></span>

<span data-ttu-id="15bba-172">Ambiente que contém a conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="15bba-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="15bba-173">-Forçar</span><span class="sxs-lookup"><span data-stu-id="15bba-173">-Force</span></span>

<span data-ttu-id="15bba-174">Sobrescreva o contexto existente com o mesmo nome sem solicitar.</span><span class="sxs-lookup"><span data-stu-id="15bba-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="15bba-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="15bba-175">-GraphAccessToken</span></span>

<span data-ttu-id="15bba-176">AccessToken para Serviço Graph.</span><span class="sxs-lookup"><span data-stu-id="15bba-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="15bba-177">-Identidade</span><span class="sxs-lookup"><span data-stu-id="15bba-177">-Identity</span></span>

<span data-ttu-id="15bba-178">Faça logon usando uma Identidade de Serviço Gerenciado.</span><span class="sxs-lookup"><span data-stu-id="15bba-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="15bba-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="15bba-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="15bba-180">AccessToken para Serviço KeyVault.</span><span class="sxs-lookup"><span data-stu-id="15bba-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="15bba-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="15bba-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="15bba-182">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="15bba-182">Obsolete.</span></span> <span data-ttu-id="15bba-183">Para usar o ponto de extremidade MSI personalizado, de definir a variável MSI_ENDPOINT ambiente, por exemplo, " http://localhost:50342/oauth2/token ".</span><span class="sxs-lookup"><span data-stu-id="15bba-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="15bba-184">Nome do host para o serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="15bba-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="15bba-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="15bba-185">-ManagedServicePort</span></span>

<span data-ttu-id="15bba-186">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="15bba-186">Obsolete.</span></span> <span data-ttu-id="15bba-187">Para usar o ponto de extremidade MSI personalizado, de definir a variável MSI_ENDPOINT ambiente, por exemplo, " http://localhost:50342/oauth2/token ". Número da porta do serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="15bba-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="15bba-188">-ManagedServiceSecsecsec</span><span class="sxs-lookup"><span data-stu-id="15bba-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="15bba-189">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="15bba-189">Obsolete.</span></span> <span data-ttu-id="15bba-190">Para usar o segredo de MSI personalizado, de definir as variáveis de MSI_SECRET.</span><span class="sxs-lookup"><span data-stu-id="15bba-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="15bba-191">Token para o logon do serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="15bba-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="15bba-192">-MaxContextPopulation</span><span class="sxs-lookup"><span data-stu-id="15bba-192">-MaxContextPopulation</span></span>

<span data-ttu-id="15bba-193">Número máximo de assinatura para preencher contextos após o logon.</span><span class="sxs-lookup"><span data-stu-id="15bba-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="15bba-194">O padrão é 25.</span><span class="sxs-lookup"><span data-stu-id="15bba-194">Default is 25.</span></span> <span data-ttu-id="15bba-195">Para preencher todas as assinaturas de contextos, de definida como -1.</span><span class="sxs-lookup"><span data-stu-id="15bba-195">To populate all subscriptions to contexts, set to -1.</span></span>

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

### <span data-ttu-id="15bba-196">-Escopo</span><span class="sxs-lookup"><span data-stu-id="15bba-196">-Scope</span></span>

<span data-ttu-id="15bba-197">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="15bba-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="15bba-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="15bba-198">-ServicePrincipal</span></span>

<span data-ttu-id="15bba-199">Indica que essa conta autentica fornece credenciais de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15bba-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="15bba-200">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="15bba-200">-SkipContextPopulation</span></span>

<span data-ttu-id="15bba-201">Ignora a população de contexto se nenhum contexto for encontrado.</span><span class="sxs-lookup"><span data-stu-id="15bba-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="15bba-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="15bba-202">-SkipValidation</span></span>

<span data-ttu-id="15bba-203">Ignorar a validação do token de acesso.</span><span class="sxs-lookup"><span data-stu-id="15bba-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="15bba-204">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="15bba-204">-Subscription</span></span>

<span data-ttu-id="15bba-205">Nome da assinatura ou ID.</span><span class="sxs-lookup"><span data-stu-id="15bba-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="15bba-206">-Locatário</span><span class="sxs-lookup"><span data-stu-id="15bba-206">-Tenant</span></span>

<span data-ttu-id="15bba-207">Nome ou ID do locatário opcional.</span><span class="sxs-lookup"><span data-stu-id="15bba-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="15bba-208">Devido às limitações da API atual, você deve usar uma ID de locatário em vez de um nome de locatário ao se conectar a uma conta de negócios para empresas (B2B).</span><span class="sxs-lookup"><span data-stu-id="15bba-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="15bba-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="15bba-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="15bba-210">Use a autenticação de código de dispositivo em vez de um controle do navegador.</span><span class="sxs-lookup"><span data-stu-id="15bba-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="15bba-211">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="15bba-211">-Confirm</span></span>

<span data-ttu-id="15bba-212">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15bba-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15bba-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15bba-213">-WhatIf</span></span>

<span data-ttu-id="15bba-214">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="15bba-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15bba-215">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15bba-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15bba-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bba-216">CommonParameters</span></span>
<span data-ttu-id="15bba-217">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bba-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bba-218">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15bba-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bba-219">Entradas</span><span class="sxs-lookup"><span data-stu-id="15bba-219">INPUTS</span></span>

### <span data-ttu-id="15bba-220">System.String</span><span class="sxs-lookup"><span data-stu-id="15bba-220">System.String</span></span>

## <span data-ttu-id="15bba-221">Saídas</span><span class="sxs-lookup"><span data-stu-id="15bba-221">OUTPUTS</span></span>

### <span data-ttu-id="15bba-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="15bba-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="15bba-223">Notas</span><span class="sxs-lookup"><span data-stu-id="15bba-223">NOTES</span></span>

## <span data-ttu-id="15bba-224">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15bba-224">RELATED LINKS</span></span>
