---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116335"
---
# New-AzStorageBlobRangeToRestore

## Sinopse
Cria um objeto de Intervalo de Blob para restaurar uma conta de Armazenamento.

## Sintaxe

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzStorageBrangeRangeToRestore** cria um objeto de intervalo blob, que pode ser usado em Restore-AzStorageBrangeRange.

## Exemplos

### Exemplo 1: cria um intervalo de blob para restaurar
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Esse comando cria um intervalo de blob para restaurar, que começa no contêiner1/blob1 (incluir) e termina no contêiner2/blob2 (excluir).

### Exemplo 2: cria um intervalo de blob que será restaurado do primeiro blob em ordem alfabética para um blob específico (excluir)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Esse comando cria um intervalo de blob que será restaurado do primeiro blob da ordem alfabética para um contêiner de blob específico2/blob2 (excluir)

### Exemplo 3: cria um intervalo de blob que será restaurado de um blob específico (incluir) até o último blob em ordem alfabética
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Esse comando cria um intervalo de blob que será restaurado de um contêiner de blob1/blob1 específico (incluir) até o último blob em ordem alfabética.

### Exemplo 4: cria um intervalo de blobs que restaurará todos os blobs
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Esse comando cria um intervalo de blobs que restaurará todos os blobs.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRange
Especifique o intervalo final de restauração de blob.
O intervalo final será excluído na restauração de blobs.
De defini-lo como um strng vazio para restaurar até o fim.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Especifique o intervalo inicial de restauração de blob.
O intervalo inicial será incluído na restauração de blobs.
De defini-la como cadeia de caracteres vazia para restaurar do começo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Management.Storage.Models.PSBstoreRestoreRange

## Notas

## LINKS RELACIONADOS
