---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945970"
---
# New-AzureSqlDatabaseServerContext

## Sinopse
Cria um contexto de conexão do servidor.

## SYNTAX

### ByServerNameWithSqlAuth (padrão)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSqlDatabaseServerContext** cria um contexto de conexão do servidor de banco de dados SQL do Azure.
Use a autenticação do SQL Server para criar um contexto de conexão para um servidor de banco de dados SQL usando as credenciais especificadas.
Você pode especificar o servidor de banco de dados SQL por nome, pelo nome totalmente qualificado ou por URL.
Para obter uma credencial, use o cmdlet Get-Credential que solicita que você especifique o nome de usuário e a senha.

Use o cmdlet **New-AzureSqlDatabaseServerContext** com autenticação baseada em certificado para criar um contexto de conexão para o servidor de banco de dados SQL especificado usando os dados de assinatura do Azure especificados.
Você pode especificar o servidor de banco de dados SQL por nome ou pelo nome totalmente qualificado.
Você pode especificar os dados de assinatura como um parâmetro ou pode ser recuperado da assinatura atual do Azure.
Use o cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx para selecionar a assinatura atual do Azure.

## EXEMPLOS

### Exemplo 1: criar um contexto usando a autenticação do SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Este exemplo usa a autenticação do SQL Server.

O primeiro comando solicita as credenciais de administrador do servidor e armazena as credenciais na variável $Credential.

O segundo comando se conecta ao servidor de banco de dados SQL chamado lpqd0zbr8y usando $Credential.

O comando final cria um banco de dados denominado Database17 no servidor que faz parte do contexto em $Context.

### Exemplo 2: criar um contexto usando a autenticação baseada em certificado
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Este exemplo usa a autenticação baseada em certificado.

Os dois primeiros comandos atribuem valores para as variáveis $SubscriptionId e $Thumbprint.

O terceiro comando obtém o certificado identificado pela impressão digital no $Thumbprint e o armazena em $Certificate.

O quarto comando define a assinatura como Subscription07 e o quinto comando seleciona essa assinatura.

O comando final cria um contexto na assinatura atual do servidor chamado lpqd0zbr8y.

## OS

### -Credential
Especifica um objeto Credential que fornece autenticação do SQL Server para que você acesse o servidor.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Especifica o nome FQDN (nome de domínio totalmente qualificado) do servidor de banco de dados SQL do Azure.
Por exemplo, Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Especifica a URL que este cmdlet usa para acessar o portal do SQL DatabaseManagement do Azure para o servidor.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -Nomedoservidor
Especifica o nome do servidor de banco de dados.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Especifica o nome da assinatura do Azure que este cmdlet usa para criar o contexto de conexão.
Se você não especificar um valor para esse parâmetro, o cmdlet usará a assinatura atual.
Execute o cmdlet Select-AzureSubscription para alterar a assinatura atual.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Indica que esse cmdlet usa a assinatura do Azure para a criação do contexto de conexão.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. IServerDataServiceContext

## INFORMA
* Se você autenticar sem especificar um domínio e se usar o Windows PowerShell 2,0, o cmdlet Get-Credential retornará uma barra invertida ( \\ ) precedida para o nome de usuário, por exemplo, \User. O Windows PowerShell 3,0 não adiciona a barra invertida. Esta barra invertida não é reconhecida pelo parâmetro *Credential* do cmdlet **New-AzureSqlDatabaseServerContext** . Para removê-la, use comandos semelhantes ao seguinte:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## LINKS RELACIONADOS

[Cmdlets do banco de dados SQL do Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


