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
# Connect-AzureRmAccount

## Sinopse
Conecte-se ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### UserWithSubscriptionId (padrão)
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Connect-AzureRmAccount se conecta ao Azure com uma conta autenticada para uso com as solicitações do cmdlet do Azure Resource Manager.

Você pode usar essa conta autenticada somente com os cmdlets do Azure Resource Manager.

Para adicionar uma conta autenticada para uso com cmdlets de gerenciamento de serviços, use o Add-AzureAccount ou o cmdlet Import-AzurePublishSettingsFile.

Depois de executar esse cmdlet, você pode se desconectar de uma conta do Azure usando Disconnect-AzureRmAccount.

## EXEMPLOS

### Exemplo 1: usar um logon interativo para se conectar a uma conta do Azure
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Este comando se conecta a uma conta do Azure.

Para executar cmdlets do Azure Resource Manager com esta conta, você deve fornecer credenciais da conta da Microsoft ou da ID organizacional no prompt.

Se a autenticação multifator estiver habilitada para suas credenciais, você deverá fazer logon usando a opção interativo ou usar a autenticação de entidade de serviço.

### Exemplo 2: conectar-se a uma conta do Azure usando credenciais de ID organizacional
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.

O segundo comando se conecta a uma conta do Azure usando as credenciais armazenadas em $Credential.

Esta conta é autenticada com o Gerenciador de recursos do Azure usando credenciais de ID da organização.

Você não pode usar a autenticação multifator ou credenciais de conta da Microsoft para executar cmdlets do Azure Resource Manager com esta conta.

### Exemplo 3: conectar-se a uma conta da entidade de serviço do Azure
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

O primeiro comando obtém as credenciais do usuário e as armazena na variável $Credential.

O segundo comando se conecta ao Azure usando as credenciais de entidade de serviço armazenadas em $Credential para o locatário especificado.

O parâmetro de comutação UserPrincipal indica que a conta é autenticada como uma entidade de serviço.

### Exemplo 4: usar um logon interativo para se conectar a uma conta para um locatário e uma assinatura específicos
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Esse comando se conecta a uma conta do Azure e configurado AzureRM PowerShell para executar cmdlets para o locatário e a assinatura especificados por padrão.

### Exemplo 5: adicionar uma conta usando o logon de identidade de serviço gerenciado
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Esse comando conecta-se usando a identidade de serviço gerenciado do ambiente de host (por exemplo, se executado em um VirtualMachine com uma identidade de serviço gerenciado atribuída, isso permitirá que o código seja acessado usando essa identidade atribuída)

## OS

### -AccessToken
Especifica um token de acesso.

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

### -AccountId
ID da conta para token de acesso

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

### -ApplicationId
SPN

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

### -CertificateThumbprint
Hash do certificado (impressão digital)

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

### -Contextname
Nome do contexto padrão deste logon.  Você poderá selecionar esse contexto por este nome após o logon.

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

### -Credential
Especifica um objeto PSCredential.
Para obter mais informações sobre o objeto PSCredential, digite Get-Help Get-Credential.

O objeto PSCredential fornece a ID de usuário e a senha para as credenciais de ID organizacional ou a ID do aplicativo e o segredo para as credenciais do principal do serviço.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Ambiente
Ambiente que contém a conta para a qual entrar

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

### -Force
Substituir o contexto existente com o mesmo nome, se houver.

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

### -GraphAccessToken
Serviço do AccessToken para Graph

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

### -Identidade
Faça logon usando a identidade de serviço gerenciado no ambiente atual.

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

### -KeyVaultAccessToken
AccessToken para o serviço de keyvault

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

### -ManagedServiceHostName
Nome do host para logon no serviço gerenciado

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

### -ManagedServicePort
Número da porta para o logon no serviço gerenciado

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

### -Escopo
Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.

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

### -UserPrincipal
Indica que essa conta é autenticada fornecendo as credenciais de entidade de serviço.

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

### -SkipValidation
Ignorar validação para token de acesso

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

### -Assinatura
Nome ou ID da assinatura

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

### -Tenantid
Nome ou ID do locatário opcional

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### String
O parâmetro ' SubscriptionId ' aceita o valor do tipo ' String ' do pipeline

### String
O parâmetro ' Subscriptionname ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### PSAzureProfile
Credenciais, assinatura, conta e informações de locatário para o usuário conectado.

## INFORMA

## LINKS RELACIONADOS

