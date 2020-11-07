---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946298"
---
# Get-AzureSqlDatabase

## Sinopse
Recupera um ou mais bancos de dados.

## SYNTAX

### ByConnectionContext (padrão)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabase** recupera uma ou mais instâncias de um banco de dados SQL do Azure de um servidor de banco de dados SQL do Azure.
Você pode especificar o servidor com um contexto de conexão de servidor de banco de dados SQL do Azure que você cria usando o cmdlet **New-AzureSqlDatabaseServerContext** .
Ou, se você especificar o nome do servidor do banco de dados SQL do Azure, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação de acesso ao servidor.

Se você não especificar um banco de dados, o cmdlet **Get-AzureSqlDatabase** retornará todos os bancos de dados do servidor especificado.

Recuperando bancos de dados recuperáveis desconectados:

Recupere bancos de dados recuperáveis desconectados usando o parâmetro *RestorableDropped* .
Para retornar todos os bancos de dados removidos recuperáveis, use o parâmetro *RestorableDropped* sem *DatabaseName* e *DatabaseDeletionDate*.
Para retornar um banco de dados recuperável específico, use o parâmetro *RestorableDropped* com os parâmetros *DatabaseName* e *DatabaseDeletionDate* .
Ao recuperar um banco de dados recuperável específico usando o parâmetro *DatabaseName* , você também deve incluir o parâmetro *DatabaseDeletionDate* e o valor *DatabaseDeletionDate* especificado deve incluir milissegundos para corresponder ao banco de dados desejado.

O cmdlet **Get-AzureSqlDatabase** retorna todos os bancos de dados removidos recuperáveis em um servidor ou um banco de dados específico que corresponda a *DatabaseName* e *DatabaseDeletionDate*.
Para retornar os bancos de dados removidos recuperáveis que satisfaçam critérios diferentes, como todos os bancos de dados removidos recuperáveis de um nome específico, você deve retornar todos os bancos de dados recuperáveis e filtrar os resultados no cliente.

## EXEMPLOS

### Exemplo 1: recuperar todos os bancos de dados em um servidor
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Esse comando recupera todos os bancos de dados no servidor chamado lpqd0zbr8y.

### Exemplo 2: recuperar todos os bancos de dados removidos recuperáveis em um servidor
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Esse comando recupera todos os bancos de dados removidos recuperáveis no servidor chamado lpqd0zbr8y.

### Exemplo 3: recuperar um banco de dados de um servidor especificado por um contexto de conexão
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Esse comando recupera o banco de dados denominado Database01 do servidor especificado pelo contexto de conexão $Context.

### Exemplo 4: armazenar um objeto de banco de dados em uma variável
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Esse comando recupera o banco de dados denominado Database01 do servidor chamado lpqd0zbr8y.
O comando armazena o objeto de banco de dados na variável $Database 01.

### Exemplo 5: recuperar um banco de dados recuperável removido
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Esse comando recupera o banco de dados removido recuperável chamado Database01 que foi excluído no 11/9/2012 do servidor chamado lpqd0zbr8y.
Esse comando armazena os resultados na variável $DroppedDB.

### Exemplo 6: recuperar todos os bancos de dados removidos recuperáveis em um servidor e filtrar os resultados
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Esse comando recupera todos os bancos de dados removidos recuperáveis no servidor chamado lpqd0zbr8y e filtra os resultados somente para bancos de dados chamados ContactDB.

## OS

### -ConnectionContext
Especifica o contexto de conexão de um servidor do qual recuperar um banco de dados.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Banco de dados
Especifica um objeto que representa o banco de dados recuperado pelo cmdlet.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Especifica a data e a hora de uma exclusão.
Se você especificar o parâmetro *RestorableDropped* , especifique esse parâmetro para recuperar um banco de dados recuperável Descartado com base na data e hora de exclusão.

O parâmetro *DatabaseDeletionDate* deve incluir milissegundos para corresponder ao tempo do banco de dados desejado.
Especificar um valor sem nenhum resultado de milissegundos não é possível localizar o banco de dados.

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

### -DatabaseName
Especifica o nome do banco de dados que este cmdlet recupera.

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
Indica que esse cmdlet retorna objetos *RestorableDroppedDatabase* em vez de objetos de *banco de dados* .
Você pode usar o parâmetro *DatabaseDeletionDate* para selecionar um banco de dados recuperável que pode ser removida.

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

### -RestorableDroppedDatabase
Especifica um objeto que representa o banco de dados recuperável ignorado que esse cmdlet recupera.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que contém o banco de dados que este cmdlet recupera.
O cmdlet usa a assinatura atual do Azure para acessar o servidor.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

## EXIBE

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Esse cmdlet retorna um objeto de *banco de dados* se você não especificar o parâmetro *RestorableDropped* .

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Esse cmdlet retorna um objeto *RestorableDroppedDatabase* se você especificar o parâmetro *RestorableDropped* .

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


