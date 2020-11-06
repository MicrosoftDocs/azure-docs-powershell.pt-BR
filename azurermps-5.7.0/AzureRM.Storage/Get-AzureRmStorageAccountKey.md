---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427402"
---
# Get-AzureRmStorageAccountKey

## Sinopse
Obtém as teclas de acesso para uma conta de armazenamento do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStorageAccountKey** Obtém as teclas de acesso para uma conta de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter as teclas de acesso para uma conta de armazenamento
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Este comando obtém as chaves da conta de armazenamento do Azure especificada.

### Exemplo 2: obter uma tecla de acesso específica para uma conta de armazenamento
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## OS

### -Nome
Especifica o nome da conta de armazenamento para a qual esse cmdlet obtém chaves.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a conta de armazenamento.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmStorageAccountKey](./New-AzureRmStorageAccountKey.md)
