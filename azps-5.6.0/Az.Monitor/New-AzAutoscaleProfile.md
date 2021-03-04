---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: 52c3849a7e0e5ce732f54cd1136b2cc52dfbb94c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889218"
---
# <span data-ttu-id="26134-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="26134-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="26134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26134-102">SYNOPSIS</span></span>
<span data-ttu-id="26134-103">Cria um perfil de escala automática.</span><span class="sxs-lookup"><span data-stu-id="26134-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="26134-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26134-104">SYNTAX</span></span>

### <span data-ttu-id="26134-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="26134-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26134-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="26134-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26134-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="26134-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26134-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26134-108">DESCRIPTION</span></span>
<span data-ttu-id="26134-109">O cmdlet **New-AzAutoscaleProfile** cria um perfil de escala automática.</span><span class="sxs-lookup"><span data-stu-id="26134-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="26134-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26134-110">EXAMPLES</span></span>

### <span data-ttu-id="26134-111">Exemplo 1: Criar perfil único com uma data fixa</span><span class="sxs-lookup"><span data-stu-id="26134-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="26134-112">O primeiro comando cria uma regra de escala automática chamada Solicitações e, em seguida, a armazena na variável $Rule de escala automática.</span><span class="sxs-lookup"><span data-stu-id="26134-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="26134-113">O segundo comando cria um perfil chamado Profile01 com uma data fixa usando a regra em $Rule.</span><span class="sxs-lookup"><span data-stu-id="26134-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="26134-114">Exemplo 2: Criar um perfil com uma agenda</span><span class="sxs-lookup"><span data-stu-id="26134-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="26134-115">O primeiro comando cria uma regra de escala automática chamada Solicitações e, em seguida, a armazena na variável $Rule de escala automática.</span><span class="sxs-lookup"><span data-stu-id="26134-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="26134-116">O segundo comando cria um perfil chamado SecondProfileName com uma agenda recorrente usando a regra em $Rule.</span><span class="sxs-lookup"><span data-stu-id="26134-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="26134-117">Exemplo 3: Criar perfis com duas regras</span><span class="sxs-lookup"><span data-stu-id="26134-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="26134-118">Os dois primeiros comandos criam regras e as armazenam nas variáveis $Rule 1 e $Rule 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="26134-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="26134-119">O terceiro comando cria um perfil chamado ProfileName usando as regras em Rule1 e Rule2 e, em seguida, armazena-o na variável $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="26134-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="26134-120">O comando final cria um perfil chamado SecondProfileName usando as regras em Rule1 e Rule2 e, em seguida, armazena-o na variável $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="26134-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="26134-121">Exemplo 4: Criar um perfil sem agendamento ou data fixa</span><span class="sxs-lookup"><span data-stu-id="26134-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="26134-122">O primeiro comando cria uma regra de escala automática chamada Solicitações e, em seguida, a armazena na variável $Rule de escala automática.</span><span class="sxs-lookup"><span data-stu-id="26134-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="26134-123">O segundo comando cria um perfil sem uma agenda ou uma data fixa e o armazena na variável $Profile.</span><span class="sxs-lookup"><span data-stu-id="26134-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="26134-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26134-124">PARAMETERS</span></span>

### <span data-ttu-id="26134-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="26134-125">-DefaultCapacity</span></span>
<span data-ttu-id="26134-126">Especifica a capacidade padrão.</span><span class="sxs-lookup"><span data-stu-id="26134-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26134-127">-DefaultProfile</span></span>
<span data-ttu-id="26134-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="26134-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26134-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="26134-129">-EndTimeWindow</span></span>
<span data-ttu-id="26134-130">Especifica o fim da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="26134-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="26134-131">-MaximumCapacity</span></span>
<span data-ttu-id="26134-132">Especifica a capacidade máxima.</span><span class="sxs-lookup"><span data-stu-id="26134-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="26134-133">-MinimumCapacity</span></span>
<span data-ttu-id="26134-134">Especifica a capacidade mínima.</span><span class="sxs-lookup"><span data-stu-id="26134-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-135">-Name</span><span class="sxs-lookup"><span data-stu-id="26134-135">-Name</span></span>
<span data-ttu-id="26134-136">Especifica o nome do perfil a ser criado.</span><span class="sxs-lookup"><span data-stu-id="26134-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="26134-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="26134-138">Especifica a frequência de recorrência.</span><span class="sxs-lookup"><span data-stu-id="26134-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="26134-139">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="26134-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26134-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="26134-140">None</span></span>
- <span data-ttu-id="26134-141">Segundo</span><span class="sxs-lookup"><span data-stu-id="26134-141">Second</span></span>
- <span data-ttu-id="26134-142">Minuto</span><span class="sxs-lookup"><span data-stu-id="26134-142">Minute</span></span>
- <span data-ttu-id="26134-143">Hora</span><span class="sxs-lookup"><span data-stu-id="26134-143">Hour</span></span>
- <span data-ttu-id="26134-144">Dia</span><span class="sxs-lookup"><span data-stu-id="26134-144">Day</span></span>
- <span data-ttu-id="26134-145">Semana</span><span class="sxs-lookup"><span data-stu-id="26134-145">Week</span></span>
- <span data-ttu-id="26134-146">Mês</span><span class="sxs-lookup"><span data-stu-id="26134-146">Month</span></span>
- <span data-ttu-id="26134-147">Ano Nem todos esses valores são suportados.</span><span class="sxs-lookup"><span data-stu-id="26134-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-148">-Rule</span><span class="sxs-lookup"><span data-stu-id="26134-148">-Rule</span></span>
<span data-ttu-id="26134-149">Especifica a lista de regras a adicionar ao perfil.</span><span class="sxs-lookup"><span data-stu-id="26134-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="26134-150">-ScheduleDay</span></span>
<span data-ttu-id="26134-151">Especifica os dias agendados.</span><span class="sxs-lookup"><span data-stu-id="26134-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="26134-152">-ScheduleHour</span></span>
<span data-ttu-id="26134-153">Especifica o horário agendado.</span><span class="sxs-lookup"><span data-stu-id="26134-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="26134-154">-ScheduleMinute</span></span>
<span data-ttu-id="26134-155">Especifica os minutos agendados.</span><span class="sxs-lookup"><span data-stu-id="26134-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="26134-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="26134-157">Especifica o fuso horário da agenda.</span><span class="sxs-lookup"><span data-stu-id="26134-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="26134-158">-StartTimeWindow</span></span>
<span data-ttu-id="26134-159">Especifica o início da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="26134-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="26134-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="26134-161">Especifica o fuso horário da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="26134-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26134-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26134-162">CommonParameters</span></span>
<span data-ttu-id="26134-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26134-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26134-164">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26134-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26134-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26134-165">INPUTS</span></span>

### <span data-ttu-id="26134-166">System.String</span><span class="sxs-lookup"><span data-stu-id="26134-166">System.String</span></span>

### <span data-ttu-id="26134-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="26134-167">System.DateTime</span></span>

### <span data-ttu-id="26134-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="26134-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="26134-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26134-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26134-170">System.Collections.Generic.List `1[[System.Nullable` 1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26134-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26134-171">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="26134-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="26134-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26134-172">OUTPUTS</span></span>

### <span data-ttu-id="26134-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="26134-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="26134-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="26134-174">NOTES</span></span>

## <span data-ttu-id="26134-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26134-175">RELATED LINKS</span></span>

[<span data-ttu-id="26134-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26134-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="26134-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="26134-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="26134-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26134-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="26134-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="26134-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="26134-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="26134-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


