---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599427"
---
# Get-AzProviderOperation

## Sinopse
Obtém as operações de um provedor de recursos do Azure que é protegível usando o Azure RBAC.

## SYNTAX

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O Get-AzProviderOperation Obtém as operações expostas pelos provedores de recursos do Azure.
As operações podem ser compostas para criar funções personalizadas no Azure RBAC.
O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com o caractere curinga (es) possível *) que determina os detalhes de operações a serem exibidos. Use Get-AzProviderOperation * para obter todas as operações para todos os provedores de recursos do Azure. Use Get-AzProviderOperation Microsoft. Compute/* para obter todas as operações do provedor de recursos Microsoft. COMPUTE.

## EXEMPLOS

### Obter todas as ações para todos os provedores
```
PS C:\> Get-AzProviderOperation *
```

### Obter ações para um provedor de recursos específico
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Obter todas as ações que podem ser executadas em máquinas virtuais
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
A cadeia de caracteres de pesquisa da operação (com caracteres curinga possíveis (*))

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. PSResourceProviderOperation

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS
