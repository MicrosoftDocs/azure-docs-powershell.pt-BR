---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: ee7321f6021c6e4b2f56209d6c6a7fd5a6ff79a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601563"
---
# <span data-ttu-id="54b7a-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="54b7a-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="54b7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="54b7a-103">Cria um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="54b7a-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="54b7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54b7a-104">SYNTAX</span></span>

### <span data-ttu-id="54b7a-105">ByDaily (padrão)</span><span class="sxs-lookup"><span data-stu-id="54b7a-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54b7a-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="54b7a-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54b7a-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="54b7a-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54b7a-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="54b7a-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54b7a-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="54b7a-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54b7a-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="54b7a-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54b7a-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54b7a-111">DESCRIPTION</span></span>
<span data-ttu-id="54b7a-112">O cmdlet **New-AzAutomationSchedule** cria um cronograma na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="54b7a-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="54b7a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54b7a-113">EXAMPLES</span></span>

### <span data-ttu-id="54b7a-114">Exemplo 1: criar um cronograma único na hora local</span><span class="sxs-lookup"><span data-stu-id="54b7a-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="54b7a-115">O primeiro comando obtém a ID de fuso horário do sistema e a armazena na variável $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="54b7a-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="54b7a-116">O segundo comando cria uma agenda que é executada uma vez na data atual em 11:00 PM no fuso horário especificado...</span><span class="sxs-lookup"><span data-stu-id="54b7a-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="54b7a-117">Exemplo 2: criar um cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="54b7a-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="54b7a-118">O primeiro comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="54b7a-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="54b7a-119">Especifique uma hora que tenha pelo menos cinco minutos no futuro.</span><span class="sxs-lookup"><span data-stu-id="54b7a-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="54b7a-120">O segundo comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="54b7a-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="54b7a-121">O comando especifica um tempo futuro.</span><span class="sxs-lookup"><span data-stu-id="54b7a-121">The command specifies a future time.</span></span>
<span data-ttu-id="54b7a-122">O comando final cria um cronograma diário chamado Schedule02 para começar no horário armazenado no $StartDate e expirar no horário armazenado no $EndDate.</span><span class="sxs-lookup"><span data-stu-id="54b7a-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="54b7a-123">Exemplo 3: criar um cronograma recorrente semanal</span><span class="sxs-lookup"><span data-stu-id="54b7a-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="54b7a-124">O primeiro comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="54b7a-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="54b7a-125">O segundo comando cria uma matriz de dias da semana que contém segunda-feira, terça-feira, quarta-feira e sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="54b7a-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="54b7a-126">O comando final cria um plano diário chamado Schedule03 que vai funcionar de segunda a sexta-feira, a cada semana, em 13:00.</span><span class="sxs-lookup"><span data-stu-id="54b7a-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="54b7a-127">O cronograma nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="54b7a-127">The schedule will never expire.</span></span>

## <span data-ttu-id="54b7a-128">OS</span><span class="sxs-lookup"><span data-stu-id="54b7a-128">PARAMETERS</span></span>

### <span data-ttu-id="54b7a-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54b7a-129">-AutomationAccountName</span></span>
<span data-ttu-id="54b7a-130">Especifica o nome de uma conta de automação para a qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="54b7a-131">-DayInterval</span></span>
<span data-ttu-id="54b7a-132">Especifica um intervalo, em dias, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="54b7a-133">Se você não especificar esse parâmetro e não especificar o parâmetro *OneTime* , o valor padrão será um (1).</span><span class="sxs-lookup"><span data-stu-id="54b7a-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="54b7a-134">-DayOfWeek</span></span>
<span data-ttu-id="54b7a-135">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="54b7a-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="54b7a-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="54b7a-137">Especifica a ocorrência da semana no mês em que a agenda é executada.</span><span class="sxs-lookup"><span data-stu-id="54b7a-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="54b7a-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="54b7a-138">psdx_paramvalues</span></span>
- <span data-ttu-id="54b7a-139">um</span><span class="sxs-lookup"><span data-stu-id="54b7a-139">1</span></span>
- <span data-ttu-id="54b7a-140">2</span><span class="sxs-lookup"><span data-stu-id="54b7a-140">2</span></span>
- <span data-ttu-id="54b7a-141">3D</span><span class="sxs-lookup"><span data-stu-id="54b7a-141">3</span></span>
- <span data-ttu-id="54b7a-142">4</span><span class="sxs-lookup"><span data-stu-id="54b7a-142">4</span></span>
- <span data-ttu-id="54b7a-143">-1</span><span class="sxs-lookup"><span data-stu-id="54b7a-143">-1</span></span>
- <span data-ttu-id="54b7a-144">Primeiros</span><span class="sxs-lookup"><span data-stu-id="54b7a-144">First</span></span>
- <span data-ttu-id="54b7a-145">Secundária</span><span class="sxs-lookup"><span data-stu-id="54b7a-145">Second</span></span>
- <span data-ttu-id="54b7a-146">Terceiriza</span><span class="sxs-lookup"><span data-stu-id="54b7a-146">Third</span></span>
- <span data-ttu-id="54b7a-147">Fourth</span><span class="sxs-lookup"><span data-stu-id="54b7a-147">Fourth</span></span>
- <span data-ttu-id="54b7a-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="54b7a-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="54b7a-149">-DaysOfMonth</span></span>
<span data-ttu-id="54b7a-150">Especifica uma lista de dias do mês para o cronograma mensal.</span><span class="sxs-lookup"><span data-stu-id="54b7a-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="54b7a-151">-DaysOfWeek</span></span>
<span data-ttu-id="54b7a-152">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="54b7a-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b7a-153">-DefaultProfile</span></span>
<span data-ttu-id="54b7a-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54b7a-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b7a-155">-Descrição</span><span class="sxs-lookup"><span data-stu-id="54b7a-155">-Description</span></span>
<span data-ttu-id="54b7a-156">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="54b7a-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="54b7a-157">-ExpiryTime</span></span>
<span data-ttu-id="54b7a-158">Especifica o tempo de expiração de um cronograma como um objeto **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="54b7a-158">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="54b7a-159">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="54b7a-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="54b7a-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="54b7a-161">Indica que esse objeto de agendamento será usado para agendar uma configuração de atualização de software</span><span class="sxs-lookup"><span data-stu-id="54b7a-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="54b7a-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="54b7a-162">-HourInterval</span></span>
<span data-ttu-id="54b7a-163">Especifica um intervalo, em horas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="54b7a-164">-MonthInterval</span></span>
<span data-ttu-id="54b7a-165">Especifica um intervalo, em meses, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="54b7a-166">-Name</span></span>
<span data-ttu-id="54b7a-167">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="54b7a-168">-OneTime</span></span>
<span data-ttu-id="54b7a-169">Especifica que o cmdlet cria um agendamento de uma vez.</span><span class="sxs-lookup"><span data-stu-id="54b7a-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b7a-170">-ResourceGroupName</span></span>
<span data-ttu-id="54b7a-171">Especifica o nome de um grupo de recursos para o qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="54b7a-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="54b7a-172">-StartTime</span></span>
<span data-ttu-id="54b7a-173">Especifica a hora de início de um cronograma como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="54b7a-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="54b7a-174">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="54b7a-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="54b7a-175">Se o parâmetro *timezone* for especificado, o deslocamento será ignorado e o fuso horário especificado será usado.</span><span class="sxs-lookup"><span data-stu-id="54b7a-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-176">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="54b7a-176">-TimeZone</span></span>
<span data-ttu-id="54b7a-177">Especifica o fuso horário do cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="54b7a-178">Esta cadeia de caracteres pode ser a ID da IANA ou a ID do fuso horário do Windows.</span><span class="sxs-lookup"><span data-stu-id="54b7a-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="54b7a-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="54b7a-179">-WeekInterval</span></span>
<span data-ttu-id="54b7a-180">Especifica um intervalo, em semanas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="54b7a-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b7a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b7a-181">CommonParameters</span></span>
<span data-ttu-id="54b7a-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b7a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b7a-183">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b7a-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b7a-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54b7a-184">INPUTS</span></span>

### <span data-ttu-id="54b7a-185">System. String</span><span class="sxs-lookup"><span data-stu-id="54b7a-185">System.String</span></span>

### <span data-ttu-id="54b7a-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54b7a-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="54b7a-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54b7a-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54b7a-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54b7a-188">OUTPUTS</span></span>

### <span data-ttu-id="54b7a-189">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="54b7a-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="54b7a-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54b7a-190">NOTES</span></span>

## <span data-ttu-id="54b7a-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54b7a-191">RELATED LINKS</span></span>

[<span data-ttu-id="54b7a-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="54b7a-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="54b7a-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="54b7a-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="54b7a-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="54b7a-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


