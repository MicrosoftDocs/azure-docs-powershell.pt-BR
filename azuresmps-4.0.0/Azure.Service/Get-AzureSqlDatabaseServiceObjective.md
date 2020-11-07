---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945568"
---
# Get-AzureSqlDatabaseServiceObjective

## Sinopse
Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.

## SYNTAX

### ByConnectionContext (padrão)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseServiceObjective** Obtém objetivos de serviço para um servidor de banco de dados SQL do Azure.
Os objetivos do serviço são chamados de níveis de desempenho.
Se você não especificar um objetivo de serviço, esse cmdlet retornará todos os objetivos de serviço válidos para o servidor especificado.

Este cmdlet se aplica a camadas de serviço básicas, padrão e Premium.

## EXEMPLOS

### Exemplo 1: obter todos os objetivos do serviço usando um contexto de conexão
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Esse comando obtém todos os objetivos de serviço do servidor que o contexto de conexão $Context especifica.

### Exemplo 2: obter todos os objetivos do serviço usando um nome de servidor
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Esse comando obtém todos os objetivos de serviço do servidor chamado Server01.

## OS

### -Contexto
Especifica o contexto de conexão de um servidor.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Especifica o nome de um servidor.

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
Especifica um objeto que representa o objetivo do serviço que esse cmdlet obtém.
Os valores válidos são: 

- Básico: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Padrão (S0): f1173c43-91bd-4AAA-973C-54e79e15235b
- Padrão (S1): 1b1ebd4d-D903-4baa-97f9-4ea675f5e928
- Padrão (S2): 455330e1-00CD-488b-b5fa-177c226f28b7
- * Padrão (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-B252-925be0a19446

* Padrão (S3) é parte da atualização de banco de dados do SQL V12 (prévia) mais recente.
Para obter mais informações, consulte o [que há de novo no Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) na biblioteca do Azure.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Imobjecname
Especifica o nome de um objetivo de serviço a obter.
Os valores válidos são: Basic, S0, S1, S2, S3, P1, P2 e P3.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. FileObject

## EXIBE

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Obter objetivo do nível de serviço](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


