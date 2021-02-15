---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113719"
---
# Set-AzSqlDatabaseDataMaskingRule

## Sinopse
Define as propriedades de uma regra de mascaramento de dados para um banco de dados.

## Sintaxe

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzSqlDatabaseDataMaskingRule** define uma regra de mascaramento de dados para um banco de dados SQL do Azure.
Para usar o cmdlet, forneça os parâmetros *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* para identificar a regra.
Você pode fornecer qualquer um dos parâmetros *de SchemaName,* *TableName* e *ColumnName* para retarget a regra.
*Especifique o parâmetro MascararFunção* para modificar como os dados são máscaras.
Se você especificar um valor de Número ou Texto para *MascararFunção,* poderá especificar os parâmetros *NumberFrom* e *NumberTo* para mascaramento de número ou os parâmetros *PrefixSize,* *ReplacementString* e *SuffixSize* para mascaramento de texto.
Se o comando for bem-sucedido e se você especificar o parâmetro *PassThru,* o cmdlet retornará um objeto que descreva as propriedades da regra de mascaramento de dados e os identificadores de regra.
Os identificadores de regra incluem, mas não estão limitados a, **ResourceGroupName,** **ServerName,** **DatabaseName** e **RuleId.**
Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.

## Exemplos

### Exemplo 1: alterar o intervalo de uma regra de mascaramento de dados em um banco de dados
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Esse comando modifica uma regra de mascaramento de dados que tem a Regra de ID17.
Essa regra opera no banco de dados chamado Database01 no servidor Server01.
Esse comando altera os limites do intervalo no qual um número aleatório é gerado como o valor mascarado.
O novo intervalo está entre 23 e 42.

### Exemplo 2

Define as propriedades de uma regra de mascaramento de dados para um banco de dados. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## Parâmetros

### -Nomeda Coluna
Especifica o nome da coluna direcionada pela regra de mascaramento.

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

### -Nomedo Banco de Dados
Especifica o nome do banco de dados.

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

### -MascararFunção
Especifica a função de mascaramento que a regra usa.
Os valores aceitáveis para este parâmetro são:
- Padrão
- NoMasking
- Texto
- Número
- SocialSecurityNumber
- CreditCardNumber
- Email O valor padrão é Padrão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Especifica o número de limite inferior do intervalo a partir do qual um valor aleatório é selecionado.
Especifique esse parâmetro somente se você especificar um valor de Número para *o parâmetro MascaramentoFuncional.*
O valor padrão é 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Especifica o número de limite superior do intervalo a partir do qual um valor aleatório é selecionado.
Especifique esse parâmetro somente se você especificar um valor de Número para *o parâmetro MascaramentoFuncional.*
O valor padrão é 0.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -PrefixSize
Especifica o número de caracteres no início do texto que não estão mascarados.
Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*
O valor padrão é 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
Especifica o número de caracteres no final do texto que não estão mascarados.
Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*
O valor padrão é 0.

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

### -SchemaName
Especifica o nome de um esquema.

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

### -SufixoSize
Especifica o número de caracteres no final do texto que não estão mascarados.
Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*
O valor padrão é 0.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomeda Tabela
Especifica o nome da tabela de banco de dados que contém a coluna mascarada.

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

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## Saídas

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel

## Notas

## LINKS RELACIONADOS

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[New-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


