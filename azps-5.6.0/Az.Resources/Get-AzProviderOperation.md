---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901581"
---
# Get-AzProviderOperation

## SYNOPSIS
Obtém as operações de um provedor de recursos do Azure que são rescuráveis usando o Azure RBAC.

## SINTAXE

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O Get-AzProviderOperation obtém as operações expostas pelos provedores de recursos do Azure.
As operações podem ser compostas para criar funções personalizadas no Azure RBAC.
O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com caracteres curinga possíveis( ) que determina os detalhes *das operações a ser exibidos. Use Get-AzProviderOperation * para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzProviderOperation Microsoft.Compute/* para obter todas as operações do provedor de recursos Microsoft.Compute.

## EXEMPLOS

### Exemplo 1: Obter todas as ações para todos os provedores
```powershell
PS C:\> Get-AzProviderOperation *
```

### Exemplo 2: Obter ações para um provedor de recursos específico
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Exemplo 3: Obter todas as ações que podem ser executadas em máquinas virtuais
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARÂMETROS

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

### -OperationSearchString
A cadeia de caracteres de pesquisa de operação (com caracteres curinga possíveis (*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## NOTES
Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS RELACIONADOS
