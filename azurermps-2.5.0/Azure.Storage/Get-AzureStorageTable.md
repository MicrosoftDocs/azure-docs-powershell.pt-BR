---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 834400893dc3d2065a8ca3f0b27783e0a4d5604e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786027"
---
# Get-AzureStorageTable

## Sinopse
Lista as tabelas de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### TableName (padrão)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da tabela.
Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.
Caso contrário, ele lista todas as tabelas que correspondem ao nome especificado ou o padrão normal Name.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.
Você pode usar isso para localizar todas as tabelas que começam com a mesma cadeia de caracteres, como Table.

```yaml
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


