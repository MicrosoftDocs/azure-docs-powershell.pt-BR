---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112282"
---
# New-AzDataMigrationDatabaseInfo

## Sinopse
Cria o objeto DatabaseInfo para o serviço de migração de banco de dados do Azure, que especifica a origem do banco de dados para migração.

## SYNTAX

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzDataMigrationDatabaseInfo cria o objeto DatabaseInfo que especifica a instância do banco de dados de origem a ser migrada. O nome do banco de dados é usado como parâmetro de entrada.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

O exemplo anterior cria um novo objeto DatabaseInfo para o banco de dados de origem **AdventureWorks2016**.
Esse script pressupõe que você já esteja conectado à sua conta do Azure. Você pode confirmar seu status de logon usando o cmdlet Get-AzSubscription.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Nome do banco de dados de origem.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Management. datamigration. Models. DatabaseInfo

## INFORMA

## LINKS RELACIONADOS
