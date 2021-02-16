---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402415"
---
# Get-AzureSqlDatabaseCopy

## Sinopse
Verifica o status das relações de cópia.

## Sintaxe

### ByServerNameOnly (Padrão)
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

## Descrição
O cmdlet **Get-AzureSqlDatabaseCopy** verifica o status de uma ou mais relações de cópia ativa.
Execute este cmdlet depois de executar o cmdlet Start-AzureSqlDatabaseCopy ou Stop-AzureSqlDatabaseCopy cmdlet.
Você pode verificar uma relação de cópia específica, todas as relações de cópia ou uma lista filtrada de relações de cópia, como todas as cópias em um servidor de destino específico.
Você pode executar esse cmdlet no servidor que hospeda o banco de dados de origem ou de destino.

Este cmdlet é sincronizado.
O cmdlet bloqueia o console do Azure PowerShell até que ele retorne um objeto de status.

Os *parâmetros PartnerServer* *e PartnerDatabase* são opcionais.
Se você não especificar um dos parâmetros, esse cmdlet retornará uma tabela de resultados.
Para ver o status de apenas um determinado banco de dados, especifique os dois parâmetros.

## Exemplos

### Exemplo 1: Obter o status de cópia de um banco de dados
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Esse comando obtém o status do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.
O *parâmetro PartnerServer* restringe esse comando ao servidor bk0b8kf658.

### Exemplo 2: Obter o status de todas as cópias em um servidorGet o status de todas as cópias em um servidor
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Esse comando obtém o status de todas as cópias ativas no servidor chamado lpqd0zbr8y.

## Parâmetros

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL do Azure de origem.
Este cmdlet obtém o status de cópia do banco de dados especificado por esse parâmetro.

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
Este cmdlet obtém o status de cópia do banco de dados especificado por esse parâmetro.
Este parâmetro aceita a entrada de pipeline.

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

### -Nomedo Banco de Dados
Especifica o nome do banco de dados de origem.
Esse cmdlet obtém o status da cópia do banco de dados especificado por esse parâmetro.

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
Se esse banco de dados não for encontrado no modo sys.dm_database_copies de gerenciamento dinâmico, esse cmdlet retornará um objeto de status vazio.

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
Se esse servidor não for encontrado no modo sys.dm_database_copies de gerenciamento dinâmico, esse cmdlet retornará um objeto de status vazio.

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
Especifica o perfil do Azure a partir do qual este cmdlet é lido.
Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.

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

### -ServerName
Especifica o nome do servidor no qual reside a cópia do banco de dados.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## Saídas

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## Notas
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para ver um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte New-AzureSqlDatabaseServerContext cmdlet.

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


