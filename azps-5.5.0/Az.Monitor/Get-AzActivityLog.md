---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113566"
---
# Get-AzActivityLog

## Sinopse
Recuperar eventos do Log de Atividades.

## Sintaxe

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet Get-AzActivityLog recupera eventos do Log de Atividades. Os eventos podem ser associados à ID de assinatura atual, À ID de correlação, ao grupo de recursos, à ID do recurso ou ao provedor de recursos.

## Exemplos

### Exemplo 1: Obter um log de eventos por ID da assinatura
```
PS C:\>Get-ActivityAzLog
```

Esse comando lista no máximo 1.000 eventos associados à ID de assinatura do usuário que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 2: Obter um log de eventos por ID de assinatura com um número máximo de eventos
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Esse comando lista no máximo 100 eventos associados à ID de assinatura do usuário que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 3: Obter um log de eventos por ID de assinatura com uma hora de início.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Esse comando lista no máximo 1.000 eventos associados à ID de assinatura do usuário que ocorreu em ou após 2017-06-01T10:30 hora local se essa data/hora não for mais antiga do que 90 dias a partir da data/hora atual.

### Exemplo 4: Obter um log de eventos por ID de assinatura com uma hora de início e hora de término.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Esse comando lista no máximo 1.000 dos eventos associados à ID de assinatura do usuário que ocorreram no período local de 2017-04-01T10:30 e antes de 2017-04-14T11:30 local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.

### Exemplo 5: Obter um log de eventos por ID de correlação
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Esse comando lista no máximo 1.000 eventos associados à ID de correlação especificada que ocorreu 7 dias a partir da data/hora atual. 
**OBSERVAÇÃO:** geralmente é apenas um evento.

### Exemplo 6: Obter um log de eventos por ID de correlação com um número máximo de eventos
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Esse comando lista no máximo 100 eventos associados à ID de correlação especificada que ocorreu 7 dias a partir da data/hora atual. 
**OBSERVAÇÃO:** geralmente é apenas um evento.

### Exemplo 7: Obter um log de eventos por ID de correlação e hora de início
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Esse comando lista no máximo 1.000 eventos associados à ID de correlação especificada que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.
**OBSERVAÇÃO:** geralmente é apenas um evento.

### Exemplo 8: Obter um log de eventos por ID de correlação com hora de início e hora de término
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Esse comando lista no máximo 1000 eventos associados à ID de correlação especificada que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.

### Exemplo 9: Obter um log de eventos para um grupo de recursos
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Esse comando lista no máximo 1.000 os eventos associados ao grupo de recursos especificado que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 10: Obter um log de eventos para um grupo de recursos com um número máximo de eventos
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Esse comando lista no máximo 100 eventos associados ao grupo de recursos especificado que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 11: Obter um log de eventos para um grupo de recursos por hora de início
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Esse comando lista no máximo 1.000 eventos associados ao grupo de recursos especificado que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.

### Exemplo 12: Obter um log de eventos para um grupo de recursos com uma hora de início e uma hora de término
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Esse comando lista no máximo 1000 eventos associados ao grupo de recursos especificado que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for anterior a 90 dias a partir da data/hora atual, ou seja: o período de retenção.

### Exemplo 13: Obter um log de eventos por ID do recurso
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Esse comando lista no máximo 1.000 eventos associados à ID de recurso especificada que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 14: Obter um log de eventos por ID do recurso com um número máximo de eventos
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Esse comando lista no máximo 100 eventos associados à ID de recurso especificada que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 15: Obter um log de eventos por ID do recurso com uma hora de início
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Esse comando lista no máximo 1000 eventos associados à ID de recurso especificada que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.

### Exemplo 16: Obter um log de eventos por ID do recurso com uma hora de início e uma hora de término
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Esse comando lista no máximo 1000 eventos associados à ID de recurso especificada que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.

### Exemplo 17: Obter um log de eventos por provedor de recursos
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreram 7 dias a partir da data/hora atual.

### Exemplo 18: Obter um log de eventos por provedor de recursos com um número máximo de eventos
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Esse comando lista no máximo 100 eventos associados ao provedor de recursos especificado que ocorreu 7 dias a partir da data/hora atual.

### Exemplo 19: Obter um log de eventos por provedor de recursos com uma hora de início
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreu em ou após 2017-05-22T04:30:00 hora local se a hora de início não for mais antiga do que 90 dias a partir da data/hora atual.

### Exemplo 20: Obter um log de eventos por provedor de recursos com uma hora de início e uma hora de término
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Esse comando lista no máximo 1.000 eventos associados ao provedor de recursos especificado que ocorreu em ou após 2017-04-15T04:30 hora local, mas antes de 2017-04-25T12:30 hora local se o intervalo de data/hora inteiro não for mais antigo do que 90 dias a partir da data/hora atual, ou seja: o período de retenção.

## Parâmetros

### -Chamador
O chamador dos eventos a buscar

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
A CorrelationId

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -DetailedOutput
Retornar objeto com todos os detalhes dos eventos (o padrão é retornar apenas alguns atributos, ou seja, nenhum detalhe)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
O tempo de término da consulta

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
O número máximo de registros a buscar.
Alias: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A ResourceId

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
O nome do ResourceProvider

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
A ID de correlação da consulta

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
O status dos eventos a buscar

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## Saídas

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## Notas

## LINKS RELACIONADOS
