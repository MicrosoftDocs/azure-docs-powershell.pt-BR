---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425610"
---
# Get-AzsEdgeGatewayPool

## Sinopse
Retorna objetos do pool de gateway em um local.

## SYNTAX

### Lista (padrão)
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### Obter
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Retorna objetos do pool do gateway de borda em um local.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsEdgeGatewayPool
```

Obter uma lista de todos os pools de gateways de borda.

### --------------------------EXEMPLO 2--------------------------
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

Obter um pool específico do gateway de borda.

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

### -Local
Local do recurso.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do pool de gateways de borda.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupo de recursos no qual o provedor de recursos foi registrado.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
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

### Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool

## INFORMA

## LINKS RELACIONADOS

