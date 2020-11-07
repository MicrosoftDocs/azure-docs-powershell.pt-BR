---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946403"
---
# Stop-AzureSqlDatabaseCopy

## Sinopse
Finaliza uma relação de cópia contínua.

## SYNTAX

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

## DESCRITIVO
O cmdlet **Stop-AzureSqlDatabaseCopy** Finaliza uma relação de cópia contínua.
Esse cmdlet interrompe a movimentação de dados entre o banco de dados de origem e o banco de dados secundário ou de destino e, em seguida, altera o estado do banco de dados secundário para ser um banco de dados online autônomo.

Há duas maneiras de finalizar uma relação de cópia contínua, rescisão ou término planejado e rescisão forçado com possível perda de dados.
No servidor que hospeda o banco de dados de origem, você pode executar esse cmdlet no modo de término ou de término forçado.
No servidor que hospeda o banco de dados secundário, você deve usar o modo de terminação forçado.

Uma conclusão planejada aguarda até todas as transações confirmadas no banco de dados de origem, no momento em que você executar o cmdlet, foram duplicadas para o banco de dados secundário.
A rescisão forçada não aguarda a replicação de nenhuma transação confirmada pendente e pode causar possível perda de dados no banco de dados secundário.

Embora o status de replicação esteja pendente, somente a terminação forçada pode encerrar com êxito uma relação de cópia contínua.
Se o status de replicação estiver pendente, a rescisão não forçada não será aceita.

## EXEMPLOS

### Exemplo 1: encerrar uma relação de cópia contínua
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Esse comando encerra a relação de cópia contínua do banco de dados chamado pedidos no servidor chamado lpqd0zbr8y.
O servidor chamado bk0b8kf658 hospeda o banco de dados secundário.

### Exemplo 2: finalizar forçosamente uma relação de cópia contínua
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

O primeiro comando obtém a relação de cópia de banco de dados para o banco de dados chamado Orders no servidor chamado lpqd0zbr8y.

O segundo comando finaliza forçosamente uma relação de cópia contínua do servidor que hospeda o banco de dados secundário.

## OS

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL de origem do Azure.
Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.

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
Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.
Esse parâmetro aceita entrada de pipeline.

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

### -DatabaseName
Especifica o nome de um banco de dados.
Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.

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

### -Force
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
Indica que esse cmdlet causa o encerramento forçado da relação de cópia contínua.
A rescisão forçada pode causar perda de dados.
Para executar esse cmdlet em um servidor que hospeda o banco de dados de destino, você deve especificar esse parâmetro.
Para executar esse cmdlet em um servidor que hospeda o banco de dados de origem, se o banco de dados secundário estiver indisponível, você deve especificar esse parâmetro.

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
Se você especificar um nome, ele deve corresponder ao nome do banco de dados de origem.

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
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -Nomedoservidor
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## EXIBE

### Nenhuma

## INFORMA
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet **New-AzureSqlDatabaseServerContext** .
* Restrições: no servidor que hospeda o banco de dados secundário, há suporte somente para encerramento forçado.
* Impacto da rescisão no antigo banco de dados secundário: após a rescisão, o banco de dados secundário se torna um banco de dados independente. Se a propagação já estiver concluída no banco de dados secundário, após o término, este banco de dados está aberto para acesso total. Se o banco de dados de origem for um banco de dados de leitura e gravação, o primeiro banco de dados secundário se tornará um banco de dados de leitura-gravação.

  Se a propagação estiver em andamento, a propagação será abortada, e o antigo banco de dados secundário nunca se tornará visível no servidor que hospeda o banco de dados secundário.

* Você pode definir o banco de dados de origem como modo somente leitura. Isso garante que os bancos de dados secundários e de origem sejam sincronizados após a rescisão e certifique-se de que nenhuma transação seja comprometida durante a rescisão. Quando o encerramento terminar, defina a fonte de volta para o modo de leitura-gravação. Opcionalmente, você também pode definir o antigo banco de dados secundário para o modo de leitura-gravação.
* Monitoramento: para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation** .

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Parar cópia do banco de dados](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Cmdlets do banco de dados SQL do Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


