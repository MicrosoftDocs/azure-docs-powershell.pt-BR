---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609950"
---
# Get-AzureRmProviderOperation

## Sinopse
Obtém as operações de um provedor de recursos do Azure que é protegível usando o Azure RBAC.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O Get-AzureRmProviderOperation Obtém as operações expostas pelos provedores de recursos do Azure.
As operações podem ser compostas para criar funções personalizadas no Azure RBAC.
O comando assume como entrada uma cadeia de caracteres de pesquisa de operação (com um possível caractere curinga (*)) que determina os detalhes de operações a serem exibidos.

Use Get-AzureRmProviderOperation * para obter todas as operações para todos os provedores de recursos do Azure.

Use Get-AzureRmProviderOperation Microsoft. COMPUTE/* para obter todas as operações do provedor de recursos Microsoft. COMPUTE.

## EXEMPLOS

### Obter todas as ações para todos os provedores
```
PS C:\> Get-AzureRmProviderOperation *
```

### Obter ações para um provedor de recursos específico
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### Obter todas as ações que podem ser executadas em máquinas virtuais
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
A cadeia de caracteres de pesquisa da operação (com caracteres curinga possíveis (*))

```yaml
Type: String
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

### String
O parâmetro ' OperationSearchString ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Resources. Models. PSResourceProviderOperation

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação

## LINKS RELACIONADOS
