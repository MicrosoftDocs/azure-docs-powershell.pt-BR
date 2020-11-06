---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609812"
---
# Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry

## Sinopse
Obtém uma entrada na ACL de um catálogo ou item de catálogo na análise do data Lake.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### GetCatalogAclEntry (padrão)
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetCatalogAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntry
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** Obtém uma lista de entradas (ACEs) na lista de controle de acesso (ACL) de um catálogo ou item de catálogo na análise do data Lake.

## EXEMPLOS

### Exemplo 1: obter a ACL para um catálogo
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Esse comando obtém a ACL para o catálogo da conta do data Lake Analytics especificada

### Exemplo 2: obter a entrada ACL do proprietário do usuário para um catálogo
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Este comando obtém a entrada ACL do proprietário do usuário para o catálogo da conta do data Lake Analytics especificada

### Exemplo 3: obter a entrada ACL do proprietário do grupo para um catálogo
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Este comando obtém a entrada ACL do proprietário do grupo para o catálogo da conta do data Lake Analytics especificada

### Exemplo 4: obter a ACL para um banco de dados
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Este comando obtém a ACL para o banco de dados da conta do data Lake Analytics especificada

### Exemplo 5: obter a entrada ACL do proprietário de um usuário para um banco de dados
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Este comando obtém a entrada ACL do proprietário do usuário para o banco de dados da conta especificada do data Lake Analytics

### Exemplo 6: obter a entrada ACL do proprietário de um grupo para um banco de dados
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Esse comando obtém a entrada ACL do proprietário do grupo para o banco de dados da conta especificada do data Lake Analytics

## OS

### -Conta
Especifica o nome da conta do data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -GroupOwner
Obter entrada de ACL do catálogo para proprietário do grupo

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
Especifica o tipo de catálogo ou item (ns) de catálogo. Os valores aceitáveis para esse parâmetro são:
- Catálogo
- Base

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do data Lake Analytics de um catálogo ou item de catálogo.
As partes do caminho devem ser separadas por um ponto (.).

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Userowner
Obtenha a entrada ACL do catálogo para proprietário do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
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

### System. String

### Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance

## EXIBE

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl

## INFORMA

## LINKS RELACIONADOS

[O U-SQL agora oferece controle de acesso no nível do banco de dados](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
