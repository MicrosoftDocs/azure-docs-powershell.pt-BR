---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425664"
---
# Get-AzsSubscriptionPlan

## Sinopse
Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.

## SYNTAX

### Lista (padrão)
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### Obter
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### Identificação
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.

## OS

### -Acquisitionid
O identificador de aquisição do plano

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

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetSubscriptionId
A ID da assinatura de destino.

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Início
Retorne os N principais itens conforme especificado pelo valor do parâmetro.
Aplica-se após o parâmetro-Skip.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition

## INFORMA

## LINKS RELACIONADOS

