---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775138"
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. subscriptions. admin. Models. CheckNameAvailabilityResponse

## INFORMA

## LINKS RELACIONADOS

