---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: f8c419f59c05b2160ef02fbf239ecc2815bf1109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430590"
---
# Get-AzureStorageQueue

## Sinopse
Lista as filas de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### QueueName (padrão)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageQueue** lista as filas de armazenamento associadas a uma conta de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: listar todas as filas de armazenamento do Azure
```
PS C:\>Get-AzureStorageQueue
```

Este comando obtém uma lista de todas as filas de armazenamento da conta de armazenamento atual.

### Exemplo 2: listar filas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Esse comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com a fila.

### Exemplo 3: listar filas de armazenamento do Azure usando prefixo do nome da fila
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

Este exemplo usa o parâmetro *prefix* para obter uma lista de filas de armazenamento cujo nome começa com a fila.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode criá-lo usando o cmdlet **New-AzureStorageContext** .

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
Especifica um nome.
Se não for especificado um nome, o cmdlet obterá uma lista de todas as filas.
Se um nome completo ou parcial for especificado, o cmdlet obterá todas as filas correspondentes ao padrão de nome.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
Especifica um prefixo usado no nome das filas que você deseja obter.

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### IStorageContext

O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline

### String

O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


