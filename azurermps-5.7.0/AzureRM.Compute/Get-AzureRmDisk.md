---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431068"
---
# Get-AzureRmDisk

## Sinopse
Obtém as propriedades de um disco.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDisk** Obtém as propriedades de um disco.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

Este comando obtém as propriedades do disco chamado "Disk01" no grupo de recursos "ResourceGroup01".

### Exemplo 2
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

Esse comando obtém as propriedades de todos os discos no grupo de recursos "ResourceGroup01".

### Exemplo 3
```
PS C:\> Get-AzureRmDisk
```

Esse comando obtém as propriedades de todos os discos na assinatura.

## OS

### -Diskname
Especifica o nome de um disco.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList

## INFORMA

## LINKS RELACIONADOS

