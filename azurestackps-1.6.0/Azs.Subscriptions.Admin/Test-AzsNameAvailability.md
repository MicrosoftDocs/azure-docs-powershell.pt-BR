---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425861"
---
# Test-AzsNameAvailability

## Sinopse
Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado

## SYNTAX

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## DESCRITIVO
Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

Retorna o avaialbility do tipo de recurso e do nome de recurso de assinaturas especificado

## OS

### -Nome
O nome do recurso a ser verificado.

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

### -ResourceType
O tipo de recurso a ser verificado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse

## INFORMA

## LINKS RELACIONADOS

