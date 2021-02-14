---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110962"
---
# Get-AzSqlDatabaseGeoBackup

## Sinopse
Obtém um backup geo-redundante de um banco de dados.

## Sintaxe

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzSqlDatabaseGeoBackup** obtém um backup especificado de redundância geográfica de um banco de dados SQL ou todos os backups disponíveis de redundância geográfica em um servidor especificado.
Um backup redundante geográfico é um recurso restaurável usando arquivos de dados de uma localização geográfica separada.
Você pode usar Geo-Restore para restaurar um backup geo redundante em caso de uma paralisação regional para recuperar seu banco de dados em uma nova região.
Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.

## Exemplos

### Exemplo 1: Obter todos os backups geo redundantes em um servidor
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Esse comando obtém todos os backups geo redundantes disponíveis em um servidor especificado.

### Exemplo 2: Obter um backup geo redundante especificado
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Esse comando obtém o backup geo redundante do banco de dados chamado ContosoDatabase.

### Exemplo 3: Obter todos os backups geo redundantes em um servidor usando filtragem
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Esse comando obtém todos os backups geo redundantes disponíveis em um servidor especificado que começa com "Contoso".

## Parâmetros

### -Nomedo Banco de Dados
Especifica o nome do banco de dados a ser obter.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o servidor de banco de dados SQL está atribuído.

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
Especifica o nome do servidor que hospeda o backup a ser restaurado.

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
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

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

## Saídas

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel

## Notas

## LINKS RELACIONADOS

[Visão geral: continuidade de negócios na nuvem e recuperação de desastres de banco de dados com o banco de dados SQL](http://go.microsoft.com/fwlink/?LinkId=746881)

[Recuperar um banco de dados SQL do Azure de uma paralisação](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
