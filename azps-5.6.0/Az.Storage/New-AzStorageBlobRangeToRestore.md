---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891976"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Cria um objeto Blob Range para restaurar uma conta de Armazenamento.

## SINTAXE

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzStorageBlobRangeToRestore** cria um objeto de intervalo Blob, que pode ser usado em Restore-AzStorageBlobRange.

## EXEMPLOS

### Exemplo 1: cria um intervalo de blob para restaurar
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Este comando cria um intervalo de blob a ser restaurado, que começa em container1/blob1 (include) e termina em container2/blob2 (exclude).

### Exemplo 2: cria um intervalo de blob que será restaurado do primeiro blob em ordem alfabética, para um blob específico (excluir)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Este comando cria um intervalo de blob que será restaurado do primeiro blob da ordem alfabética, para um blob contêiner2/blob2 específico (excluir)

### Exemplo 3: cria um intervalo de blob que será restaurado de um blob específico (include), até o último blob em ordem alfabética
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Este comando cria um intervalo de blob que será restaurado de um blob container1/blob1 específico (include), até o último blob em ordem alfabética.

### Exemplo 4: cria um intervalo de blob que restaurará todos os blobs
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Este comando cria um intervalo de blob que restaurará todos os blobs.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
O intervalo final será excluído em blobs de restauração.
De defini-lo como strng vazio para restaurar até o final.

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
O intervalo inicial será incluído em blobs de restauração.
De defini-la como cadeia de caracteres vazia para ser restaurada desde o início.

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

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## NOTES

## LINKS RELACIONADOS
