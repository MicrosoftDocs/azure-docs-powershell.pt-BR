---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610798"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## Sinopse
Obtém os detalhes de uma regra de autorização de namespace Eventubs ou obtém uma lista de regras de autorização.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## DESCRITIVO
O cmdlet Get-AzureRmEventHubNamespaceAuthorizationRule Obtém os detalhes de uma regra de autorização de namespace de hubs de eventos especificada ou uma lista de regras de autorização de namespace.
Se o nome da regra de autorização for fornecido, os detalhes de uma única regra de autorização serão retornados.
Se um nome de regra de autorização não for fornecido, uma lista de todas as regras de autorização no namespace será retornada.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Retorna a regra de autorização \` MyAuthRuleName \` no namespace de hubs de eventos \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .

### Exemplo 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Retorna a regra de autorização padrão \` RootManageSharedAccessKey \` no namespace de hubs de eventos \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .

### Exemplo 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Retorna todas as regras de autorização no namespace de hubs de evento \` Mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .

## OS

### -AuthorizationRuleName
O nome da regra de autorização do namespace de hubs de eventos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

