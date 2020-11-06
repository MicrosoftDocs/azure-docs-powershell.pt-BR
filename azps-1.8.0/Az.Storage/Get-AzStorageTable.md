---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 5c575ace97687ca6906a73e8e79d93343f369f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598643"
---
# Get-AzStorageTable

## Sinopse
Lista as tabelas de armazenamento.

## SYNTAX

### TableName (padrão)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: listar todas as tabelas de armazenamento do Azure
```
PS C:\>Get-AzStorageTable
```

Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.

### Exemplo 2: listar tabelas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzStorageTable -Name table*
```

Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com Table.

### Exemplo 3: listar tabelas de armazenamento do Azure usando prefixo de nome de tabela
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Esse comando usa o parâmetro *prefix* para obter tabelas de armazenamento cujo nome começa com Table.

## OS

### -Contexto
Especifica o contexto de armazenamento.
Para criá-la, você pode usar o cmdlet New-AzStorageContext.

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

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


