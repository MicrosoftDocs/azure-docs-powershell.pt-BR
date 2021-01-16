---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260113"
---
# Stop-AzSqlDatabaseActivity

## Sinopse
Cancela a operação de atualizações assíncronas no banco de dados.

## SYNTAX

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzSqlDatabaseActivity** cancela a operação de atualizações assíncronas no banco de dados.

## EXEMPLOS

### Exemplo 1: cancelar a operação de atualizações assíncronas no banco de dados
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

Esse comando cancela a operação de atualizações assíncronas no banco de dados.

## OS

### -DatabaseName
Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -ElasticPoolName
O nome do pool elástico do SQL do Azure.

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

### -OperationId
Especifica a ID da operação que este cmdlet obtém.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.

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
Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.

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

### System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## EXIBE

### Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel

## INFORMA

## LINKS RELACIONADOS
