---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785423"
---
# Get-UsageAggregates

## Sinopse
Obtém os detalhes de uso da assinatura do Azure relatados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-UsageAggregates** obtém dados de uso da assinatura do Azure agregados nas seguintes propriedades: 

- Horários de início e término de quando o uso foi relatado.

- A precisão da agregação, diária ou por hora.

- Detalhe o nível de instância para várias instâncias do mesmo recurso.

Para resultados consistentes, os dados retornados se baseiam quando os detalhes de uso foram relatados pelo recurso do Azure.

Para obter mais informações, consulte referência da API REST de cobrança do Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) na biblioteca Microsoft Developer Network.

## EXEMPLOS

### Exemplo 1: recuperar dados de assinatura
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Esse comando recupera os dados de uso relatados para a assinatura entre o 5/2/2015 e o 5/5/2015.

## OS

### -AggregationGranularity
Especifica a precisão da agregação dos dados.
Os valores válidos são: diariamente e por hora.

O valor padrão é diário.

```yaml
Type: AggregationGranularity
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
Para um grande conjunto de resultados, as respostas são paginadas usando-se tokens de continuação.
O token de continuação funciona como um indicador para progresso.
Se você não especificar esse parâmetro, os dados serão recuperados do início do dia ou da hora especificado em *ReportedStartTime*.
Recomendamos que você siga o próximo link na página resposta a, apesar dos dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ReportedEndTime
Especifica a hora de término informada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.

O Azure é um sistema distribuído, abrangendo vários datacenters em todo o mundo, portanto há um atraso entre o momento em que o recurso foi realmente consumido, que é o tempo de uso do recurso e quando o evento de uso atinge o sistema de cobrança, que é o tempo informado sobre o uso do recurso.
Para obter todos os eventos de uso de uma assinatura reportada por um período de tempo, você consulta por hora reportada.
Apesar de você consultar por tempo informado, o cmdlet agrega os dados de resposta pelo tempo de uso do recurso.
Os dados de uso dos recursos são o pivô útil para a análise dos dados.

```yaml
Type: DateTime
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
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Detalhes do
Indica se esse cmdlet retorna detalhes em nível de instância com os dados de uso.

O valor padrão é $True.

Se $False, o serviço agregará os resultados no lado do servidor e, portanto, retornará menos grupos de agregação.
Por exemplo, se você estiver executando três sites, por padrão, receberá três itens de linha para o consumo de site.
No entanto, quando o valor é $False, todos os dados para o mesmo **SubscriptionId** , **meterid** , **usageStartTime** e **usageEndTime** são recolhidos em um único item de linha.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse

## INFORMA

## LINKS RELACIONADOS

