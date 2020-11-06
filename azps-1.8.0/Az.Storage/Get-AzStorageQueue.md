---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 1f0e9f17ea6d240f9f29f677325173e0bbef38f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598653"
---
# Get-AzStorageQueue

## Sinopse
Lista as filas de armazenamento.

## SYNTAX

### QueueName (padrão)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzStorageQueue** lista as filas de armazenamento associadas a uma conta de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: listar todas as filas de armazenamento do Azure
```
PS C:\>Get-AzStorageQueue
```

Este comando obtém uma lista de todas as filas de armazenamento da conta de armazenamento atual.

### Exemplo 2: listar filas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Esse comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com a fila.

### Exemplo 3: listar filas de armazenamento do Azure usando prefixo do nome da fila
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

Este exemplo usa o parâmetro *prefix* para obter uma lista de filas de armazenamento cujo nome começa com a fila.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode criá-lo usando o cmdlet **New-AzStorageContext** .

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica um nome.
Se não for especificado um nome, o cmdlet obterá uma lista de todas as filas.
Se um nome completo ou parcial for especificado, o cmdlet obterá todas as filas correspondentes ao padrão de nome.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Especifica um prefixo usado no nome das filas que você deseja obter.

```yaml
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## INFORMA

## LINKS RELACIONADOS

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


