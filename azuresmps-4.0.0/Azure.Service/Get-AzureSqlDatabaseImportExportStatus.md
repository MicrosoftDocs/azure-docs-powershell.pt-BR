---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946294"
---
# Get-AzureSqlDatabaseImportExportStatus

## Sinopse
Obtém o status de uma solicitação de importação ou exportação.

## SYNTAX

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSqlDatabaseImportExportStatus** Obtém o status de uma solicitação de importação ou exportação.
O cmdlet Start-AzureSqlDatabaseImport ou Start-AzureSqlDatabaseExport iniciar solicitações.
Você pode especificar o objeto de solicitação usando o parâmetro de *solicitação* ou pode identificar a solicitação usando o parâmetro *RequestId* e os parâmetros *username* , *password* e *nomedoservidor* .

## EXEMPLOS

### Exemplo 1: obter o status de uma solicitação de exportação
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

O primeiro comando cria uma solicitação de exportação e armazena-a na variável $ExportRequest.

O segundo comando obtém o status da solicitação de exportação armazenada em $ExportRequest.

## OS

### -Senha
Especifica a senha necessária para se conectar ao servidor do banco de dados SQL do Azure.
Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -Solicitação
Especifica um objeto **ImportExportRequest** .
Para obter um objeto de solicitação de importação ou exportação, use o cmdlet Start-AzureSqlDatabaseImport ou Start-AzureSqlDatabaseExport.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
Especifica o GUID da operação de importação ou de exportação para a qual esse cmdlet obtém o status.
Se você especificar esse parâmetro, você deve especificar os parâmetros *username* , *password* e *nomedoservidor* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor de banco de dados SQL do Azure.
Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Especifica o nome de usuário necessário para se conectar ao servidor do banco de dados SQL do Azure.
Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExport. StatusInfo

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Obter o status do banco de dados de exportação de importação](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


