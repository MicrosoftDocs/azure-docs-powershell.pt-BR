---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426138"
---
# Get-AzureStorageTableStoredAccessPolicy

## Sinopse
Obtém a política de acesso armazenado ou políticas para uma tabela de armazenamento do Azure.

## SYNTAX

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageTableStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma tabela de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Esse comando obtém a política de acesso chamada Policy50 na tabela armazenamento chamada Table02.

### Exemplo 2: obter todas as políticas de acesso armazenadas em uma tabela de armazenamento
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

Esse comando obtém todas as políticas de acesso na tabela chamada Table02.

## OS

### -Contexto
Especifica o contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.

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

### -Política
Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tabela
Especifica o nome da tabela de armazenamento do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

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

[New-AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[Remove-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Set-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


