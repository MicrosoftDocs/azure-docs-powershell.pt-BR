---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 44273f05793e8f84b28e6dc68f8cc12633fadf0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428926"
---
# <span data-ttu-id="649ae-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="649ae-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="649ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="649ae-102">SYNOPSIS</span></span>
<span data-ttu-id="649ae-103">Cria um perfil de autoescala.</span><span class="sxs-lookup"><span data-stu-id="649ae-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="649ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="649ae-104">SYNTAX</span></span>

### <span data-ttu-id="649ae-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="649ae-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String> -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="649ae-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="649ae-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="649ae-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="649ae-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="649ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="649ae-108">DESCRIPTION</span></span>
<span data-ttu-id="649ae-109">O cmdlet **New-AzureRmAutoscaleProfile** cria um perfil de autoescala.</span><span class="sxs-lookup"><span data-stu-id="649ae-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="649ae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="649ae-110">EXAMPLES</span></span>

### <span data-ttu-id="649ae-111">Exemplo 1: criar um perfil único com uma data fixa</span><span class="sxs-lookup"><span data-stu-id="649ae-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="649ae-112">O primeiro comando cria uma regra de autoescala chamada solicitações e, em seguida, armazena-a na variável $Rule.</span><span class="sxs-lookup"><span data-stu-id="649ae-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="649ae-113">O segundo comando cria um perfil chamado Profile01 com uma data fixa usando a regra em $Rule.</span><span class="sxs-lookup"><span data-stu-id="649ae-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="649ae-114">Exemplo 2: criar um perfil com um cronograma</span><span class="sxs-lookup"><span data-stu-id="649ae-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="649ae-115">O primeiro comando cria uma regra de autoescala chamada solicitações e, em seguida, armazena-a na variável $Rule.</span><span class="sxs-lookup"><span data-stu-id="649ae-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="649ae-116">O segundo comando cria um perfil chamado SecondProfileName com um cronograma recorrente usando a regra em $Rule.</span><span class="sxs-lookup"><span data-stu-id="649ae-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="649ae-117">Exemplo 3: criar perfis com duas regras</span><span class="sxs-lookup"><span data-stu-id="649ae-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="649ae-118">Os dois primeiros comandos criam regras e os armazenam nas variáveis $Rule 1 e $Rule 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="649ae-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="649ae-119">O terceiro comando cria um perfil chamado ProfileName usando as regras em Rule1 e Rule2 e, em seguida, armazena-o na variável $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="649ae-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="649ae-120">O comando final cria um perfil chamado SecondProfileName usando as regras do Rule1 e do Rule2 e, em seguida, armazena-o na variável $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="649ae-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="649ae-121">Exemplo 4: criar um perfil sem agenda ou data fixa</span><span class="sxs-lookup"><span data-stu-id="649ae-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="649ae-122">O primeiro comando cria uma regra de autoescala chamada solicitações e, em seguida, armazena-a na variável $Rule.</span><span class="sxs-lookup"><span data-stu-id="649ae-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="649ae-123">O segundo comando cria um perfil sem um cronograma ou uma data fixa e, em seguida, armazena-o na variável $Profile.</span><span class="sxs-lookup"><span data-stu-id="649ae-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="649ae-124">OS</span><span class="sxs-lookup"><span data-stu-id="649ae-124">PARAMETERS</span></span>

### <span data-ttu-id="649ae-125">-Defaultcapacity</span><span class="sxs-lookup"><span data-stu-id="649ae-125">-DefaultCapacity</span></span>
<span data-ttu-id="649ae-126">Especifica a capacidade padrão.</span><span class="sxs-lookup"><span data-stu-id="649ae-126">Specifies the default capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649ae-127">-DefaultProfile</span></span>
<span data-ttu-id="649ae-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="649ae-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="649ae-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="649ae-129">-EndTimeWindow</span></span>
<span data-ttu-id="649ae-130">Especifica o fim da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="649ae-130">Specifies the end of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="649ae-131">-MaximumCapacity</span></span>
<span data-ttu-id="649ae-132">Especifica a capacidade máxima.</span><span class="sxs-lookup"><span data-stu-id="649ae-132">Specifies the maximum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="649ae-133">-MinimumCapacity</span></span>
<span data-ttu-id="649ae-134">Especifica a capacidade mínima.</span><span class="sxs-lookup"><span data-stu-id="649ae-134">Specifies the minimum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="649ae-135">-Name</span></span>
<span data-ttu-id="649ae-136">Especifica o nome do perfil a ser criado.</span><span class="sxs-lookup"><span data-stu-id="649ae-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="649ae-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="649ae-138">Especifica a frequência de recorrência.</span><span class="sxs-lookup"><span data-stu-id="649ae-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="649ae-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="649ae-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="649ae-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="649ae-140">None</span></span>
- <span data-ttu-id="649ae-141">Secundária</span><span class="sxs-lookup"><span data-stu-id="649ae-141">Second</span></span>
- <span data-ttu-id="649ae-142">Minuto</span><span class="sxs-lookup"><span data-stu-id="649ae-142">Minute</span></span>
- <span data-ttu-id="649ae-143">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="649ae-143">Hour</span></span>
- <span data-ttu-id="649ae-144">Contas</span><span class="sxs-lookup"><span data-stu-id="649ae-144">Day</span></span>
- <span data-ttu-id="649ae-145">Emana</span><span class="sxs-lookup"><span data-stu-id="649ae-145">Week</span></span>
- <span data-ttu-id="649ae-146">Mensais</span><span class="sxs-lookup"><span data-stu-id="649ae-146">Month</span></span>
- <span data-ttu-id="649ae-147">Year</span><span class="sxs-lookup"><span data-stu-id="649ae-147">Year</span></span>

<span data-ttu-id="649ae-148">Nem todos esses valores são suportados.</span><span class="sxs-lookup"><span data-stu-id="649ae-148">Not all of these values are supported.</span></span>

```yaml
Type: RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-149">-Regra</span><span class="sxs-lookup"><span data-stu-id="649ae-149">-Rule</span></span>
<span data-ttu-id="649ae-150">Especifica a lista de regras a serem adicionadas ao perfil.</span><span class="sxs-lookup"><span data-stu-id="649ae-150">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases: Rules

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-151">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="649ae-151">-ScheduleDay</span></span>
<span data-ttu-id="649ae-152">Especifica os dias agendados.</span><span class="sxs-lookup"><span data-stu-id="649ae-152">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleDays

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-153">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="649ae-153">-ScheduleHour</span></span>
<span data-ttu-id="649ae-154">Especifica as horas agendadas.</span><span class="sxs-lookup"><span data-stu-id="649ae-154">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleHours

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-155">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="649ae-155">-ScheduleMinute</span></span>
<span data-ttu-id="649ae-156">Especifica os minutos agendados.</span><span class="sxs-lookup"><span data-stu-id="649ae-156">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleMinutes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-157">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="649ae-157">-ScheduleTimeZone</span></span>
<span data-ttu-id="649ae-158">Especifica o fuso horário do cronograma.</span><span class="sxs-lookup"><span data-stu-id="649ae-158">Specifies the time zone of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-159">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="649ae-159">-StartTimeWindow</span></span>
<span data-ttu-id="649ae-160">Especifica o início da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="649ae-160">Specifies the start of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-161">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="649ae-161">-TimeWindowTimeZone</span></span>
<span data-ttu-id="649ae-162">Especifica o fuso horário da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="649ae-162">Specifies the time zone of the time window.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="649ae-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649ae-163">CommonParameters</span></span>
<span data-ttu-id="649ae-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="649ae-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649ae-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="649ae-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649ae-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="649ae-166">INPUTS</span></span>

### <span data-ttu-id="649ae-167">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="649ae-167">None</span></span>
<span data-ttu-id="649ae-168">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="649ae-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="649ae-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="649ae-169">OUTPUTS</span></span>

### <span data-ttu-id="649ae-170">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="649ae-170">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="649ae-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="649ae-171">NOTES</span></span>

## <span data-ttu-id="649ae-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="649ae-172">RELATED LINKS</span></span>

[<span data-ttu-id="649ae-173">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="649ae-173">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="649ae-174">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="649ae-174">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="649ae-175">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="649ae-175">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="649ae-176">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="649ae-176">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="649ae-177">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="649ae-177">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)

