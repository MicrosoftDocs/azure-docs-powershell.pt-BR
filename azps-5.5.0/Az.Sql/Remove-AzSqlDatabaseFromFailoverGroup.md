---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115731"
---
# Remove-AzSqlDatabaseFromFailoverGroup

## Sinopse
Remove um ou mais bancos de dados de um Grupo failover de banco de dados SQL do Azure.

## Sintaxe

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
Remove um ou mais bancos de dados do Grupo de Failover de Banco de Dados SQL do Azure especificado. Os bancos de dados e as relações de replicação são deixados intactos, mas não estarão mais acessíveis por meio dos pontos de extremidade do Grupo de Failover.
Para obter objetos de banco de dados com os quais preencher o parâmetro "-Banco de Dados", use (por exemplo) o cmdlet Get-AzSqlDatabase dados.
O servidor principal do Grupo de Failover deve ser usado para executar o comando.

## Exemplos

### Exemplo 1
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

Esse comando remove um banco de dados de um Grupo de Failover ao insucesá-lo.

### Exemplo 2
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

Esse comando remove todos os bancos de dados de um Grupo de Failover.

### Exemplo 3
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

Esse comando remove todos os bancos de dados em um Pool Elástica de um Grupo de Failover.

## Parâmetros

### -Banco de dados
Um ou mais bancos de dados SQL do Azure no servidor principal do Grupo de Failover a serem removidos do Grupo de Failover.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
O nome do Grupo failover de banco de dados SQL do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Forçar
Ignorar a mensagem de confirmação para executar a ação.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ServerName
O nome do servidor de banco de dados SQL principal do Azure do Grupo failover.

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### System.Collections.Generic.List'1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]

## Saídas

### Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel

## Notas

## LINKS RELACIONADOS

[New-AzSqlDatabaseFailoverGroup](./New-AzSqlDatabaseFailoverGroup.md)

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[Add-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[Switch-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
