---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: c486e7d33593e779a59efa6c4360fe660eac4015
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433130"
---
# Get-AzureRmLog

## Sinopse
Obtém um log de eventos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Consulta sobre CorrelationId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Query no resourceName
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Consulta em ResourceGroupProvider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroup] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Consulta sobre resourceprovider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Consultar no nível da assinatura
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmLog** Obtém um log de eventos.
Os eventos podem ser associados à ID da assinatura atual, ID de correlação, grupo de recursos, ID do recurso ou provedor de recursos.

## EXEMPLOS

### Exemplo 1: obter um log de eventos por ID de assinatura
```
PS C:\>Get-AzureRmLog
```

Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.

### Exemplo 2: obter um log de eventos por ID de assinatura com um número máximo de eventos
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

Este comando lista os eventos mais recentes do 100 associados à ID de assinatura do usuário que levaram 7 dias a partir da data/hora atual.

### Exemplo 3: obter um log de eventos por ID de assinatura com uma hora de início.
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

Este comando lista os eventos mais recentes do 1000 associados à ID de assinatura do usuário que ocorreu em ou após 2017-06-01T10:30 Hora local se essa data/hora não for anterior a 90 dias a partir da data/hora atual.

### Exemplo 4: obter um log de eventos por ID de assinatura com hora de início e hora de término.
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Este comando listará, no máximo, 1000 dos eventos associados à ID de assinatura do usuário que ocorreu em ou após 2017-04-01T10:30 Hora local e antes de 2017-04-14T11:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.

### Exemplo 5: obter um log de eventos por ID de correlação
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual. 
**Observação** : geralmente, esse é apenas um evento.

### Exemplo 6: obter um log de eventos por ID de correlação com um número máximo de eventos
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

Este comando lista os eventos mais recentes do 100 associados à ID de correlação especificada que ocorreram 7 dias a partir da data/hora atual. 
**Observação** : geralmente, esse é apenas um evento.

### Exemplo 7: obter um log de eventos por ID de correlação e hora de início
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Este comando lista os eventos da maioria 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.
**Observação** : geralmente, esse é apenas um evento.

### Exemplo 8: obter um log de eventos por ID de correlação com hora de início e hora de término
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Este comando lista os eventos mais recentes do 1000 associados à ID de correlação especificada que ocorreram em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.

### Exemplo 9: obter um log de eventos para um grupo de recursos
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS"
```

Este comando lista no máximo 1000 os eventos associados ao grupo de recursos especificado que levaram 7 dias a partir da data/hora atual.

### Exemplo 10: obter um log de eventos para um grupo de recursos com um número máximo de eventos
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

Este comando lista os eventos de no máximo 100 associados ao grupo de recursos especificado que levou 7 dias da data/hora atual.

### Exemplo 11: obter um log de eventos para um grupo de recursos por hora de início
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Este comando lista no máximo 1000 Evetns associados ao grupo de recursos especificado que ocorreria em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.

### Exemplo 12: obter um log de eventos para um grupo de recursos com hora de início e hora de término
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Este comando lista os eventos de no máximo 1000 associados ao grupo de recursos especificado que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja: o período de retenção.

### Exemplo 13: obter um log de eventos por ID do recurso
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Este comando lista os eventos mais recentes do 1000 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.

### Exemplo 14: obter um log de eventos por ID do recurso com um número máximo de eventos
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

Este comando lista os eventos mais recentes do 100 associados à ID do recurso especificado que ocorreram 7 dias a partir da data/hora atual.

### Exemplo 15: obter um log de eventos por ID do recurso com uma hora de início
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Este comando lista os eventos da maioria 1000 associados à ID do recurso especificada que ocorreram em ou após 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.

### Exemplo 16: obter um log de eventos por ID do recurso com hora de início e hora de término
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Este comando lista os eventos de no máximo 1000 associados à ID de recurso especificada que ocorreu em ou após 2017-04-15T04:30 tempo local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.

### Exemplo 17: obter um log de eventos por provedor de recursos
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.

### Exemplo 18: obter um log de eventos do provedor de recursos com um número máximo de eventos
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

Este comando lista os eventos mais recentes do 100 associados ao provedor de recursos especificado que levaram 7 dias a partir da data/hora atual.

### Exemplo 19: obter um log de eventos do provedor de recursos com uma hora de início
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Este comando lista os eventos do 1000 associados ao provedor de recursos especificado que ocorreram em ou depois de 2017-05-22T04:30:00 hora local se a hora de início não for anterior a 90 dias a partir da data/hora atual.

### Exemplo 20: obter um log de eventos do provedor de recursos com uma hora de início e hora de término
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Este comando lista os eventos mais recentes do 1000 associados ao provedor de recursos especificado que ocorreram em ou após 2017-04-15T04:30 Hora local, mas antes de 2017-04-25T12:30 horas locais se o intervalo de data/hora completo não for anterior a 90 dias da data/hora atual, ou seja, o período de retenção.

## OS

### -Chamador
Especifica um chamador.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CorrelationId
Especifica a ID de correlação.
Esse parâmetro é obrigatório.

```yaml
Type: System.String
Parameter Sets: Query on CorrelationId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DetailedOutput
Indica que esse cmdlet exibe a saída detalhada.
Por padrão, a saída é resumida.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Especifica a hora de término da consulta na hora local.
O valor padrão é a hora atual.
O valor deve ser posterior a *StartTime*.

Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxEvents
Especifica o número total de registros a serem recuperados para o filtro especificado.
O valor padrão é 1000 e o valor máximo aceito é 100000. Os valores negativos e 0 são ignorados e o valor padrão será usado.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxRecords

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resource
Especifica o nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: Query on ResourceGroupProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Especifica a ID do recurso.

```yaml
Type: System.String
Parameter Sets: Query on ResourceIdName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourceprovider
Especifica um provedor de recurso filtrar por.

```yaml
Type: System.String
Parameter Sets: Query on ResourceProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Especifica a hora de início da consulta na hora local.
O valor padrão é *EndTime* menos sete dias.

Você pode usar o cmdlet Get-Date para obter um objeto **DateTime** .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Especifica o status.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### Nenhuma

## EXIBE

### Nenhuma

## INFORMA

## LINKS RELACIONADOS

