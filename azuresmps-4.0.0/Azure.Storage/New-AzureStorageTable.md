---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426064"
---
# New-AzureStorageTable

## Sinopse
Cria uma tabela de armazenamento.

## SYNTAX

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: criar uma tabela de armazenamento do Azure
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

Esse comando cria uma tabela de armazenamento com um nome de tableabc.

### Exemplo 2: criar várias tabelas de armazenamento do Azure
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

Esse comando cria várias tabelas.
Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.

## OS

### -Contexto
Especifica o contexto de armazenamento.
Para criá-la, você pode usar o cmdlet New-AzureStorageContext.

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
Especifica um nome para a nova tabela.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

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

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


