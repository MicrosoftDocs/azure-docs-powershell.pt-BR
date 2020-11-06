---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432857"
---
# New-AzureRmSubscriptionDefinition

## Sinopse
Cria uma definição de assinatura.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Criar definição de assinatura
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## DESCRITIVO
O cmdlet **New-AzureRmSubscriptionDefinition** cria uma definição de assinatura.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

Cria uma definição de assinatura com um nome de exibição de assinatura padrão.

### Exemplo 2
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

Cria uma definição de assinatura com um nome de exibição de assinatura personalizado.

## OS

### -Nome
O nome da definição de assinatura a ser criada.

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

### -Offertype
O tipo de oferta a ser usado ao criar a assinatura subjacente.

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

### -SubscriptionDisplayName
O nome de exibição a ser usado ao criar a assinatura subjacente da definição de assinatura.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition

## INFORMA

## LINKS RELACIONADOS

