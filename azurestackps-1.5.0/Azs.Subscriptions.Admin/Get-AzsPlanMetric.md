---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425665"
---
# Get-AzsPlanMetric

## Sinopse
Obter as métricas do plano.

## SYNTAX

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## DESCRITIVO
Obter as métricas do plano.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

Obter as métricas de um plano.

## OS

### -PlanName
Nome do plano.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos no qual o recurso está localizado.

```yaml
Type: String
Parameter Sets: (All)
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

### Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric

## INFORMA

## LINKS RELACIONADOS

