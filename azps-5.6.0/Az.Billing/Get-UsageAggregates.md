---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890021"
---
# Get-UsageAggregates

## SYNOPSIS
Obtém os detalhes de uso da assinatura do Azure relatados.

## SINTAXE

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-UsageAggregates** obtém dados agregados de uso da assinatura do Azure pelas seguintes propriedades: 
- Horários de início e término de quando o uso foi relatado.
- Precisão de agregação, diariamente ou por hora.
- Detalhes de nível de instância para várias instâncias do mesmo recurso.
Para resultados consistentes, os dados retornados se baseiam em quando os detalhes de uso foram relatados pelo recurso do Azure.
Para obter mais informações, consulte Referência da API REST de Cobrança do Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( na biblioteca da Rede de https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Desenvolvedores da Microsoft.

## EXEMPLOS

### Exemplo 1: Recuperar dados de assinatura
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Este comando recupera os dados de uso relatados para a assinatura entre 2/5/2015 e 5/5/2015.

## PARÂMETROS

### -AggregationGranularity
Especifica a precisão de agregação dos dados.
Os valores válidos são: Diário e Hora.
O valor padrão é Daily.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Especifica o token de continuação que foi recuperado do corpo da resposta na chamada anterior.
Para um conjunto de resultados grande, as respostas são páginadas usando tokens de continuação.
O token de continuação serve como um indicador para o progresso.
Se você não especificar esse parâmetro, os dados serão recuperados do início do dia ou da hora especificado em *ReportedStartTime*.
Recomendamos que você siga o próximo link na resposta à página embora os dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -ReportedEndTime
Especifica a hora final relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.
O Azure é um sistema distribuído, abrangendo vários datacenters em todo o mundo, portanto, há um atraso entre quando o recurso foi realmente consumido, que é o tempo de uso do recurso e quando o evento de uso atingiu o sistema de cobrança, que é o tempo de uso do recurso relatado.
Para obter todos os eventos de uso de uma assinatura que são relatados por um período de tempo, você consulta por hora relatada.
Mesmo que você consulte por hora relatada, o cmdlet agrega os dados de resposta pelo tempo de uso do recurso.
Os dados de uso de recursos são o pivô útil para analisar os dados.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Especifica a hora de início relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Indica se esse cmdlet retorna detalhes no nível da instância com os dados de uso.
O valor padrão é $True.
Se $False, o serviço agrega os resultados no lado do servidor e, portanto, retorna menos grupos agregados.
Por exemplo, se você estiver executando três sites, por padrão, receberá três itens de linha para consumo de sites.
No entanto, quando o valor é $False, todos os dados para a mesma **subscriptionId,** **meterId,** **usageStartTime** e **usageEndTime** são recolhidos em um único item de linha.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## NOTES

## LINKS RELACIONADOS
