---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426152"
---
# Get-AzureStorageQueueStoredAccessPolicy

## Sinopse
Obtém a política de acesso armazenado ou políticas para uma fila de armazenamento do Azure.

## SYNTAX

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageQueueStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma fila de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter uma política de acesso armazenado na fila
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

Esse comando obtém a política de acesso chamada Policy12 na fila de armazenamento chamada MyQueue.

### Exemplo 2: obter todas as políticas de acesso armazenadas na fila
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
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

### -Política
Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).

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

### -Queue
Especifica o nome da fila de armazenamento do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

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

[New-AzureStorageQueueStoredAccessPolicy](./New-AzureStorageQueueStoredAccessPolicy.md)

[Remove-AzureStorageQueueStoredAccessPolicy](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[Set-AzureStorageQueueStoredAccessPolicy](./Set-AzureStorageQueueStoredAccessPolicy.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


