---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774248"
---
# Get-AzsSubscriptionsQuota

## Sinopse
Obtenha a lista de cotas do provedor de recursos de assinatura em um local.

## SYNTAX

### Lista (padrão)
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### Obter
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Obter a lista de cotas em um local.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsSubscriptionsQuota
```

Obtenha a lista de cotas do provedor de recursos de assinatura em um local.

## OS

### -Local
O local do AzureStack.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome da cota.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. subscriptions. admin. Models. quota

## INFORMA

## LINKS RELACIONADOS

