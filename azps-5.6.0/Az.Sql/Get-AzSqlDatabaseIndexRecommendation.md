---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 2205c241625f0bfdc2be21cda34c5bc3d6d07c12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901427"
---
# Get-AzSqlDatabaseIndexRecommendation

## SYNOPSIS
Obtém as operações de índice recomendadas para um servidor ou banco de dados.

## SINTAXE

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzSqlDatabaseIndexRecommendation obtém** as operações de índice recomendadas para um servidor ou banco de dados do Azure SQL Database.

## EXEMPLOS

### Exemplo 1: obter recomendações de índice para todos os bancos de dados no servidor
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Este comando retorna recomendações de índice para todos os bancos de dados no servidor server01.

### Exemplo 2: Obter recomendações de índice para um banco de dados específico
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Este comando retorna recomendações de índice para banco de dados específico.

### Exemplo 3: obter uma recomendação de índice único pelo nome
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

Este comando retorna a recomendação de índice único por nome.

## PARÂMETROS

### -DatabaseName
Especifica o nome do banco de dados para o qual este cmdlet obtém recomendações de índice.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -IndexRecommendationName
Especifica o nome da recomendação de índice que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos para o que o servidor é atribuído.
Este cmdlet obtém recomendações de índice para um banco de dados hospedado por esse servidor.

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
Especifica o servidor que hospeda o banco de dados para o qual este cmdlet obtém recomendações de índice.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
Especifica o nome de uma tabela SQL Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Sql.Model.IndexRecommendation

## NOTES

## LINKS RELACIONADOS

[Start-AzSqlDatabaseExecuteIndexRecommendation](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[Stop-AzSqlDatabaseExecuteIndexRecommendation](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
