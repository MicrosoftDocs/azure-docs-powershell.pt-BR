---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946293"
---
# Get-AzureSqlDatabaseOperation

## Sinopse
Obtém o status das operações de banco de dados em um servidor do Azure.

## SYNTAX

### ByConnectionContext (padrão)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseOperation** Obtém o status das operações de banco de dados no servidor do Azure especificado.
Se você especificar somente o parâmetro *ServerName* ou *ConnectionContext* , o cmdlet obterá todas as operações de banco de dados para o servidor.
Se você também especificar um banco de dados usando o parâmetro *Database* ou *DatabaseName* , esse cmdlet obterá todas as operações para o banco de dados especificado.
Se você especificar um GUID de operação e *nomedoservidor* ou *ConnectionContext* , o cmdlet receberá uma única operação de banco de dados.

## EXEMPLOS

### Exemplo 1: obter o status de todas as operações de banco de dados de um banco de dados
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Esse comando obtém o status de todas as operações de banco de dados no banco de dados chamada Database17 no servidor que o contexto de conexão $Context especifica.

### Exemplo 2: obter o status de todas as operações de banco de dados de um servidor
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Esse comando obtém o status de todas as operações de banco de dados no servidor que o contexto de conexão $Context especifica.

## OS

### -ConnectionContext
Especifica o contexto de conexão de um servidor.

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
Especifica um objeto que representa um banco de dados SQL do Azure.
Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .

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

### -DatabaseName
Especifica o nome de um banco de dados.
Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
Especifica a ID da operação que representa uma operação de banco de dados específica para a qual esse cmdlet obtém o status.
Você pode obter IDs de operação solicitando todas as operações de banco de dados de um banco de dados SQL do Azure ou servidor.
Se você especificar esse parâmetro, deverá especificar o parâmetro *ServerName* ou o parâmetro *ConnectionContext* .

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Especifica o nome de um servidor.

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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext

### System. GUID

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []
Esse cmdlet retorna uma matriz de objetos **DatabaseOperationResponseList** se você obtém várias operações.

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Status da operação do banco de dados](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


