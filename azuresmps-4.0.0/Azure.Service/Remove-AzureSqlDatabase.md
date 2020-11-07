---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946108"
---
# Remove-AzureSqlDatabase

## Sinopse
Exclui um banco de dados SQL do Azure.

## SYNTAX

### ByNameWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureSqlDatabase** exclui um banco de dados SQL do Azure por contexto de conexão do servidor ou nome do servidor.
Você pode criar um contexto de conexão do servidor de banco de dados SQL do Azure usando o cmdlet **New-AzureSqlDatabaseServerContext** e, em seguida, usá-lo com este cmdlet.

Quando você exclui um banco de dados especificando um nome de servidor de banco de dados SQL do Azure, o cmdlet **Remove-AzureSqlDatabase** usa o nome e as informações de assinatura atuais do Azure para executar a operação.

## EXEMPLOS

### Exemplo 1: remover um banco de dados
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Esse comando Remove o banco de dados chamado Database01 do contexto de conexão do servidor de banco de dados SQL do Azure $Context.

### Exemplo 2: remover um banco de dados usando um nome de servidor
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Esse comando Remove o banco de dados chamado Database01 do servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.

### Exemplo 3: remover um banco de dados usando o pipeline
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Este exemplo demonstra o método alternativo para passar o objeto de banco de dados pelo pipeline.

## OS

### -ConnectionContext
Especifica o contexto de conexão de um servidor do qual esse cmdlet Remove um banco de dados.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Banco de dados
Especifica um objeto que representa o banco de dados que este cmdlet Remove.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do banco de dados que este cmdlet Remove.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Permite a conclusão da ação sem solicitar confirmação ao usuário.

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
Especifica o nome do servidor em que esse cmdlet exclui o banco de dados.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## EXIBE

## INFORMA
* Por causa da severidade da operação, por padrão, esse cmdlet solicita confirmação. Para ignorar a confirmação, especifique o parâmetro *Force* .

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Excluir banco de dados](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


