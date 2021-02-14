---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111266"
---
# Get-AzStorageQueue

## Sinopse
Lista as filas de armazenamento.

## Sintaxe

### Nome da Fila (Padrão)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O **cmdlet Get-AzStorageQueue** lista as filas de armazenamento associadas a uma conta de Armazenamento do Azure.

## Exemplos

### Exemplo 1: Listar todas as filas de Armazenamento do Azure
```
PS C:\>Get-AzStorageQueue
```

Esse comando obtém uma lista de todas as filas de armazenamento da conta de Armazenamento atual.

### Exemplo 2: Listar filas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Esse comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com fila.

### Exemplo 3: Listar filas de armazenamento do Azure usando o prefixo de nome da fila
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

Este exemplo usa o parâmetro *Prefixo* para obter uma lista de filas de armazenamento cujo nome começa com fila.

## Parâmetros

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode criar usando o **cmdlet New-AzStorageContext.**

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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
Se nenhum nome for especificado, o cmdlet obtém uma lista de todas as filas.
Se um nome completo ou parcial for especificado, o cmdlet obtém todas as filas que corresponderem ao padrão de nome.

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

### -Prefixo
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## Saídas

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## Notas

## LINKS RELACIONADOS

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


