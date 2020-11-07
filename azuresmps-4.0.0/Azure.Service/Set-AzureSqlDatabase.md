---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945865"
---
# Set-AzureSqlDatabase

## Sinopse
Define propriedades para um banco de dados SQL do Azure.

## SYNTAX

### ByNameWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureSqlDatabase** define propriedades para um banco de dados SQL do Azure.
Você pode especificar o banco de dados por nome ou passar um objeto do banco de dados SQL do Azure pelo pipeline.
Você pode especificar o servidor por nome ou passar um contexto de conexão do servidor de banco de dados SQL do Azure.
Crie um contexto de conexão executando o cmdlet **New-AzureSqlDatabaseServerContext** .
Se você especificar o servidor por nome, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação.

## EXEMPLOS

### Exemplo 1: alterar o tamanho de um banco de dados usando um contexto de conexão
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

Este exemplo altera o tamanho do banco de dados chamado Database01 para 20 GB, no contexto de conexão do servidor de banco de dados SQL do Azure $Context.

### Exemplo 2: alterar o tamanho de um banco de dados usando um nome de servidor
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

Este exemplo altera o tamanho do banco de dados chamado Database01 para 20 GB no servidor chamado lpqd0zbr8y.

## OS

### -ConnectionContext
Especifica o contexto de conexão de um servidor.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Banco de dados
Especifica um objeto que representa o banco de dados SQL do Azure que esse cmdlet modifica.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do banco de dados que este cmdlet modifica.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edição
Especifica a nova edição para o banco de dados SQL do Azure.
Os valores válidos são: 

- Nenhuma
- Pela
- Empresarial
- Basic
- Oficial
-  Gratifica

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Permite a conclusão da ação sem solicitar confirmação.

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

### -MaxSizeBytes
Especifica o novo tamanho máximo para o banco de dados em bytes.
Você pode especificar esse parâmetro ou o parâmetro *MaxSizeGB* .
Consulte o parâmetro *MaxSizeGB* para obter valores aceitáveis com base na edição.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Especifica o novo tamanho máximo para o banco de dados em gigabytes.
Você pode especificar esse parâmetro ou o parâmetro *MaxSizeBytes* .
Os valores aceitáveis são diferentes de acordo com a edição.

Valores básicos da edição: 1 ou 2

Valores de edição padrão: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 ou 250

Valores da edição Premium: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 ou 500

Valores da edição da Web: 1 ou 5

Valores da edição para empresas: 10, 20, 30, 40, 50, 100 ou 150

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewDatabaseName
Especifica o novo nome do banco de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Retorna o banco de dados SQL do Azure atualizado.

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
Especifica o nome do servidor que contém o banco de dados que esse cmdlet modifica.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Missão-objeto
Especifica um objeto que representa o novo objetivo de serviço (nível de desempenho) para esse banco de dados.
Os valores válidos são: 

- Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b
- Padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928
- Padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7
- * Padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446

* Padrão (S3) é parte da atualização de banco de dados do SQL V12 (prévia) mais recente.
Para obter mais informações, consulte o que há de novo na visualização do SQL banco de dados do Azure V12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sincronizar
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Atualizar banco de dados](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


