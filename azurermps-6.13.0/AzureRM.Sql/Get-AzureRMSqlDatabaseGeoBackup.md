---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: f22730e39a1b53cfea8181163dd770c67dc598a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429315"
---
# Get-AzureRmSqlDatabaseGeoBackup

## Sinopse
Obtém um backup de um banco de dados com redundância geográfica.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRMSqlDatabaseGeoBackup** Obtém um backup de redundância geográfica especificado de um banco de dados SQL ou todos os backups com redundância geográfica disponíveis em um servidor especificado.
Um backup com redundância geográfica é um recurso recuperável que usa arquivos de dados de uma localização geográfica separada.
Você pode usar Geo-Restore para restaurar um backup com redundância geográfica em caso de falha regional para recuperar seu banco de dados em uma nova região.
Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.

## EXEMPLOS

### Exemplo 1: obter todos os backups com redundância geográfica em um servidor
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Esse comando obtém todos os backups com redundância geográfica disponíveis em um servidor especificado.

### Exemplo 2: obter um backup de redundância geográfica especificado
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Esse comando obtém o backup com redundância geográfica de banco de dados chamado ContosoDatabase.

## OS

### -DatabaseName
Especifica o nome do banco de dados a ser obtido.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o servidor de banco de dados SQL está atribuído.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que hospeda o backup a ser restaurado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseGeoBackupModel

## INFORMA

## LINKS RELACIONADOS

[Visão geral: continuidade de negócios em nuvem e recuperação de desastres do banco de dados com SQL](https://go.microsoft.com/fwlink/?LinkId=746881)

[Recuperar um banco de dados SQL do Azure de uma interrupção](https://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
