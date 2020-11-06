---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427735"
---
# Get-AzureRmStreamAnalyticsQuota

## Sinopse
Obtém informações sobre a cota de unidade de streaming para uma região.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmStreamAnalyticsQuota** Obtém informações sobre a cota de unidade de streaming para uma região.

## EXEMPLOS

### EXEMPLO 1: obter informações sobre a cota de unidade de streaming para uma região
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

Esse comando retorna informações sobre a cota da unidade de streaming e o uso na região oeste dos EUA.

## OS

### -Local
Especifica o nome de uma região do Azure ou o local do Data Center para o qual obter informações sobre a cota da unidade de streaming.
Consulte https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services para obter uma lista de regiões do Azure com suporte.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSQuota

## INFORMA

## LINKS RELACIONADOS

[Cmdlets do Azure Stream Analytics](./AzureRM.StreamAnalytics.md)


