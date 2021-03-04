---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891539"
---
# Connect-AzAccount

## SYNOPSIS
Conecte-se ao Azure com uma conta autenticada para uso com cmdlets dos módulos do Az PowerShell.

## SINTAXE

### UserWithSubscriptionId (Padrão)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

O cmdlet se conecta ao Azure com uma conta autenticada para uso com `Connect-AzAccount` cmdlets dos módulos do Az PowerShell. Você pode usar essa conta autenticada somente com solicitações do Gerenciador de Recursos do Azure. Para adicionar uma conta autenticada para uso com o Gerenciamento de Serviços, use `Add-AzureAccount` o cmdlet do módulo do Azure PowerShell. Se nenhum contexto for encontrado para o usuário atual, a lista de contexto do usuário será preenchida com um contexto para cada uma das 25 primeiras assinaturas.
A lista de contextos criados para o usuário pode ser encontrada executando `Get-AzContext -ListAvailable` . Para ignorar essa população de contexto, especifique o parâmetro de opção **SkipContextPopulation.** Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando `Disconnect-AzAccount` .

## EXEMPLOS

### Exemplo 1: Conectar-se a uma conta do Azure

Este exemplo se conecta a uma conta do Azure. Você deve fornecer uma conta da Microsoft ou credenciais de ID organizacional. Se a autenticação multifa factor estiver habilitada para suas credenciais, você deverá fazer logoff usando a opção interativa ou usar a autenticação de entidade de serviço.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exemplo 2: (somente Windows PowerShell 5.1) Conecte-se ao Azure usando credenciais de ID organizacional

Esse cenário funciona somente Windows PowerShell 5.1. O primeiro comando solicita credenciais de usuário e as armazena na `$Credential` variável. O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas em `$Credential` . Essa conta é autenticada com o Azure usando credenciais de ID organizacional.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exemplo 3: Conectar-se ao Azure usando uma conta de entidade de serviço

O primeiro comando solicita credenciais de entidade de serviço e as armazena na `$Credential` variável. Insira a ID do aplicativo para o nome de usuário e o segredo da entidade de serviço como senha quando solicitado. O segundo comando conecta o locatário do Azure especificado usando as credenciais de entidade de serviço armazenadas na `$Credential` variável. O parâmetro de opção **ServicePrincipal** indica que a conta é autenticada como uma entidade de serviço.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exemplo 4: usar um logon interativo para se conectar a um locatário e assinatura específicos

Este exemplo se conecta a uma conta do Azure com o locatário e a assinatura especificados.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exemplo 5: Conectar usando uma Identidade de Serviço Gerenciado

Este exemplo se conecta usando a MSI (Identidade de Serviço Gerenciado) do ambiente host. Por exemplo, você entra no Azure de uma máquina virtual que tem uma MSI atribuída.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Exemplo 6: Conectar-se usando o logon de Identidade de Serviço Gerenciado e ClientId

Este exemplo se conecta usando a Identidade de Serviço Gerenciado **de myUserAssignedIdentity**. Ele adiciona a identidade atribuída pelo usuário à máquina virtual e, em seguida, se conecta usando o ClientId da identidade atribuída pelo usuário. Para obter mais informações, [consulte Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).

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

### Exemplo 7: Conectar-se usando certificados

Este exemplo se conecta a uma conta do Azure usando autenticação de entidade de serviço baseada em certificado.
A entidade de serviço usada para autenticação deve ser criada com o certificado especificado. Para obter mais informações sobre como criar certificados auto-assinados e atribuir permissões a eles, consulte Usar o [Azure PowerShell para](/azure/active-directory/develop/howto-authenticate-service-principal-powershell) criar uma entidade de serviço com um certificado

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

## PARÂMETROS

### -AccessToken

Especifica um token de acesso.

> [!CAUTION]
> Tokens de acesso são um tipo de credencial. Você deve tomar as precauções de segurança apropriadas para mantê-las confidenciais. Os tokens de acesso também têm tempo de vida e podem impedir que tarefas em execução longas sejam concluídas.

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

### -AccountId

ID da conta para token de acesso **no conjunto de parâmetros AccessToken.** ID da conta do serviço gerenciado no **conjunto de parâmetros ManagedService.** Pode ser uma ID de recurso de serviço gerenciado ou a ID do cliente associada.
Para usar a identidade atribuída ao sistema, deixe este campo em branco.

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

### -ApplicationId

ID do aplicativo da entidade de serviço.

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

### -CertificateThumbprint

Hash de certificado ou impressão digital.

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

### -ContextName

Nome do contexto padrão do Azure para esse logon. Para obter mais informações sobre contextos do Azure, consulte Objetos de contexto do [Azure PowerShell.](/powershell/azure/context-persistence)

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

### -Credential

Especifica um **objeto PSCredential.** Para obter mais informações sobre o **objeto PSCredential,** digite `Get-Help Get-Credential` . O **objeto PSCredential** fornece a ID do usuário e a senha para credenciais de ID organizacional, ou a ID do aplicativo e o segredo para credenciais de entidade de serviço.

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

### -DefaultProfile

As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Environment

Ambiente que contém a conta do Azure.

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

### -Force

Sobrescreva o contexto existente com o mesmo nome sem solicitar.

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

### -GraphAccessToken

AccessToken for Graph Service.

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

### -Identity

Faça logon usando uma Identidade de Serviço Gerenciado.

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

### -KeyVaultAccessToken

AccessToken para Serviço KeyVault.

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

### -ManagedServiceHostName

Obsoleto. Para usar o ponto de extremidade MSI personalizado, de definir a variável de ambiente MSI_ENDPOINT, por exemplo, " http://localhost:50342/oauth2/token ". Nome do host para o serviço gerenciado.

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

### -ManagedServicePort

Obsoleto. Para usar o ponto de extremidade MSI personalizado, de definir a variável de ambiente MSI_ENDPOINT, por exemplo, " http://localhost:50342/oauth2/token ". Número da porta para o serviço gerenciado.

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

### -ManagedServiceSecret

Obsoleto. Para usar o segredo MSI personalizado, de definir a variável de ambiente MSI_SECRET. Token para o logon do serviço gerenciado.

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

### -MaxContextPopulation

Número máximo de assinatura para preencher contextos após o logon. O padrão é 25. Para preencher todas as assinaturas em contextos, de acordo com -1.

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

### -Scope

Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.

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

### -ServicePrincipal

Indica que essa conta é autenticada fornecendo credenciais de entidade de serviço.

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

### -SkipContextPopulation

Ignora a população de contexto se nenhum contexto for encontrado.

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

### -SkipValidation

Ignore a validação do token de acesso.

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

### -Subscription

Nome da assinatura ou ID.

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

### -Tenant

ID ou nome de locatário opcional.

> [!NOTE]
> Devido às limitações da API atual, você deve usar uma ID de locatário em vez de um nome de locatário ao se conectar a uma conta de negócios para empresas (B2B).

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

### -UseDeviceAuthentication

Use a autenticação de código de dispositivo em vez de um controle do navegador.

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

### -Confirm

Solicita a confirmação antes de executar o cmdlet.

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

### -WhatIf

Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## NOTES

## LINKS RELACIONADOS
