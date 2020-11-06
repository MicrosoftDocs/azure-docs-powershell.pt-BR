---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427933"
---
# Set-AzureRmEventHubNamespace

## Sinopse
Atualiza o namespace de hubs de eventos especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### NamespaceParameterSet (padrão)
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### AutoInflateParameterSet
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## DESCRITIVO
O cmdlet Set-AzureRmEventHubNamespace atualiza as propriedades do namespace de hubs de eventos especificado.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

Atualiza o estado do namespace \` Mynamespacename \` a ser criado.

### Exemplo 2
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

Atualiza o estado do namespace \` Mynamespacename \` com autoinflate = Enabled e MaximumThroughputUnits = 10

## OS

### -Local
Localização geográfica do namespace dos hubs de eventos.

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

### -SkuCapacity
As unidades de produtividade do hub de eventos.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Nome SKU do namespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Estado
Especifica o estado (desabilitado ou habilitado) do namespace.

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Hashtables que representam marcas de recursos.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoInflate
Indica se o autoinflar está habilitado

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumThroughputUnits
Limite superior de unidades de produtividade quando o autoinflar está habilitado, o vaule deve estar dentro de 0 a 20 unidades de produtividade.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do namespace do EventHub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## SENSORES

### System. String

### System. Int32

### Microsoft. Azure. Management. EventHub. Models. Namespacestate

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. EventHub. Models. Namespaceattributes

## INFORMA

## LINKS RELACIONADOS

