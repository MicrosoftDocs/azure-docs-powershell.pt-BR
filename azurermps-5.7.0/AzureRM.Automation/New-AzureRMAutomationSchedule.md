---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440137"
---
# <span data-ttu-id="a73b0-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a73b0-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="a73b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a73b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a73b0-103">Cria um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="a73b0-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a73b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a73b0-104">SYNTAX</span></span>

### <span data-ttu-id="a73b0-105">ByDaily (padrão)</span><span class="sxs-lookup"><span data-stu-id="a73b0-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a73b0-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="a73b0-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a73b0-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="a73b0-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a73b0-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a73b0-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a73b0-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="a73b0-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a73b0-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="a73b0-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a73b0-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a73b0-111">DESCRIPTION</span></span>
<span data-ttu-id="a73b0-112">O cmdlet **New-AzureRmAutomationSchedule** cria um cronograma na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a73b0-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="a73b0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a73b0-113">EXAMPLES</span></span>

### <span data-ttu-id="a73b0-114">Exemplo 1: criar um cronograma único na hora local</span><span class="sxs-lookup"><span data-stu-id="a73b0-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="a73b0-115">O primeiro comando obtém a ID de fuso horário do sistema e a armazena na variável $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="a73b0-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="a73b0-116">O segundo comando cria uma agenda que é executada uma vez na data atual em 11:00 PM no fuso horário especificado...</span><span class="sxs-lookup"><span data-stu-id="a73b0-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="a73b0-117">Exemplo 2: criar um cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="a73b0-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a73b0-118">O primeiro comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="a73b0-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="a73b0-119">Especifique uma hora que tenha pelo menos cinco minutos no futuro.</span><span class="sxs-lookup"><span data-stu-id="a73b0-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="a73b0-120">O segundo comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a73b0-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="a73b0-121">O comando especifica um tempo futuro.</span><span class="sxs-lookup"><span data-stu-id="a73b0-121">The command specifies a future time.</span></span>

<span data-ttu-id="a73b0-122">O comando final cria um cronograma diário chamado Schedule01 para começar no horário armazenado no $StartDate e expirar no horário armazenado no $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a73b0-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="a73b0-123">OS</span><span class="sxs-lookup"><span data-stu-id="a73b0-123">PARAMETERS</span></span>

### <span data-ttu-id="a73b0-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a73b0-124">-AutomationAccountName</span></span>
<span data-ttu-id="a73b0-125">Especifica o nome de uma conta de automação para a qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="a73b0-126">-DayInterval</span></span>
<span data-ttu-id="a73b0-127">Especifica um intervalo, em dias, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="a73b0-128">Se você não especificar esse parâmetro e não especificar o parâmetro *OneTime* , o valor padrão será um (1).</span><span class="sxs-lookup"><span data-stu-id="a73b0-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a73b0-129">-DayOfWeek</span></span>
<span data-ttu-id="a73b0-130">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="a73b0-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="a73b0-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="a73b0-132">Especifica a ocorrência da semana no mês em que a agenda é executada.</span><span class="sxs-lookup"><span data-stu-id="a73b0-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="a73b0-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a73b0-133">psdx_paramvalues</span></span>

- <span data-ttu-id="a73b0-134">um</span><span class="sxs-lookup"><span data-stu-id="a73b0-134">1</span></span>
- <span data-ttu-id="a73b0-135">2</span><span class="sxs-lookup"><span data-stu-id="a73b0-135">2</span></span>
- <span data-ttu-id="a73b0-136">3D</span><span class="sxs-lookup"><span data-stu-id="a73b0-136">3</span></span>
- <span data-ttu-id="a73b0-137">4</span><span class="sxs-lookup"><span data-stu-id="a73b0-137">4</span></span>
- <span data-ttu-id="a73b0-138">-1</span><span class="sxs-lookup"><span data-stu-id="a73b0-138">-1</span></span>
- <span data-ttu-id="a73b0-139">Primeiros</span><span class="sxs-lookup"><span data-stu-id="a73b0-139">First</span></span>
- <span data-ttu-id="a73b0-140">Secundária</span><span class="sxs-lookup"><span data-stu-id="a73b0-140">Second</span></span>
- <span data-ttu-id="a73b0-141">Terceiriza</span><span class="sxs-lookup"><span data-stu-id="a73b0-141">Third</span></span>
- <span data-ttu-id="a73b0-142">Fourth</span><span class="sxs-lookup"><span data-stu-id="a73b0-142">Fourth</span></span>
- <span data-ttu-id="a73b0-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="a73b0-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="a73b0-144">-DaysOfMonth</span></span>
<span data-ttu-id="a73b0-145">Especifica uma lista de dias do mês para o cronograma mensal.</span><span class="sxs-lookup"><span data-stu-id="a73b0-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a73b0-146">-DaysOfWeek</span></span>
<span data-ttu-id="a73b0-147">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="a73b0-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73b0-148">-DefaultProfile</span></span>
<span data-ttu-id="a73b0-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a73b0-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a73b0-150">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a73b0-150">-Description</span></span>
<span data-ttu-id="a73b0-151">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a73b0-152">-ExpiryTime</span></span>
<span data-ttu-id="a73b0-153">Especifica o tempo de expiração de um cronograma como um objeto **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="a73b0-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="a73b0-154">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="a73b0-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="a73b0-155">-HourInterval</span></span>
<span data-ttu-id="a73b0-156">Especifica um intervalo, em horas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-157">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="a73b0-157">-MonthInterval</span></span>
<span data-ttu-id="a73b0-158">Especifica um intervalo, em meses, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="a73b0-159">-Name</span></span>
<span data-ttu-id="a73b0-160">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-161">-OneTime</span><span class="sxs-lookup"><span data-stu-id="a73b0-161">-OneTime</span></span>
<span data-ttu-id="a73b0-162">Especifica que o cmdlet cria um agendamento de uma vez.</span><span class="sxs-lookup"><span data-stu-id="a73b0-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73b0-163">-ResourceGroupName</span></span>
<span data-ttu-id="a73b0-164">Especifica o nome de um grupo de recursos para o qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a73b0-165">-StartTime</span></span>
<span data-ttu-id="a73b0-166">Especifica a hora de início de um cronograma como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="a73b0-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a73b0-167">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="a73b0-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a73b0-168">.</span><span class="sxs-lookup"><span data-stu-id="a73b0-168">.</span></span> <span data-ttu-id="a73b0-169">Se o parâmetro *timezone* for especificado, o deslocamento será ignorado e o fuso horário especificado será usado.</span><span class="sxs-lookup"><span data-stu-id="a73b0-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-170">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="a73b0-170">-TimeZone</span></span>
<span data-ttu-id="a73b0-171">Especifica o fuso horário do cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="a73b0-172">Esta cadeia de caracteres pode ser a ID da IANA ou a ID do fuso horário do Windows.</span><span class="sxs-lookup"><span data-stu-id="a73b0-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-173">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="a73b0-173">-WeekInterval</span></span>
<span data-ttu-id="a73b0-174">Especifica um intervalo, em semanas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="a73b0-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73b0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73b0-175">CommonParameters</span></span>
<span data-ttu-id="a73b0-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73b0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73b0-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73b0-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73b0-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a73b0-178">INPUTS</span></span>

### <span data-ttu-id="a73b0-179">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a73b0-179">None</span></span>
<span data-ttu-id="a73b0-180">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a73b0-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a73b0-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a73b0-181">OUTPUTS</span></span>

### <span data-ttu-id="a73b0-182">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a73b0-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a73b0-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a73b0-183">NOTES</span></span>

## <span data-ttu-id="a73b0-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a73b0-184">RELATED LINKS</span></span>

[<span data-ttu-id="a73b0-185">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a73b0-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a73b0-186">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a73b0-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a73b0-187">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a73b0-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


