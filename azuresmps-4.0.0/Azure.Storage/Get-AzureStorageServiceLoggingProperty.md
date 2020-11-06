---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426149"
---
# Get-AzureStorageServiceLoggingProperty

## Sinopse
Obtém Propriedades de registro em log dos serviços de armazenamento do Azure.

## SYNTAX

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageServiceLoggingProperty** Obtém Propriedades de log para os serviços de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter propriedades de log para o serviço blob
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Este comando obtém Propriedades de log para armazenamento de BLOB.

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

### -ServiceType
Especifica o tipo de serviço de armazenamento.
Este cmdlet obtém as propriedades de log do tipo de serviço que esse parâmetro especifica.
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

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


