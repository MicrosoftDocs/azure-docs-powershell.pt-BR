---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115649"
---
# New-AzStorageTable

## Sinopse
Cria uma tabela de armazenamento.

## Sintaxe

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.

## Exemplos

### Exemplo 1: Criar uma tabela de armazenamento do azure
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

Esse comando cria uma tabela de armazenamento com um nome de tabelaabc.

### Exemplo 2: Criar várias tabelas de armazenamento do Azure
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

Esse comando cria várias tabelas.
Ele usa o **método Dividir** da classe cadeia de caracteres **.NET** e passa os nomes no pipeline.

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
Especifica um nome para a nova tabela.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzStorageTable](./Get-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)


