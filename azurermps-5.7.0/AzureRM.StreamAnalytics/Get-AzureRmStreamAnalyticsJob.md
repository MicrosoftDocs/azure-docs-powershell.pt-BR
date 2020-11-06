---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428689"
---
# Get-AzureRmStreamAnalyticsJob

## Sinopse
Obtém informações de trabalhos do Stream Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByResourceGroup
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStreamAnalyticsJob** lista todos os trabalhos do Stream Analytics definidos na assinatura do Azure ou o grupo de recursos especificado ou obtém informações de trabalho sobre um trabalho específico em um grupo de recursos.

## EXEMPLOS

### EXEMPLO 1: obter informações sobre todos os trabalhos em uma assinatura
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

Esse comando retorna informações sobre todos os trabalhos do Stream Analytics na assinatura do Azure.

### EXEMPLO 2: obter informações sobre todos os trabalhos em um grupo de recursos
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Esse comando retorna informações sobre todos os trabalhos do Stream Analytics no grupo de recursos StreamAnalytics-padrão-oeste-US.

### EXEMPLO 3: obter informações sobre um trabalho específico em um grupo de recursos
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Esse comando retorna informações sobre o trabalho do Stream Analytics StreamingJob no grupo de recursos StreamAnalytics-padrão-oeste-US.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Especifica o nome do trabalho do Azure Stream Analytics a ser recuperado.

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NOEXPAND
Indica que o cmdlet recuperará o trabalho do Azure Stream Analytics, mas não retornará informações sobre suas entradas, saídas e transformações.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics pertence.

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
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

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Start-AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)

[Parar-AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


