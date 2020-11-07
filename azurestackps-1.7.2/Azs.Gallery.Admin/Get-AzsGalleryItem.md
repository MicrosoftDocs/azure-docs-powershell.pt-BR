---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774453"
---
# Get-AzsGalleryItem

## Sinopse
Lista itens da galeria.

## SYNTAX

### Lista (padrão)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Obter
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## DESCRITIVO
Obter uma lista de itens de galeria disponíveis no Azure Stack Marketplace

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsGalleryItem
```

Listar itens da galeria.

### --------------------------EXEMPLO 2--------------------------
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Obter um item de Galeria por nome.

## OS

### -Nome
Identidade do item de galeria.
Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem

## INFORMA

## LINKS RELACIONADOS

