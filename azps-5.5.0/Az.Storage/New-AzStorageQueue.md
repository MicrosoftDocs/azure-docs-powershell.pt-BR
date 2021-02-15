---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116103"
---
# New-AzStorageQueue

## Sinopse
Cria uma fila de armazenamento.

## Sintaxe

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzStorageQueue** cria uma fila de armazenamento no Azure.

## Exemplos

### Exemplo 1: Criar uma fila de armazenamento do Azure
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

Este exemplo cria uma fila de armazenamento chamada queueabc.

### Exemplo 2: Criar várias filas de armazenamento do Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

Este exemplo cria várias filas de armazenamento.
Ele usa o método Dividir da classe cadeia de caracteres .NET e passa os nomes no pipeline.

## Parâmetros

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode criar usando o cmdlet New-AzStorageContext dados.

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
Especifica um nome para a fila.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


