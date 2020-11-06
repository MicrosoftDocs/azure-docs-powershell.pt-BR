---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428704"
---
# Set-AzureRmSqlDatabaseDataMaskingPolicy

## Sinopse
Define o mascaramento de dados para um banco de dados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSqlDatabaseDataMaskingPolicy** define a política de máscara de dados de um banco de dados SQL do Azure.
Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.
Você pode definir o parâmetro *DataMaskingState* para especificar se as operações de máscara de dados estão habilitadas ou desabilitadas.

Você também pode definir o parâmetro *PrivilegedLogins* para especificar quais usuários têm permissão para ver os dados não mascarados.
Se o cmdlet for bem-sucedido e o parâmetro *PassThru* for usado, ele retornará um objeto que descreve a política de mascaramento de dados atual, além dos identificadores de banco de dados.
Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.

Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.

## EXEMPLOS

### Exemplo 1: definir a política de máscara de dados para um banco de dados
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

Esse comando define a política de máscara de dados para um banco de dados denominado database01 no servidor chamado Server01.

## OS

### -DatabaseName
Especifica o nome do banco de dados onde a política está definida.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataMaskingState
Especifica se a operação de máscara de dados está habilitada ou desabilitada.
Os valores aceitáveis para esse parâmetro são:

- Possibilita
- Ativo

O valor padrão é habilitado.

```yaml
Type: String
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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera nenhuma saída.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivilegedLogins
Especifica quais usuários do SQL são excluídos do mascaramento.

Esse parâmetro é preterido e será removido de versões futuras.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivilegedUsers
Especifica uma lista separada por ponto-e-vírgula de IDs de usuário privilegiadas.
Esses usuários têm permissão para exibir os dados de mascaramento.

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que hospeda o banco de dados.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingPolicyModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlDatabaseDataMaskingPolicy](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[New-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Set-AzureRmSqlDatabaseDataMaskingRule](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


