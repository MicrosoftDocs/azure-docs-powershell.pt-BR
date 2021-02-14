---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115665"
---
# Get-AzStorageTable

## Sinopse
Lista as tabelas de armazenamento.

## Sintaxe

### Nomeda Tabela (Padrão)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O **cmdlet Get-AzStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.

## Exemplos

### Exemplo 1: Listar todas as tabelas de Armazenamento do Azure
```
PS C:\>Get-AzStorageTable
```

Esse comando obtém todas as tabelas de armazenamento de uma conta de Armazenamento.

### Exemplo 2: Listar tabelas de armazenamento do Azure usando um caractere curinga
```
PS C:\>Get-AzStorageTable -Name table*
```

Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com tabela.

### Exemplo 3: Listar tabelas de armazenamento do Azure usando o prefixo de nome de tabela
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Esse comando usa o parâmetro *Prefixo* para obter tabelas de armazenamento cujo nome começa com tabela.

## Parâmetros

### -Contexto
Especifica o contexto de armazenamento.
Para criar, você pode usar o cmdlet New-AzStorageContext dados.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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
Caso contrário, ele lista todas as tabelas que corresponderem ao nome especificado ou ao padrão de nome normal.

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

### -Prefixo
Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.
Você pode usá-lo para encontrar todas as tabelas que começam com a mesma cadeia de caracteres, como tabela.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## Saídas

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## Notas

## LINKS RELACIONADOS

[New-AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


