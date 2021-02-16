---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113336"
---
# Get-AzProviderOperation

## Sinopse
Obtém as operações de um provedor de recursos do Azure que são recuráveis usando o Azure RBAC.

## Sintaxe

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
A Get-AzProviderOperation obtém as operações expostas pelos provedores de recursos do Azure.
As operações podem ser compostas para criar funções personalizadas no Azure RBAC.
O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com possíveis caracteres curinga( ) que determina os detalhes *das operações a exibir. Use Get-AzProviderOperation * para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzProviderOperation Microsoft.Compute/ para* obter todas as operações do provedor de recursos Microsoft.Compute.

## Exemplos

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

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
A cadeia de caracteres de pesquisa de operação (com possíveis caracteres curinga (*)

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## Notas
Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS RELACIONADOS
