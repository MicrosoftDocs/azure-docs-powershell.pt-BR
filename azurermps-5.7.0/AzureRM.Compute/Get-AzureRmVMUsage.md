---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610417"
---
# Get-AzureRmVMUsage

## Sinopse
Obtém o uso da contagem do núcleo da máquina virtual para um local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMUsage** Obtém o uso da contagem do núcleo da máquina virtual para um local.

## EXEMPLOS

### Exemplo 1: obter o uso da contagem do núcleo para um local
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

Esse comando obtém o uso da contagem de núcleo da máquina virtual para os locais centrais dos EUA.

## OS

### -Local
Especifica o local para o qual esse cmdlet obtém o uso da contagem do núcleo da máquina virtual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVM](./Get-AzureRmVM.md)


