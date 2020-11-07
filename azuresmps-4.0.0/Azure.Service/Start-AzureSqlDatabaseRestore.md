---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945426"
---
# Start-AzureSqlDatabaseRestore

## Sinopse
Executa uma restauração point-in-time de um banco de dados.

## SYNTAX

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureSqlDatabaseRestore** executa uma restauração point-in-time de um banco de dados básico, padrão ou Premium.
O banco de dados SQL do Azure retém backups básicos de banco de dados por 7 dias, padrão por 14 dias e Premium para 35 dias.
A operação de restauração cria um novo banco de dados.
Se o banco de dados de origem não for excluído, o parâmetro *SourceDatabaseName* e *TargetDatabaseName* deverá ter valores diferentes.

No momento, o banco de dados SQL do Azure não é compatível com a restauração entre servidores.
Os nomes dos servidores de origem e de destino devem ser iguais.

## EXEMPLOS

### Exemplo 1: restaurar um banco de dados especificado como um objeto para um point-in-time
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

O primeiro comando obtém um objeto de banco de dados para o banco de dados chamado Database17 no servidor chamado Server01 e, em seguida, armazena-o na variável $Database.

O segundo comando restaura o banco de dados para um point-in-time específico.
O comando especifica o nome do novo banco de dados.

### Exemplo 2: restaurar um banco de dados especificado pelo nome para um point-in-time
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Esse comando restaura o banco de dados chamado Database17 a um point-in-time específico.
O comando especifica o nome do novo banco de dados.

### Exemplo 3: restaurar um banco de dados Descartado especificado como um objeto para um ponto no tempo
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

O primeiro comando obtém um objeto de banco de dados para o banco de dados chamado Database01 no servidor chamado Server01.
O comando especifica o parâmetro *RestorableDropped* .
Portanto, o cmdlet obtém o banco de dados recuperável desconectado do ponto de restauração especificado.
O comando armazena esse objeto de banco de dados na variável $Database.

O segundo comando restaura o banco de dados ignorado especificado pela $Database.
O comando especifica o nome do novo banco de dados.

## OS

### -PointInTime
Especifica o ponto de restauração no qual restaurar o banco de dados.
Quando a operação de restauração termina, o banco de dados é restaurado para o estado em que se encontra na data e hora em que esse parâmetro especifica.
Por padrão, para um banco de dados dinâmico definido como a hora atual e para um banco de dados solto, esse cmdlet usa a hora em que o banco de dados foi Descartado.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
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

### -RestorableDropped
Indica que esse cmdlet restaura um banco de dados recuperável removido.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Especifica o nome do banco de dados que este cmdlet restaura.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Especifica a data e a hora em que o banco de dados foi excluído.
Você deve incluir milissegundos quando especificar o tempo para corresponder ao tempo de exclusão do banco de dados real.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Especifica o nome do banco de dados dinâmico que este cmdlet restaura.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Especifica um objeto que representa o banco de dados recuperável ignorado que esse cmdlet restaura.
Para obter um objeto **RestorableDroppedDatabase** , use o cmdlet Get-AzureSqlDatabase e especifique o parâmetro *RestorableDropped* .

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Especifica o nome do servidor no qual o banco de dados de origem está em tempo real ou em execução, ou no qual o banco de dados de origem foi executado antes de ser excluído.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Especifica o nome do novo banco de dados que a operação de restauração cria.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Especifica o nome do servidor para o qual esse cmdlet restaura o banco de dados.

No momento, o banco de dados SQL do Azure não é compatível com a restauração entre servidores.
Os nomes dos servidores de origem e de destino devem ser iguais.

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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation

## INFORMA
* Você deve usar a autenticação baseada em certificado para executar esse cmdlet. Execute os seguintes comandos no computador onde executar este cmdlet: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Criar solicitação de restauração de banco de dados](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


