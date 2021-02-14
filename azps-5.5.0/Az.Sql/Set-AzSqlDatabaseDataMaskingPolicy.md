---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110908"
---
# Set-AzSqlDatabaseDataMaskingPolicy

## Sinopse
Define o mascaramento de dados para um banco de dados.

## Sintaxe

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzSqlDatabaseDataMaskingPolicy** define a política de mascaramento de dados para um banco de dados SQL do Azure.
Para usar esse cmdlet, use os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.
Você pode definir o parâmetro *DataMaskingState* para especificar se as operações de mascaramento de dados estão habilitadas ou desabilitadas.
Se o cmdlet for bem-sucedido e o parâmetro *PassThru* for usado, retornará um objeto que descreve a política de mascaramento de dados atual, além dos identificadores de banco de dados.
Os identificadores de banco de dados incluem, mas não estão limitados a, **ResourceGroupName,** **ServerName** e **DatabaseName.**
Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.

## Exemplos

### Exemplo 1: Definir a política de mascaramento de dados para um banco de dados
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

Esse comando define a política de mascaramento de dados para um banco de dados chamado banco de dados01 no servidor chamado servidor01.

## Parâmetros

### -Nomedo Banco de Dados
Especifica o nome do banco de dados onde a política está definida.

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

### -DataMaskingState
Especifica se a operação de mascaramento de dados está habilitada ou desabilitada.
Os valores aceitáveis para este parâmetro são:
- Habilitado
- Desabilitado O valor padrão está habilitado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
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

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera saída.

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

### -PrivilegedUsers
Especifica uma lista separada por ponto e vírgula de IDs de usuário privilegiados.
Esses usuários têm permissão para exibir os dados de mascaramento.

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
Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.

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
Especifica o nome do servidor que hospeda o banco de dados.

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

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel

## Notas

## LINKS RELACIONADOS

[Get-AzSqlDatabaseDataMaskingPolicy](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[New-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Set-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


