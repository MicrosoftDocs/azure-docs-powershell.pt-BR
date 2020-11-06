---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427069"
---
# Get-AzureStorageTable

## Sinopse
Lista as tabelas de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### TableName (padrão)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: listar todas as tabelas de armazenamento do Azure
```
PS C:\>Get-AzureStorageTable
```

Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.

### Exemplo 2: listar tabelas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzureStorageTable -Name table*
```

Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com Table.

### Exemplo 3: listar tabelas de armazenamento do Azure usando prefixo de nome de tabela
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Esse comando usa o parâmetro *prefix* para obter tabelas de armazenamento cujo nome começa com Table.

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
Especifica o nome da tabela.
Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.
Caso contrário, ele lista todas as tabelas que correspondem ao nome especificado ou o padrão normal Name.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.
Você pode usar isso para localizar todas as tabelas que começam com a mesma cadeia de caracteres, como Table.

```yaml
Type: String
Parameter Sets: TablePrefix
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

### IStorageContext

O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline

### String

O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


