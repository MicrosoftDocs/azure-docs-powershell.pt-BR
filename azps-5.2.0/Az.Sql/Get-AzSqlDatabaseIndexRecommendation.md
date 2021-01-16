---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260469"
---
# Get-AzSqlDatabaseIndexRecommendation

## Sinopse
Obtém as operações de índice recomendadas para um servidor ou banco de dados.

## SYNTAX

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSqlDatabaseIndexRecommendation** Obtém as operações de índice recomendadas para um banco de dados ou um servidor de banco de dados SQL do Azure.

## EXEMPLOS

### Exemplo 1: obter recomendações de índice para todos os bancos de dados no servidor
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Esse comando retorna recomendações de índice para todos os bancos de dados no Server Server01.

### Exemplo 2: obter recomendações de índice para um banco de dados específico
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Esse comando retorna recomendações de índice para um banco de dados específico.

### Exemplo 3: obter uma única recomendação de índice por nome
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

Esse comando retorna a recomendação de índice único por nome.

## OS

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
Especifica o nome do grupo de recursos para o qual o servidor está atribuído.
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

### -Nomedoservidor
Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet obtém recomendações de índice.

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
Especifica o nome de uma tabela SQL do Azure.

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

### -Confirme
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. Model. IndexRecommendation

## INFORMA

## LINKS RELACIONADOS

[Start-AzSqlDatabaseExecuteIndexRecommendation](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[Parar-AzSqlDatabaseExecuteIndexRecommendation](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
