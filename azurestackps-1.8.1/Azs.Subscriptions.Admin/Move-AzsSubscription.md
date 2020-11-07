---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774922"
---
# Move-AzsSubscription

## Sinopse
Mover assinaturas entre ofertas de provedor delegado.

## SYNTAX

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## DESCRITIVO
Mover assinaturas entre ofertas de provedor delegado.
Esse processo executará apenas uma remarcação, a oferta subjacente, planos, as cotas para as assinaturas não serão alteradas.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Move user subscriptions to a delegated provider offer.
```

Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

### --------------------------EXEMPLO 2--------------------------
```
Move user subscriptions from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1 '" | em que {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds

## OS

### -AsJob
Especifica se a operação de movimentação deve ser executada como um trabalho.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDelegatedProviderOffer
Especifica a oferta do provedor delegado totalmente qualificado na qual esse cmdlet Move assinaturas.
NULO se as assinaturas forem removidas para o provedor padrão.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Especifica uma matriz de identificadores de recursos de assinatura totalmente qualificados que esse cmdlet Move.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

