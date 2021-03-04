---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888424"
---
# New-AzSqlDatabaseFailoverGroup

## SYNOPSIS
Este comando cria um novo Grupo de Failover SQL Banco de Dados do Azure.

## SINTAXE

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
Cria um novo Grupo SQL Failover de Banco de Dados do Azure para os servidores especificados.
Dois pontos de extremidade do Azure SQL Database TDS são criados em FailoverGroupName.SqlDatabaseDnsSuffix (por exemplo, FailoverGroupName.database.windows.net) e FailoverGroupName.secondary.SqlDatabaseDnsSuffix. Esses pontos de extremidade podem ser usados para se conectar aos servidores primários e secundários no Grupo de Failover, respectivamente. Se o servidor principal for afetado por uma interrupção, o failover automático dos pontos de extremidade e bancos de dados será acionado conforme ditado pela política de failover e o período de carência do Grupo de Failover.
Os Grupos de Failover recém-criados não contêm bancos de dados. Para controlar o conjunto de bancos de dados em um Grupo de Failover, use os cmdlets 'Add-AzSqlDatabaseToFailoverGroup' e 'Remove-AzSqlDatabaseFromFailoverGroup'.
Somente valores maiores ou iguais a 1 hora são suportados para o parâmetro '-GracePeriodWithDataLossHours'.

## EXEMPLOS

### Exemplo 1
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

Este comando cria um novo Grupo de Failover com a política de failover 'Automatic' para dois servidores no mesmo grupo de recursos.

### Exemplo 2
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

Este comando cria um novo Grupo de Failover com a política de failover 'Manual' para dois servidores em grupos de recursos diferentes.

## PARÂMETROS

### -AllowReadOnlyFailoverToPrimary
Se uma interrupção no servidor secundário deve disparar o failover automático do ponto de extremidade somente leitura. Esse recurso ainda não tem suporte.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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
O nome do Grupo de Failover do Banco de Dados do Azure SQL a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverPolicy
A política de failover do Grupo de Failover SQL Banco de Dados do Azure.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
Intervalo antes que o failover automático seja iniciado se ocorrer uma paralisação no servidor primário e o failover não puder ser concluído sem perda de dados.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
O nome do grupo de recursos secundário do Grupo de Failover de Banco de Dados do Azure SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServerName
O nome do servidor secundário do Grupo de Failover de Banco de Dados do Azure SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
O nome do Servidor de Banco de Dados do Azure SQL principal do Grupo de Failover.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel

## NOTES

## LINKS RELACIONADOS

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[Add-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[Remove-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[Switch-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL documentação do banco de dados](https://docs.microsoft.com/azure/sql-database/)
