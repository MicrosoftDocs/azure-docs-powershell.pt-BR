---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945571"
---
# Get-AzureSqlDatabaseServer

## Sinopse
Obtém informações sobre os servidores de banco de dados SQL do Azure.

## SYNTAX

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseServer** Obtém informações sobre as instâncias do servidor de banco de dados SQL do Azure na assinatura atual.
Se você especificar um servidor por nome, esse cmdlet retornará um objeto que contém informações sobre esse servidor.
Caso contrário, o cmdlet retorna informações sobre todos os servidores.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os servidores
```
PS C:\> Get-AzureSqlDatabaseServer
```

Esse comando retorna informações sobre todas as instâncias do servidor de banco de dados SQL do Azure na assinatura atual.

### Exemplo 2: obter informações sobre um servidor específico
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Esse comando retorna informações sobre o servidor chamado lpqd0zbr8y.

## OS

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
Especifica o nome do servidor que este cmdlet Remove.
Especifique o nome do servidor, não o nome DNS totalmente qualificado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext

## EXIBE

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Servidores de lista](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


