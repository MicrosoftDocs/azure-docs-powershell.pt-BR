---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116952"
---
# Get-UsageAggregates

## Sinopse
Obtém os detalhes de uso da assinatura do Azure relatados.

## Sintaxe

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Get-UsageAggregates** obtém dados agregados de uso da assinatura do Azure pelas seguintes propriedades: 
- Horários de início e término de quando o uso foi relatado.
- Precisão de agregação, diariamente ou por hora.
- Detalhes do nível de instância para várias instâncias do mesmo recurso.
Para obter resultados consistentes, os dados retornados são baseados em quando os detalhes de uso foram relatados pelo recurso do Azure.
Para obter mais informações, consulte Referência da API REST de Cobrança do Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( na biblioteca do Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network.

## Exemplos

### Exemplo 1: Recuperar dados da assinatura
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Esse comando recupera os dados de uso relatados da assinatura entre 02/05/2015 e 05/05/2015.

## Parâmetros

### -AggregationArularity
Especifica a precisão de agregação dos dados.
Os valores válidos são: Diário e Hora.
O valor padrão é Diário.

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
Para um grande conjunto de resultados, as respostas são páginas usando tokens de continuação.
O token de continuação serve como um indicador para o progresso.
Se você não especificar esse parâmetro, os dados serão recuperados do início do dia ou da hora especificados no *ReportedStartTime.*
Recomendamos que você siga o próximo link na resposta à página, embora os dados.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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
Especifica a hora de término relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.
O Azure é um sistema distribuído, abrangendo vários datacenters em todo o mundo, portanto, há um atraso entre quando o recurso foi realmente consumido, que é o tempo de uso do recurso e quando o evento de uso atingiu o sistema de cobrança, que é o tempo relatado pelo uso do recurso.
Para obter todos os eventos de uso de uma assinatura que são relatados por um período de tempo, você consulta por hora relatada.
Mesmo que você consulte por hora reportada, o cmdlet agrega os dados de resposta pelo tempo de uso do recurso.
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
Por exemplo, se você estiver executando três sites, por padrão, receberá três itens de linha para consumo de site.
No entanto, quando o valor é $False, todos os dados para a mesma **ID** de assinatura, **meterId,** **usageStartTime** e **usageEndTime** são recolhidos em um único item de linha.

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

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## Notas

## LINKS RELACIONADOS
