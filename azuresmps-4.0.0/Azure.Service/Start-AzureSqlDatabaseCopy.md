---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945845"
---
# Start-AzureSqlDatabaseCopy

## Sinopse
Inicia uma operação de cópia de um banco de dados SQL do Azure.

## SYNTAX

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureSqlDatabaseCopy** inicia uma operação única de cópia ou uma operação de cópia contínua de um banco de dados SQL específico do Azure.
Este cmdlet não é Transactional.

O banco de dados original é o banco de dados de origem.
A cópia é o banco de dados secundário ou de destino.
Para uma cópia contínua, os bancos de dados de origem e de destino não podem residir no mesmo servidor e os servidores que hospedam os bancos de dados de origem e de destino devem fazer parte da mesma assinatura.

Se você não especificar o parâmetro *ContinuousCopy* , esse cmdlet criará uma cópia única do banco de dados de origem.
Quando a resposta é recebida, a operação ainda pode estar em andamento.
Você pode monitorar a operação usando o cmdlet Get-AzureSqlDatabaseCopy ou Get-AzureSqlDatabaseOperation.

Se você especificar *ContinuousCopy* , esse cmdlet criará uma cópia contínua do banco de dados de origem.
Quando a resposta é recebida, a operação estará em andamento.
Você pode monitorar a operação usando **Get-AzureSqlDatabaseCopy** ou **Get-AzureSqlDatabaseOperation**.

Você pode criar uma cópia contínua como um banco de dados online ou offline.
A cópia contínua online é usada para configurar o Active Geo-Replication para o banco de dados SQL do Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
A cópia contínua offline é usada para configurar o Geo-Replication padrão para o banco de dados SQL do Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## EXEMPLOS

### Exemplo 1: agendar uma cópia contínua do banco de dados
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Esse comando agenda uma cópia contínua do banco de dados chamado Orders no servidor chamado lpqd0zbr8y.
O comando cria um banco de dados de destino no servidor chamado bk0b8kf658.

### Exemplo 2: criar uma cópia única no mesmo servidor
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Esse comando cria uma cópia única do banco de dados chamada Orders no servidor chamado lpqd0zbr8y.
O comando cria uma cópia chamada OrdersCopy no mesmo servidor.

### Exemplo 3: agendar uma cópia contínua do banco de dados offline
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Esse comando agenda uma cópia contínua do banco de dados chamado Orders no servidor chamado lpqd0zbr8y.
Esse comando cria um banco de dados de destino offline no servidor chamado bk0b8kf658.

## OS

### -ContinuousCopy
Indica que a cópia do banco de dados será uma cópia contínua (um banco de dados de réplica).
Não há suporte para cópia contínua no mesmo servidor.
Se esse parâmetro não for especificado, será executada uma cópia única.
Para uma cópia única, os bancos de dados de origem e parceiro devem estar no mesmo servidor.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL de origem do Azure.
Esse parâmetro aceita entrada de pipeline.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do banco de dados de origem.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
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

### -OfflineSecondary
Especifica que uma cópia contínua é uma cópia passiva em vez de uma cópia ativa.
Se o banco de dados de origem for um banco de dados de edição padrão, este parâmetro será necessário.
Se esse parâmetro for especificado, *ContinuousCopy* também deverá ser especificado.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Especifica o nome do banco de dados de destino.
Se você especificar o parâmetro *ContinuousCopy* , o valor de *PartnerDatabase* deverá coincidir com o nome do banco de dados de origem.
Se você não especificar *ContinuousCopy* , deverá especificar um nome para o banco de dados de destino, que pode ser diferente do nome do banco de dados de origem.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Especifica o nome do servidor que hospeda o banco de dados de destino.
Esse servidor deve estar na mesma assinatura do Azure que o servidor de banco de dados de origem.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

## INFORMA
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte New-AzureSqlDatabaseServerContext cmdlet.
* Monitoramento: para verificar o status de uma ou mais relações de cópia contínua ativas no servidor, use o cmdlet **Get-AzureSqlDatabaseCopy** . Para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation** .

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Iniciar cópia de banco de dados](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Cmdlets do banco de dados SQL do Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Parar-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


