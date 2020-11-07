---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775008"
---
# Get-AzsDiskMigrationJob

## Sinopse
Retorna a lista de trabalhos de migração de disco gerenciados.

## SYNTAX

### Lista (padrão)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Obter
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## DESCRITIVO
Retorna uma lista de trabalhos de migração de disco.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Obtenha um trabalho específico de migração de disco gerenciado.

### --------------------------EXEMPLO 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

Retorna uma lista de trabalhos de migração de disco gerenciados no local local.

## OS

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
O nome do GUID do trabalho de migração.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

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
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Os parâmetros do status do trabalho de migração de disco.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob

## INFORMA

## LINKS RELACIONADOS

