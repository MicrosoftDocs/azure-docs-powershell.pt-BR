---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: 24941a301d0ffcc4e7219dc923fefcf1e007de99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110802"
---
# Get-AzSearchPrivateLinkResource

## Sinopse
Obtém detalhes do recurso de link privado para o serviço pesquisa cognitiva do Azure.

## Sintaxe

### ResourceNameParameterSet (Padrão)
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzSearchPrivateLinkResource** obtém detalhes do recurso de link privado para o serviço pesquisa cognitiva do Azure.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

O exemplo mostra como obter os detalhes do recurso de vínculo particular (no formato JSON para conveniência) para o serviço de Pesquisa Cognitiva do Azure.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -InputObject
Objeto de entrada do Serviço de Pesquisa Cognitiva do Azure.

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do Serviço de Pesquisa Cognitiva do Azure.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do Grupo de Recursos.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do Recurso de Serviço de Pesquisa Cognitiva do Azure.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource

## Notas

## LINKS RELACIONADOS

[New-AzSearchSharedPrivateLinkResource.md](./New-AzSearchSharedPrivateLinkResource.md)

[Get-AzSearchSharedPrivateLinkResource.md](./Get-AzSearchSharedPrivateLinkResource.md)

[Remove-AzSearchSharedPrivateLinkResource.md](./Remove-AzSearchSharedPrivateLinkResource.md)

[Set-AzSearchSharedPrivateLinkResource.md](./Set-AzSearchSharedPrivateLinkResource.md)