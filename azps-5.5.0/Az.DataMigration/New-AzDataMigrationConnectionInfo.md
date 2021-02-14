---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110985"
---
# New-AzDataMigrationConnectionInfo

## Sinopse
Cria um novo objeto Informações de Conexão especificando o tipo e o nome do servidor para conexão.

## Sintaxe

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O New-AzDataMigrationConnectionInfo cmdlet cria um novo objeto Informações de Conexão especificando o tipo de servidor para conexão. 

## Exemplos

### Exemplo 1
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

O exemplo anterior cria um novo objeto Informações de Conexão que fornece SQL como parâmetro ServerType.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -ServerType
Número que descreve o tipo de servidor ao qual se conectar. Atualmente, os valores com suporte são SQL para SQL Server, Instância Gerenciada do Azure SQL, MongoDb, SqlDb e Banco de Dados SQL do Azure. 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo

## Notas

## LINKS RELACIONADOS
