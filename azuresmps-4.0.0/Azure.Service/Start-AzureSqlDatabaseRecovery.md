---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945423"
---
# Start-AzureSqlDatabaseRecovery

## Sinopse
Inicia uma solicitação de restauração para um banco de dados.

## SYNTAX

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureSqlDatabaseRecovery** inicia uma solicitação de restauração para um banco de dados ao vivo ou descartado.
Esse cmdlet dá suporte à recuperação básica que usa o último backup disponível conhecido para o banco de dados.
A operação de recuperação cria um novo banco de dados.
Se você recuperar um banco de dados dinâmico no mesmo servidor, você deve especificar um nome diferente para o novo banco de dados.

Para fazer uma restauração point-in-time para um banco de dados, use o cmdlet **Start-AzureSqlDatabaseRestore** em vez disso.

## EXEMPLOS

### Exemplo 1: recuperar um banco de dados especificado como um objeto
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

O primeiro comando obtém um objeto de banco de dados usando o cmdlet **Get-AzureSqlRecoverableDatabase** .
O comando armazena esse objeto na variável $Database.

O segundo comando recupera o banco de dados armazenado em $Database.

### Exemplo 2: recuperar um banco de dados especificado pelo nome
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Esse comando recupera um banco de dados usando o nome do banco de dados.

## OS

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

### -SourceDatabase
Especifica o objeto de banco de dados que representa o banco de dados que este cmdlet recupera.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Especifica o nome do banco de dados que este cmdlet recupera.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Especifica o nome do servidor no qual o banco de dados de origem está em tempo real ou em execução, ou no qual o banco de dados de origem foi executado antes de ser excluído.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Especifica o nome do banco de dados recuperado.
Se o banco de dados de origem ainda estiver ao vivo, para recuperá-lo para o mesmo servidor, você deve especificar um nome diferente do nome do banco de dados de origem.

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

### -TargetServerName
Especifica o nome do servidor para o qual restaurar um banco de dados.
Você pode restaurar um banco de dados para o mesmo servidor ou para um servidor diferente.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Management. Sql. Models. RecoverableDatabase

## EXIBE

### Microsoft. WindowsAzure. Management. Sql. Models. RecoverDatabaseOperation

## INFORMA
* Você deve usar a autenticação baseada em certificado para executar esse cmdlet. Execute os seguintes comandos no computador em que você executa este cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Criar solicitação de recuperação de banco de dados](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Replicação geográfica no banco de dados SQL do Azure](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


