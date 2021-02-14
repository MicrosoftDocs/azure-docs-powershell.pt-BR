---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116978"
---
# <span data-ttu-id="7f973-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f973-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="7f973-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f973-102">SYNOPSIS</span></span>
<span data-ttu-id="7f973-103">Cria um cronograma de Automação.</span><span class="sxs-lookup"><span data-stu-id="7f973-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="7f973-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f973-104">SYNTAX</span></span>

### <span data-ttu-id="7f973-105">ByDaily (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7f973-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f973-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="7f973-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f973-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="7f973-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f973-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7f973-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f973-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="7f973-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f973-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="7f973-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f973-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f973-111">DESCRIPTION</span></span>
<span data-ttu-id="7f973-112">O cmdlet **New-AzAutomationSchedule** cria um cronograma no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7f973-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="7f973-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f973-113">EXAMPLES</span></span>

### <span data-ttu-id="7f973-114">Exemplo 1: Criar um cronograma único em horário local</span><span class="sxs-lookup"><span data-stu-id="7f973-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="7f973-115">O primeiro comando obtém a ID de fuso horário do sistema e a armazena na variável $TimeZone dados.</span><span class="sxs-lookup"><span data-stu-id="7f973-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="7f973-116">O segundo comando cria um cronograma que é executado uma vez na data atual às 23:00 no fuso horário especificado.</span><span class="sxs-lookup"><span data-stu-id="7f973-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="7f973-117">Exemplo 2: Criar um cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="7f973-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7f973-118">O primeiro comando cria um objeto de data usando o cmdlet Obter **Data** e, em seguida, armazena o objeto na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="7f973-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="7f973-119">Especifique um tempo que seja pelo menos cinco minutos no futuro.</span><span class="sxs-lookup"><span data-stu-id="7f973-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="7f973-120">O segundo comando cria um objeto de data usando o cmdlet Obter **Data** e, em seguida, armazena o objeto na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="7f973-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="7f973-121">O comando especifica uma hora futura.</span><span class="sxs-lookup"><span data-stu-id="7f973-121">The command specifies a future time.</span></span>
<span data-ttu-id="7f973-122">O comando final cria uma agenda diária chamada Agenda02 para começar no horário armazenado no $StartDate e expirar no horário armazenado no $EndDate.</span><span class="sxs-lookup"><span data-stu-id="7f973-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="7f973-123">Exemplo 3: Criar um cronograma recorrente semanal</span><span class="sxs-lookup"><span data-stu-id="7f973-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7f973-124">O primeiro comando cria um objeto de data usando o cmdlet Obter **Data** e, em seguida, armazena o objeto na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="7f973-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="7f973-125">O segundo comando cria uma matriz de dias da semana que contém segunda- feira, terça-feira, quarta-feira, quinta-feira e sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="7f973-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="7f973-126">O comando final cria um cronograma diário chamado Agenda03 que será executado de segunda a sexta-feira a cada semana às 13:00.</span><span class="sxs-lookup"><span data-stu-id="7f973-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="7f973-127">O cronograma nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="7f973-127">The schedule will never expire.</span></span>

## <span data-ttu-id="7f973-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f973-128">PARAMETERS</span></span>

### <span data-ttu-id="7f973-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7f973-129">-AutomationAccountName</span></span>
<span data-ttu-id="7f973-130">Especifica o nome de uma conta de Automação para a qual este cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="7f973-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="7f973-131">-DayInterval</span></span>
<span data-ttu-id="7f973-132">Especifica um intervalo, em dias, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="7f973-133">Se você não especificar esse parâmetro e não especificar o parâmetro *OneTime,* o valor padrão será um (1).</span><span class="sxs-lookup"><span data-stu-id="7f973-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="7f973-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7f973-134">-DayOfWeek</span></span>
<span data-ttu-id="7f973-135">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="7f973-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="7f973-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="7f973-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="7f973-137">Especifica a ocorrência da semana dentro do mês em que o cronograma é executado.</span><span class="sxs-lookup"><span data-stu-id="7f973-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="7f973-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="7f973-138">psdx_paramvalues</span></span>
- <span data-ttu-id="7f973-139">1</span><span class="sxs-lookup"><span data-stu-id="7f973-139">1</span></span>
- <span data-ttu-id="7f973-140">2</span><span class="sxs-lookup"><span data-stu-id="7f973-140">2</span></span>
- <span data-ttu-id="7f973-141">3</span><span class="sxs-lookup"><span data-stu-id="7f973-141">3</span></span>
- <span data-ttu-id="7f973-142">4</span><span class="sxs-lookup"><span data-stu-id="7f973-142">4</span></span>
- <span data-ttu-id="7f973-143">-1</span><span class="sxs-lookup"><span data-stu-id="7f973-143">-1</span></span>
- <span data-ttu-id="7f973-144">Primeiro</span><span class="sxs-lookup"><span data-stu-id="7f973-144">First</span></span>
- <span data-ttu-id="7f973-145">Segundo</span><span class="sxs-lookup"><span data-stu-id="7f973-145">Second</span></span>
- <span data-ttu-id="7f973-146">Terceiro</span><span class="sxs-lookup"><span data-stu-id="7f973-146">Third</span></span>
- <span data-ttu-id="7f973-147">Quarto</span><span class="sxs-lookup"><span data-stu-id="7f973-147">Fourth</span></span>
- <span data-ttu-id="7f973-148">Último Dia</span><span class="sxs-lookup"><span data-stu-id="7f973-148">LastDay</span></span>

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

### <span data-ttu-id="7f973-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="7f973-149">-DaysOfMonth</span></span>
<span data-ttu-id="7f973-150">Especifica uma lista de dias do mês para o cronograma mensal.</span><span class="sxs-lookup"><span data-stu-id="7f973-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="7f973-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="7f973-151">-DaysOfWeek</span></span>
<span data-ttu-id="7f973-152">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="7f973-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="7f973-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f973-153">-DefaultProfile</span></span>
<span data-ttu-id="7f973-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7f973-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f973-155">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7f973-155">-Description</span></span>
<span data-ttu-id="7f973-156">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="7f973-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7f973-157">-ExpiryTime</span></span>
<span data-ttu-id="7f973-158">Especifica o tempo de expiração de um cronograma como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="7f973-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7f973-159">Você pode especificar uma cadeia de caracteres que pode ser convertida em **um DateTimeOffset válido.**</span><span class="sxs-lookup"><span data-stu-id="7f973-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="7f973-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f973-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="7f973-161">Indica que esse objeto de agendamento será usado para agendar uma configuração de atualização de software</span><span class="sxs-lookup"><span data-stu-id="7f973-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="7f973-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="7f973-162">-HourInterval</span></span>
<span data-ttu-id="7f973-163">Especifica um intervalo, em horas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="7f973-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="7f973-164">-MonthInterval</span></span>
<span data-ttu-id="7f973-165">Especifica um intervalo, em Meses, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="7f973-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f973-166">-Name</span></span>
<span data-ttu-id="7f973-167">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="7f973-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="7f973-168">-OneTime</span></span>
<span data-ttu-id="7f973-169">Especifica que o cmdlet cria um cronograma único.</span><span class="sxs-lookup"><span data-stu-id="7f973-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="7f973-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f973-170">-ResourceGroupName</span></span>
<span data-ttu-id="7f973-171">Especifica o nome de um grupo de recursos para o qual este cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="7f973-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7f973-172">-StartTime</span></span>
<span data-ttu-id="7f973-173">Especifica a hora de início de um cronograma como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="7f973-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7f973-174">Você pode especificar uma cadeia de caracteres que pode ser convertida em **um DateTimeOffset válido.**</span><span class="sxs-lookup"><span data-stu-id="7f973-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="7f973-175">Se o *parâmetro Fuso* Horário for especificado, o deslocamento será ignorado e o fuso horário especificado será usado.</span><span class="sxs-lookup"><span data-stu-id="7f973-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="7f973-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="7f973-176">-TimeZone</span></span>
<span data-ttu-id="7f973-177">Especifica o fuso horário do cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="7f973-178">Essa cadeia de caracteres pode ser a ID do IANA ou a ID do Fuso Horário do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f973-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="7f973-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="7f973-179">-WeekInterval</span></span>
<span data-ttu-id="7f973-180">Especifica um intervalo, em semanas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="7f973-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="7f973-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f973-181">CommonParameters</span></span>
<span data-ttu-id="7f973-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f973-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f973-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f973-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f973-184">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f973-184">INPUTS</span></span>

### <span data-ttu-id="7f973-185">System.String</span><span class="sxs-lookup"><span data-stu-id="7f973-185">System.String</span></span>

### <span data-ttu-id="7f973-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7f973-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="7f973-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f973-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f973-188">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f973-188">OUTPUTS</span></span>

### <span data-ttu-id="7f973-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="7f973-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7f973-190">Notas</span><span class="sxs-lookup"><span data-stu-id="7f973-190">NOTES</span></span>

## <span data-ttu-id="7f973-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f973-191">RELATED LINKS</span></span>

[<span data-ttu-id="7f973-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f973-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="7f973-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f973-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="7f973-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7f973-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


