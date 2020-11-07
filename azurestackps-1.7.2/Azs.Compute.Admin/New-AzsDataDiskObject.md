---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773916"
---
# New-AzsDataDiskObject

## Sinopse
Cria um disco de dados que é usado para criar uma nova imagem da plataforma da máquina virtual.

## SYNTAX

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## DESCRITIVO
Cria um objeto que contém informações sobre um disco de dados.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

Crie um novo objeto de disco de dados.

## OS

### -LUN
Número da unidade lógica.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Localização do modelo de disco.

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

