---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425596"
---
# Get-AzsDelegatedProvider

## Sinopse
Obter a lista de delegatedProviders.

## SYNTAX

### Lista (padrão)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Obter
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## DESCRITIVO
Obter a lista de delegatedProviders.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsDelegatedProvider
```

Obter uma lista de provedores delegados.

### --------------------------EXEMPLO 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Obter um provedor delegado específico.

## OS

### -DelegatedProviderId
Identificador DelegatedProvider.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription

## INFORMA

## LINKS RELACIONADOS

