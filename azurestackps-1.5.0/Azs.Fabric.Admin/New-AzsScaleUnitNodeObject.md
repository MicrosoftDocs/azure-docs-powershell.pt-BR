---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425854"
---
# New-AzsScaleUnitNodeObject

## Sinopse
Dados de entrada que permitem adicionar um nó de unidade de escala.

## SYNTAX

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## DESCRITIVO
Dados de entrada que permitem adicionar um nó de unidade de escala.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

Crie um novo objeto de nó.

## OS

### -BMCIPv4Address
Endereço BMC da máquina física.

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

### -ComputerName
Nome de computador da máquina física.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

