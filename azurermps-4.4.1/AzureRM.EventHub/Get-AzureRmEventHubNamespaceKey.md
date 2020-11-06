---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441092"
---
# Get-AzureRmEventHubNamespaceKey

## Sinopse
Obtém detalhes das chaves e connectionStrings primárias e secundárias da regra de autorização da regra de autorização de namespace dos hubs de eventos especificados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## DESCRITIVO
O cmdlet Get-AzureRmEventHubNamespaceKey retorna os connectionStrings primário e secundário e os detalhes de chaves da regra de autorização especificada no namespace de hubs de eventos fornecido.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Obtém detalhes das chaves e connectionStrings primárias e secundárias da regra de autorização \` MyAuthRuleName \` no namespace de hubs de evento \` mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .

## OS

### -AuthorizationRuleName
O nome da regra de autorização no namespace de hubs de eventos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
O nome do namespace dos hubs de eventos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes

## INFORMA

## LINKS RELACIONADOS

