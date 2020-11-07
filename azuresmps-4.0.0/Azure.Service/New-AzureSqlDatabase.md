---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945973"
---
# New-AzureSqlDatabase

## Sinopse
Cria um banco de dados SQL do Azure.

## SYNTAX

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSqlDatabase** cria um banco de dados SQL do Azure.
Você pode especificar o servidor usando um contexto de conexão de servidor de banco de dados SQL do Azure que você cria usando o cmdlet **New-AzureSqlDatabaseServerContext** .
Ou, se você especificar o nome do servidor, o cmdlet usará as informações atuais da assinatura do Azure para autenticar a solicitação de acesso ao servidor.

Quando você cria um novo banco de dados especificando um servidor de banco de dados SQL do Azure, o cmdlet **New-AzureSqlDatabase** cria um contexto de conexão temporário usando o nome do servidor especificado e as informações atuais da assinatura do Azure para executar a operação.

## EXEMPLOS

### Exemplo 1: criar um banco de dados
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Esse comando cria um banco de dados SQL do Azure chamado Database1, para o contexto de conexão do servidor do banco de dados SQL do Azure $Context.

### Exemplo 2: criar um banco de dados na assinatura atual
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Este exemplo cria um banco de dados chamado Database1, no servidor de banco de dados SQL do Azure especificado chamado lpqd0zbr8y.
O cmdlet usa as informações de assinatura atuais do Azure para autenticar a solicitação de acesso ao servidor.

## OS

### -Agrupamento
Especifica um agrupamento para o novo banco de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionContext
Especifica o contexto de conexão de um servidor em que esse cmdlet cria um banco de dados.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do novo banco de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edição
Especifica a edição para o novo banco de dados SQL do Azure.
Os valores válidos são: 

- Nenhuma
- Pela
- Empresarial
- Basic
- Oficial
-  Gratifica

O valor padrão é Web.

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
Permite a conclusão da ação sem solicitar confirmação ao usuário.

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
Especifica o tamanho máximo do banco de dados em bytes.
Você pode especificar esse parâmetro ou o parâmetro *MaxSizeGB* .
Consulte a descrição do parâmetro *MaxSizeGB* para obter os valores aceitáveis com base na edição.

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
Especifica o tamanho máximo do banco de dados em gigabytes.
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
Especifica o nome do servidor de banco de dados SQL do Azure que deve conter o novo banco de dados.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Missão-objeto
Especifica um objeto que representa o novo objetivo de serviço (nível de desempenho) deste banco de dados.
Esse valor representa o nível dos recursos atribuídos a esse banco de dados.
Os valores válidos são: 

Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928 padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7 * padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446

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

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## INFORMA
* Para excluir um banco de dados que foi criado por **New-AzureSqlDatabase** , use o cmdlet Remove-AzureSqlDatabase.

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Criar banco de dados](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


