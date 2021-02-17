---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413057"
---
# Start-AzureSqlDatabaseCopy

## Sinopse
Inicia uma operação de cópia de um banco de dados SQL do Azure.

## Sintaxe

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

## Descrição
O cmdlet **Start-AzureSqlDatabaseCopy** inicia uma operação de cópia única ou uma operação de cópia contínua de um banco de dados SQL específico do Azure.
Este cmdlet não é transacional.

O banco de dados original é o banco de dados de origem.
A cópia é o banco de dados secundário ou de destino.
Para uma cópia contínua, os bancos de dados de origem e de destino não podem residir no mesmo servidor, e os servidores que hospedam os bancos de dados de origem e de destino devem fazer parte da mesma assinatura.

Se você não especificar o parâmetro *ContinuousCopy,* esse cmdlet criará uma cópia única do banco de dados de origem.
Quando a resposta for recebida, a operação ainda poderá estar em andamento.
Você pode monitorar a operação usando o Get-AzureSqlDatabaseCopy ou Get-AzureSqlDatabaseOperation cmdlet.

Se você especificar *ContinuousCopy,* este cmdlet criará uma cópia contínua do banco de dados de origem.
Quando a resposta for recebida, a operação estará em andamento.
Você pode monitorar a operação usando **Get-AzureSqlDatabaseCopy** ou **Get-AzureSqlDatabaseOperation.**

Você pode criar uma cópia contínua como um banco de dados online ou offline.
A cópia contínua online é usada para configurar o Active Geo-Replication para o banco de dados SQL do https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Azure.
A cópia contínua offline é usada para configurar o Geo-Replication padrão para o banco de dados SQL do https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Azure.

## Exemplos

### Exemplo 1: Agendar uma cópia contínua do banco de dados
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Esse comando agenda uma cópia contínua do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.
O comando cria um banco de dados de destino no servidor chamado bk0b8kf658.

### Exemplo 2: Criar uma cópia única no mesmo servidor
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Esse comando cria uma cópia única do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.
O comando cria uma cópia chamada OrdersCopy no mesmo servidor.

### Exemplo 3: Agendar uma cópia contínua do banco de dados offline
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Esse comando agenda uma cópia contínua do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.
Esse comando cria um banco de dados de destino offline no servidor chamado bk0b8kf658.

## Parâmetros

### -ContinuousCopy
Indica que a cópia do banco de dados será uma cópia contínua (um banco de dados de réplica).
A cópia contínua não tem suporte no mesmo servidor.
Se esse parâmetro não for especificado, uma cópia única será executada.
Para uma cópia única, os bancos de dados de origem e de parceiro devem estar no mesmo servidor.

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
Especifica um objeto que representa o banco de dados SQL do Azure de origem.
Este parâmetro aceita a entrada de pipeline.

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

### -Nomedo Banco de Dados
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

### -OfflineSecondary
Especifica que uma cópia contínua é uma cópia passiva em vez de uma cópia ativa.
Se o banco de dados de origem for um banco de dados de edição padrão, então esse parâmetro será necessário.
Se esse parâmetro for especificado, *o ContinuousCopy* também deverá ser especificado.

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
Se você especificar o parâmetro *ContinuousCopy,* o valor do *PartnerDatabase* deverá corresponder ao nome do banco de dados de origem.
Se você não especificar *a ContinuousCopy,* deverá especificar um nome para o banco de dados de destino, que pode ser diferente do nome do banco de dados de origem.

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
Esse servidor deve estar na mesma assinatura do Azure do servidor de banco de dados de origem.

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

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## Saídas

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## Notas
* Autenticação: esse cmdlet requer autenticação baseada em certificado. Para ver um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte New-AzureSqlDatabaseServerContext cmdlet.
* Monitoramento: para verificar o status de uma ou mais relações de cópia contínuas que estão ativas no servidor, use o cmdlet **Get-AzureSqlDatabaseCopy.** Para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation.**

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Iniciar Cópia do Banco de Dados](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


