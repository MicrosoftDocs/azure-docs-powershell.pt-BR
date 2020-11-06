---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427738"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## Sinopse
Define as propriedades de uma regra de máscara de dados para um banco de dados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSqlDatabaseDataMaskingRule** define uma regra de máscara de dados para um banco de dados SQL do Azure.
Para usar o cmdlet, forneça os parâmetros *ResourceGroupName* , *nome_do_servidor* , *DatabaseName* e *RuleId* para identificar a regra.
Você pode fornecer qualquer um dos parâmetros de *SchemaName* , *TableName* e *ColumnName* para redirecionar a regra.
Especifique o parâmetro *MaskingFunction* para modificar como os dados são mascarados.

Se você especificar um valor de número ou texto para *MaskingFunction* , poderá especificar os parâmetros *NumberFrom* e *numberto* para o mascaramento de número ou os parâmetros *PrefixSize* , *replaceString* e *SuffixSize* para o mascaramento de texto.
Se o comando for bem-sucedido e se você especificar o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve as propriedades da regra de máscara de dados e os identificadores de regra.
Os identificadores de regra incluem, entre outros, **ResourceGroupName** , **nome_do_servidor** , **DatabaseName** e **RuleId**.

Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.

## EXEMPLOS

### Exemplo 1: alterar o intervalo de uma regra de máscara de dados em um banco de dados
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Esse comando modifica uma regra de máscara de dados que tem a ID Rule17.
Essa regra opera no banco de dados chamado Database01 no servidor Server01.
Esse comando altera os limites do intervalo no qual um número aleatório é gerado como o valor mascarado.
O novo intervalo está entre 23 e 42.

## OS

### -ColumnName
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

### -DatabaseName
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

### -MaskingFunction
Especifica a função de mascaramento que a regra usa.
Os valores aceitáveis para esse parâmetro são:

- Assume
- Sem máscara
- Textos
- Tempo
- SocialSecurityNumber
- CreditCardNumber
- Email

O valor padrão é padrão.

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
Especifica o número limite inferior do intervalo no qual um valor aleatório é selecionado.
Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .
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

### -Numberto
Especifica o número de limite superior do intervalo no qual um valor aleatório é selecionado.
Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .
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
Por padrão, esse cmdlet não gera nenhuma saída.

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
Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .
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

### -Substitutostring
Especifica o número de caracteres no final do texto que não estão mascarados.
Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .
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

### -Nomedoservidor
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

### -SuffixSize
Especifica o número de caracteres no final do texto que não estão mascarados.
Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .
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

### -TableName
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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingRuleModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[New-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


