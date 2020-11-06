---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441606"
---
# Get-AzureRmOperationalInsightsWorkspace

## Sinopse
Obtém informações sobre um espaço de trabalho.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmOperationalInsightsWorkspace** Obtém informações sobre um espaço de trabalho existente.
Se você especificar um nome de espaço de trabalho, este cmdlet obterá informações sobre esse espaço de trabalho.
Se você não especificar um nome, esse cmdlet obterá informações sobre todos os espaços de trabalho em um grupo de recursos.
Se você não especificar um nome e um grupo de recursos, esse cmdlet obterá informações sobre todos os espaços de trabalho em uma assinatura.

## EXEMPLOS

### Exemplo 1: obter um espaço de trabalho por nome
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

Esse comando obtém um espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.

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

### -Nome
Especifica o nome do espaço de trabalho.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace]

### Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace

## INFORMA

## LINKS RELACIONADOS

[Cmdlets do Azure Operational insights](./AzureRM.OperationalInsights.md)


