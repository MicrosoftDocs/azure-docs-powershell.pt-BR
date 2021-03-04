---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888314"
---
# Get-AzDataFactoryHub

## SYNOPSIS
Obtém informações sobre hubs no Azure Data Factory.

## SINTAXE

### ByFactoryName (Padrão)
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzDataFactoryHub** obtém informações sobre hubs no Azure Data Factory.
Se você especificar o nome de um hub, esse cmdlet obterá informações sobre esse hub.
Se você não especificar um nome, esse cmdlet obterá informações sobre todos os hubs em um fábrica de dados.

## EXEMPLOS

### Exemplo 1: Obter todos os hubs de dados
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

Esse comando obtém todos os hubs de dados no grupo de recursos do Azure chamado ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.

### Exemplo 2: Obter um hub de dados específico
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

Este comando obtém informações sobre o hub chamado MyDataHub no grupo de recursos do Azure chamado ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.

## PARÂMETROS

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet obtém informações sobre hubs no fábrica de dados que este parâmetro especifica.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Especifica o nome de uma fábrica de dados.
Este cmdlet obtém informações sobre hubs no fábrica de dados que este parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -Name
Especifica o nome do hub sobre o qual obter informações.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Este cmdlet obtém informações sobre hubs que pertencem ao grupo especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## SAÍDAS

### Microsoft.Azure.Commands.DataFactories.Models.PSHub

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[New-AzDataFactoryHub](./New-AzDataFactoryHub.md)

[Remove-AzDataFactoryHub](./Remove-AzDataFactoryHub.md)


