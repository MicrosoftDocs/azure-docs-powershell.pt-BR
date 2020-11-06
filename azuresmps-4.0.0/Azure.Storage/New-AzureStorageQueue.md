---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425975"
---
# New-AzureStorageQueue

## Sinopse
Cria uma fila de armazenamento.

## SYNTAX

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageQueue** cria uma fila de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: criar uma fila de armazenamento do Azure
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

Este exemplo cria uma fila de armazenamento chamada queueabc.

### Exemplo 2: criar várias filas de armazenamento do Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

Este exemplo cria várias filas de armazenamento.
Ele usa o método Split da classe String .NET e, em seguida, passa os nomes no pipeline.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode criá-lo usando o cmdlet New-AzureStorageContext.

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

### -Nome
Especifica um nome para a fila.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


