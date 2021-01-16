---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271154"
---
# Get-AzSqlDatabaseFailoverGroup

## Sinopse
Obtém ou lista os grupos de failover do banco de dados SQL do Azure.

## SYNTAX

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Obtém um grupo específico de failover de banco de dados SQL do Azure ou lista os grupos de failover em um servidor.
Qualquer servidor no grupo de failover pode ser usado para executar o comando. Os valores retornados refletirão o estado do servidor especificado em relação ao grupo de failover.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

Lista todos os grupos de failover em um servidor.

### Exemplo 2
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

Obter um grupo específico de failover.

### Exemplo 3
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

Obtenha todos os grupos de failover em um servidor que comece com "FG".

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverGroupName
O nome do grupo de failover de banco de dados SQL do Azure a ser recuperado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
O nome do servidor de banco de dados SQL do Azure do qual recuperar o grupo de failover.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel

## INFORMA

## LINKS RELACIONADOS

[New-AzSqlDatabaseFailoverGroup](./New-AzSqlDatabaseFailoverGroup.md)

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[Add-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[Remove-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[Botão de AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
