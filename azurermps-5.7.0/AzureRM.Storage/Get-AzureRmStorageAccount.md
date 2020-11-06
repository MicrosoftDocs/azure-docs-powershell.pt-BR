---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427404"
---
# Get-AzureRmStorageAccount

## Sinopse
Obtém uma conta de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ResourceGroupParameterSet
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStorageAccount** Obtém uma conta de armazenamento especificada ou todas as contas de armazenamento em um grupo de recursos ou na assinatura.

## EXEMPLOS

### Exemplo 1: obter uma conta de armazenamento especificada
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Este comando obtém a conta de armazenamento especificada.

### Exemplo 2: obter todas as contas de armazenamento em um grupo de recursos
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

Este comando obtém todas as contas de armazenamento em um grupo de recursos.

### Exemplo 3: obter todas as contas de armazenamento na assinatura
```
PS C:\>Get-AzureRmStorageAccount
```

Este comando obtém todas as contas de armazenamento na assinatura.

## OS

### -Nome
Especifica o nome da conta de armazenamento a ser obtida.

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a conta de armazenamento a ser obtida.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
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

[New-AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
