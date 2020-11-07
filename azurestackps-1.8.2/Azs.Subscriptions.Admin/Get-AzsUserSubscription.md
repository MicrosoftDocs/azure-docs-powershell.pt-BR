---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946985"
---
# Get-AzsUserSubscription

## Sinopse
Obter a lista de assinaturas de usuários como administrador.

## SYNTAX

### Lista (padrão)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Obter
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## DESCRITIVO
Obter a lista de assinaturas de usuários como administrador.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsUserSubscription
```

Obter a lista de assinaturas de usuários como administrador.

## OS

### -Filtro
Parâmetro de filtro OData.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Parâmetro ID da assinatura.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription

## INFORMA

## LINKS RELACIONADOS

