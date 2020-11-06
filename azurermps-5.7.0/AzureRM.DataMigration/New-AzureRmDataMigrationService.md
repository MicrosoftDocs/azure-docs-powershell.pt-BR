---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610399"
---
# New-AzureRmDataMigrationService

## Sinopse
Cria uma nova instância do serviço de migração de banco de dados do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## DESCRITIVO
O cmdlet New-AzureRmDataMigrationService cria uma nova instância do serviço de migração de banco de dados do Azure. Esse cmdlet usa o nome do grupo de recursos existente do Azure, o nome exclusivo da nova instância do serviço de migração de banco de dados do Azure a ser criada, a região em que a instância é provisionada, o nome da SKU do funcionário do DMS e o nome da sub-rede virtual do Azure em que o serviço está para residir. Não há nenhum parâmetro para o nome da assinatura porque ele é esperado para que o usuário especifique a assinatura padrão da sessão de logon do Azure ou execute Get-AzureRmSubscription-Subscriptionname "mysubscriptionname" | Select-AzureRmSubscription para selecionar outra assinatura.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

O exemplo acima mostra como criar uma nova instância do serviço de migração de banco de dados do Azure chamada TestService na região central dos EUA.


## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local da instância do serviço de migração do banco de dados do Azure a ser criada, que corresponde a uma região do Azure.

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

### -ResourceGroupName
O nome do grupo de recursos.

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

### -ServiceName
O nome da instância do serviço de migração do banco de dados do Azure.

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

### -SKU
A SKU da instância do serviço de migração do banco de dados do Azure. Atualmente, os valores possíveis são Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores

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

### -VirtualSubnetId
O nome da sub-rede na rede virtual especificada a ser usada para a instância do serviço de migração do banco de dados do Azure.

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




## EXIBE

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## INFORMA

## LINKS RELACIONADOS

