---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405611"
---
# Stop-AzureSqlDatabaseCopy

## Sinopse
Termina uma relação de cópia contínua.

## Sintaxe

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Stop-AzureSqlDatabaseCopy** termina uma relação de cópia contínua.
Esse cmdlet interrompe o movimento de dados entre o banco de dados de origem e o banco de dados secundário ou de destino e altera o estado do banco de dados secundário para ser um banco de dados online autônomo.

Há duas maneiras de encerrar uma relação de cópia contínua, rescisão ou rescisão planejada e rescisão forçada com possível perda de dados.
No servidor que hospeda o banco de dados de origem, você pode executar esse cmdlet no modo de rescisão ou rescisão forçada.
No servidor que hospeda o banco de dados secundário, você deve usar o modo de rescisão forçada.

Uma rescisão planejada espera até que todas as transações comprometidas no banco de dados de origem, no momento em que você executar o cmdlet, tenham sido replicadas para o banco de dados secundário.
A rescisão forçada não espera a replicação de quaisquer transações pendentes comprometidas e pode causar uma possível perda de dados no banco de dados secundário.

Embora o status de replicação seja PENDENTE, somente a rescisão forçada pode encerrar com êxito uma relação de cópia contínua.
Se o status de replicação estiver PENDENTE, não há suporte para rescisão forçada.

## Exemplos

### Exemplo 1: Encerrar uma relação de cópia contínua
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Esse comando encerra a relação de cópia contínua do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.
O servidor chamado bk0b8kf658 hospeda o banco de dados secundário.

### Exemplo 2: encerrar uma relação de cópia contínua
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

O primeiro comando obtém a relação de cópia de banco de dados do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.

O segundo comando encerrará uma relação de cópia contínua do servidor que hospeda o banco de dados secundário.

## Parâmetros

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL do Azure de origem.
Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Especifica um objeto que representa um banco de dados.
Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.
Este parâmetro aceita a entrada de pipeline.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nomedo Banco de Dados
Especifica o nome de um banco de dados.
Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Forçar
Força o comando a ser executado sem pedir confirmação do usuário.

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

### -ForcedTermination
Indica que esse cmdlet causa rescisão forçada da relação de cópia contínua.
A rescisão forçada pode causar perda de dados.
Para executar esse cmdlet em um servidor que hospeda o banco de dados de destino, você deve especificar esse parâmetro.
Para executar esse cmdlet em um servidor que hospeda o banco de dados de origem, se o banco de dados secundário não estiver disponível, especifique esse parâmetro.

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

### -PartnerDatabase
Especifica o nome do banco de dados secundário.
Se você especificar um nome, ele deverá corresponder ao nome do banco de dados de origem.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Especifica o nome do servidor que hospeda o banco de dados de destino.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet é lido.
Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Especifica o nome do servidor no qual o banco de dados de origem reside.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## Saídas

### Nenhum

## Notas
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para ver um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet **New-AzureSqlDatabaseServerContext.**
* Restrições: no servidor que hospeda o banco de dados secundário, há suporte apenas para rescisão forçada.
* Impacto da rescisão no antigo banco de dados secundário: após a rescisão, o banco de dados secundário torna-se um banco de dados independente. Se a semeação já tiver sido concluída no banco de dados secundário, após a rescisão, esse banco de dados será aberto para acesso total. Se o banco de dados de origem for um banco de dados de leitura-gravação, o antigo banco de dados secundário também se tornará um banco de dados de leitura-gravação.

  Se o semeamento estiver em andamento, a semeação será cancelada e o antigo banco de dados secundário nunca ficará visível no servidor que hospeda o banco de dados secundário.

* Você pode definir o banco de dados de origem para o modo somente leitura. Isso garante que os bancos de dados de origem e secundários sejam sincronizados após a rescisão e garante que nenhuma transação seja comprometida durante a rescisão. Quando a rescisão terminar, de definir a origem de volta para o modo de leitura e gravação. Opcionalmente, você também pode definir o antigo banco de dados secundário para o modo de leitura-gravação.
* Monitoramento: para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation.**

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Parar Cópia do Banco de Dados](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


