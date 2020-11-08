---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113799"
---
# New-AzStorageBlobRangeToRestore

## Sinopse
Cria um objeto de intervalo de BLOB para restaurar uma conta de armazenamento.

## SYNTAX

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzStorageBlobRangeToRestore** cria um objeto de intervalo de BLOB, que pode ser usado em Restore-AzStorageBlobRange.

## EXEMPLOS

### Exemplo 1: cria um intervalo de BLOB para restaurar
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Esse comando cria um intervalo de BLOB para restaurar, que começa em Container1/blob1 (include) e termina em container2/blob2 (excluir).

### Exemplo 2: cria um intervalo de BLOB que será restaurado do primeiro blob em ordem alfabética, para um blob específico (excluir)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Esse comando cria um intervalo de BLOB que será restaurado do primeiro BLOB da ordem alfabética, para um blob específico container2/blob2 (excluir)

### Exemplo 3: cria um intervalo de BLOB que será restaurado de um blob específico (include) até o último blob em ordem alfabética
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Esse comando cria um intervalo de BLOB que será restaurado de um blob Container1/blob1 (include) específico para o último blob em ordem alfabética.

### Exemplo 4: cria um intervalo de BLOBs que restaurará todos os BLOBs
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Esse comando cria um intervalo de BLOB que restaurará todos os BLOBs.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Especifique o intervalo final da restauração de BLOB.
O intervalo final será excluído nos blobs de restauração.
Defina-o como strng vazio para restaurar para o fim.

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
Especifique o intervalo inicial da restauração de BLOB.
O intervalo inicial será incluído nos blobs de restauração.
Defina-o como uma cadeia de caracteres vazia para restaurar do início.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange

## INFORMA

## LINKS RELACIONADOS
