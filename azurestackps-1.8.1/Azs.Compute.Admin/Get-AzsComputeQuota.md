---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775118"
---
# Get-AzsComputeQuota

## Sinopse
Retorna as cotas que especificam os limites de cota para objetos de computação.

## SYNTAX

### Lista (padrão)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Obter
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Obter uma lista de cotas existentes.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Obter todas as cotas de computação no local especificado.

### --------------------------EXEMPLO 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Obtenha uma cota de computação específica.

## OS

### -Local
{{Descrição do local de preenchimento}}

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
Nome da cota.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### ComputeQuotaObject

## INFORMA

## LINKS RELACIONADOS

