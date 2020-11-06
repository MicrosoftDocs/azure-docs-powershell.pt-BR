---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427621"
---
# Get-AzureRmVmssSku

## Sinopse
Obtém os SKUs disponíveis para o VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVmssSku** Obtém os SKUs disponíveis para o conjunto de dimensionamento de máquina virtual (VMSS).

## EXEMPLOS

### Exemplo 1: obter todas as SKUs disponíveis do VMSS
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

Esse comando obtém todas as SKUs disponíveis do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.

## OS

### -ResourceGroupName
Especifica o nome do grupo de recursos do VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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

### Esse cmdlet não produz nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


