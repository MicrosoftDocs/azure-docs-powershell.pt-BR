---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426146"
---
# Get-AzureStorageServiceMetricsProperty

## Sinopse
Obtém as propriedades de métricas para o serviço de armazenamento do Azure.

## SYNTAX

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageServiceMetricsProperty** Obtém as propriedades Metrics do serviço de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter as propriedades de métricas do serviço blob
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Esse comando obtém as propriedades Metrics do armazenamento de BLOB para o tipo métricas de hora.

## OS

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -MetricsType
Especifica um tipo de métrica.
Este cmdlet obtém as propriedades de métricas do serviço de armazenamento do Azure para o tipo de métricas que esse parâmetro especifica.
Os valores aceitáveis para esse parâmetro são: Hour e minute.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Especifica o tipo de serviço de armazenamento.
Esse cmdlet obtém as propriedades de métricas do tipo que esse parâmetro especifica.
Os valores aceitáveis para esse parâmetro são:

- Irregular 
- TableName
- Coloca
- Arquivos 

Não há suporte para o valor do arquivo no momento.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
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

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


