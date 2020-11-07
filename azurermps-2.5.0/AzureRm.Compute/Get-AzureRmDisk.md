---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5bf1e7cb5a043afaaa4b6fd4d5e8f6820c14fbb1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785995"
---
# Get-AzureRmDisk

## Sinopse
Obtém as propriedades de um disco gerenciado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDisk** Obtém as propriedades de um disco gerenciado.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK

## INFORMA

## LINKS RELACIONADOS

