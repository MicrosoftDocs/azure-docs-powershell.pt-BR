---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775139"
---
# Restore-AzsStorageAccount

## Sinopse
Desexcluir uma conta de armazenamento excluída.

## SYNTAX

### Reexcluir (padrão)
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Identificação
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Desexcluir uma conta de armazenamento excluída.

## EXEMPLOS

### EXEMPLO 1
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

Desexcluir uma conta de armazenamento excluída.

## OS

### -Farmname
ID do farm.

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
ID da conta de armazenamento interna, que não está visível para Tenant.

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: Undelete
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

### -Force
Não peça confirmação.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS
