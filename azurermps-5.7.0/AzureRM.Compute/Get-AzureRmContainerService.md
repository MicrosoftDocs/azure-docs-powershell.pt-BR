---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431070"
---
# Get-AzureRmContainerService

## Sinopse
Obtém um serviço de contêiner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmContainerService** recebe um serviço de contêiner.
Você pode exibir as propriedades de um serviço de contêiner, que incluem estado, número de mestres e agentes e nome de domínio totalmente qualificado do mestre e do agente.

## EXEMPLOS

### Exemplo 1: obter um serviço de contêiner
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

Esse comando obtém um serviço de contêiner chamado CSResourceGroup17.

## OS

### -Nome
Especifica o nome do serviço de contêiner que este cmdlet obtém.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos do serviço de contêiner que este cmdlet obtém.

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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmContainerService](./New-AzureRmContainerService.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Update-AzureRmContainerService](./Update-AzureRmContainerService.md)


