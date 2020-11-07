---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946396"
---
# Add-AzureAccount

## Sinopse
Adiciona a conta do Azure ao Windows PowerShell.

## SYNTAX

### Usuário (padrão)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipalName
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureAccount** torna sua conta do Azure e suas assinaturas disponíveis no Windows PowerShell.
É como se conectar à sua conta do Azure no Windows PowerShell.
Para fazer logout da conta, use o cmdlet **Remove-AzureAccount** .

**Add-AzureAccount** baixa informações sobre a sua conta do Azure e salva-as em um arquivo de dados de assinatura em seu perfil de usuário móvel.
Ele também obtém um token de acesso que permite que o Windows PowerShell acesse sua conta do Azure em seu nome.
Quando o comando é concluído, você pode gerenciar sua conta do Azure no Windows PowerShell.

Há duas maneiras diferentes de disponibilizar sua conta do Azure para o Windows PowerShell.
Você pode usar o cmdlet **Add-AzureAccount** , que usa tokens de acesso de autenticação do Azure Active Directory (Azure AD) ou **Import-AzurePublishSettingsFile** , que usa um certificado de gerenciamento.
Para obter orientação sobre qual método usar, consulte [como: conectar-se à sua assinatura](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

Quando você executa **Add-AzureAccount** , ele exibe uma janela interativa que solicita que você entre na sua conta do Azure.
Esta entrada é válida até que o token de acesso expire.
Quando expira, os cmdlets que exigem acesso à sua conta solicitam que você execute **Add-AzureAccount** novamente.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: adicionar uma conta
```
PS C:\> Add-AzureAccount
```

Esse comando adiciona uma conta do Azure ao Windows PowerShell.
Quando você executa o comando, um Windows é exibido para solicitar o nome de usuário e a senha da conta.

### Exemplo 2: usar um arquivo de dados de assinatura alternativo
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Esse comando usa o parâmetro **SubscriptionDataFile** para o **Add-AzureAccount** direto para armazenar os dados da conta no arquivo C:\Testing\SDF.xml, em vez do arquivo padrão.

## OS

### -Credential
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ambiente
Especifica um ambiente do Azure.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Locatário
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Não é possível canalizar a entrada para este cmdlet

## EXIBE

### Nenhuma
Esse cmdlet não retorna nenhuma saída.

## INFORMA
* **Add-AzureAccount** (e o método de autenticação do Azure AD) tem precedência sobre **Import-AzurePublishSettings** (e o método de certificado de gerenciamento). Se você usar **Add-AzureAccount** mesmo uma vez na sua conta, o método de autenticação do Azure ad será usado e o certificado de gerenciamento será ignorado. Para remover o token do Azure AD e restaurar o método de certificado de gerenciamento, use o cmdlet **Remove-AzureAccount** . Para obter mais informações, digite: **Get-Help Remove-AzureAccount**.
* O erro, "suas credenciais venceram. Use Add-AzureAccount para entrar novamente. " indica que o token de acesso expirou e o Windows PowerShell não pode acessar sua conta do Azure. Para restaurar o acesso à sua conta, execute **Add-AzureAccount** novamente.
* Os cmdlets da assinatura e da conta do PowerShell do Azure recebem seus dados do arquivo de dados de assinatura, e não da conta do Azure ao vivo. Se você alterar sua conta ou assinaturas fora do Windows PowerShell, por exemplo, usando o portal de gerenciamento do Azure, execute **Add-AzureAccount** novamente para atualizar o arquivo de dados de assinatura.

## LINKS RELACIONADOS

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


