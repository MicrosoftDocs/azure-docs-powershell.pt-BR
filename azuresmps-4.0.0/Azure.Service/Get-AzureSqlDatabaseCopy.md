---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946295"
---
# Get-AzureSqlDatabaseCopy

## Sinopse
Verifica o status das relações de cópia.

## SYNTAX

### ByServerNameOnly (padrão)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseCopy** verifica o status de uma ou mais relações de cópia ativas.
Execute este cmdlet depois de executar o cmdlet Start-AzureSqlDatabaseCopy ou Stop-AzureSqlDatabaseCopy.
Você pode verificar uma relação de cópia específica, todas as relações de cópia ou uma lista filtrada de relações de cópia, como todas as cópias em um servidor de destino específico.
Você pode executar esse cmdlet no servidor que hospeda o banco de dados de origem ou de destino.

Este cmdlet é síncrono.
O cmdlet bloqueia o console do PowerShell do Azure até que ele retorne um objeto de status.

Os parâmetros *PartnerServer* e *PartnerDatabase* são opcionais.
Se você não especificar nenhum dos parâmetros, esse cmdlet retornará uma tabela de resultados.
Para ver o status de apenas um banco de dados específico, especifique ambos os parâmetros.

## EXEMPLOS

### Exemplo 1: obter o status da cópia de um banco de dados
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Esse comando obtém o status do banco de dados chamado pedidos no servidor chamado lpqd0zbr8y.
O parâmetro *PartnerServer* restringe esse comando para o servidor bk0b8kf658.

### Exemplo 2: obter o status de todas as cópias em um serverGet o status de todas as cópias em um servidor
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Esse comando obtém o status de todas as cópias ativas no servidor chamado lpqd0zbr8y.

## OS

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL de origem do Azure.
Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Especifica um objeto que representa um banco de dados.
Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.
Esse parâmetro aceita entrada de pipeline.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do banco de dados de origem.
Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Especifica o nome do banco de dados secundário.
Se esse banco de dados não for encontrado no modo de exibição de gerenciamento dinâmico sys.dm_database_copies, esse cmdlet retornará um objeto de status vazio.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Especifica o nome do servidor que hospeda o banco de dados de destino.
Se esse servidor não for encontrado no modo de exibição de gerenciamento dinâmico sys.dm_database_copies, esse cmdlet retornará um objeto de status vazio.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -Nomedoservidor
Especifica o nome do servidor no qual a cópia do banco de dados reside.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

## INFORMA
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet New-AzureSqlDatabaseServerContext.

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Cmdlets do banco de dados SQL do Azure](./Azure.SQLDatabase.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Parar-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


