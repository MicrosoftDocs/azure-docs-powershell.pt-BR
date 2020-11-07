---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945570"
---
# Get-AzureSqlDatabaseServerQuota

## Sinopse
Obtém informações de cota para um servidor de banco de dados SQL do Azure.

## SYNTAX

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseServerQuota** Obtém as informações de cota de uma instância especificada do servidor de banco de dados SQL do Azure.
Especifique um contexto de conexão ou o nome do servidor.
Se você não especificar um nome de cota, esse cmdlet obtém todas as informações de cota do servidor.

## EXEMPLOS

### Exemplo 1: obter informações para uma cota específica
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

Esse comando obtém a cota chamada Premium_Databases do servidor de banco de dados SQL do Azure especificado pela conexão armazenada na variável $Context.

### Exemplo 2: obter informações para todas as cotas
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

Esse comando obtém todos os valores de cota do servidor especificado pela $Context de conexão.

## OS

### -ConnectionContext
Especifica o contexto de conexão de um servidor.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

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

### -Quotaname
Especifica o nome do valor de cota que este cmdlet obtém.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServerQuota []

## INFORMA
* Autenticação: esse cmdlet pode usar a autenticação do SQL Server ou da autenticação baseada em certificados. Para obter exemplos de como configurar a autenticação, consulte o cmdlet New-AzureSqlDatabaseServerContext.

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


