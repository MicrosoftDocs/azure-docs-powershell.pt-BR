---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 0672e7ab292046b79ceaad61446c30c210bcb535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433329"
---
# <span data-ttu-id="05737-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05737-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="05737-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05737-102">SYNOPSIS</span></span>
<span data-ttu-id="05737-103">Cria um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="05737-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05737-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05737-104">SYNTAX</span></span>

### <span data-ttu-id="05737-105">ByDaily (padrão)</span><span class="sxs-lookup"><span data-stu-id="05737-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05737-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="05737-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05737-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="05737-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05737-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="05737-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05737-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="05737-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05737-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="05737-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05737-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05737-111">DESCRIPTION</span></span>
<span data-ttu-id="05737-112">O cmdlet **New-AzureRmAutomationSchedule** cria um cronograma na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="05737-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="05737-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05737-113">EXAMPLES</span></span>

### <span data-ttu-id="05737-114">Exemplo 1: criar um cronograma único na hora local</span><span class="sxs-lookup"><span data-stu-id="05737-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="05737-115">O primeiro comando obtém a ID de fuso horário do sistema e a armazena na variável $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="05737-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="05737-116">O segundo comando cria uma agenda que é executada uma vez na data atual em 11:00 PM no fuso horário especificado...</span><span class="sxs-lookup"><span data-stu-id="05737-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="05737-117">Exemplo 2: criar um cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="05737-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05737-118">O primeiro comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="05737-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="05737-119">Especifique uma hora que tenha pelo menos cinco minutos no futuro.</span><span class="sxs-lookup"><span data-stu-id="05737-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="05737-120">O segundo comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="05737-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="05737-121">O comando especifica um tempo futuro.</span><span class="sxs-lookup"><span data-stu-id="05737-121">The command specifies a future time.</span></span>
<span data-ttu-id="05737-122">O comando final cria um cronograma diário chamado Schedule02 para começar no horário armazenado no $StartDate e expirar no horário armazenado no $EndDate.</span><span class="sxs-lookup"><span data-stu-id="05737-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="05737-123">Exemplo 3: criar um cronograma recorrente semanal</span><span class="sxs-lookup"><span data-stu-id="05737-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05737-124">O primeiro comando cria um objeto Date usando o cmdlet **Get-Date** e, em seguida, armazena o objeto na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="05737-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="05737-125">O segundo comando cria uma matriz de dias da semana que contém segunda-feira, terça-feira, quarta-feira e sexta-feira.</span><span class="sxs-lookup"><span data-stu-id="05737-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="05737-126">O comando final cria um plano diário chamado Schedule03 que vai funcionar de segunda a sexta-feira, a cada semana, em 13:00.</span><span class="sxs-lookup"><span data-stu-id="05737-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="05737-127">O cronograma nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="05737-127">The schedule will never expire.</span></span>

## <span data-ttu-id="05737-128">OS</span><span class="sxs-lookup"><span data-stu-id="05737-128">PARAMETERS</span></span>

### <span data-ttu-id="05737-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05737-129">-AutomationAccountName</span></span>
<span data-ttu-id="05737-130">Especifica o nome de uma conta de automação para a qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="05737-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="05737-131">-DayInterval</span></span>
<span data-ttu-id="05737-132">Especifica um intervalo, em dias, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="05737-133">Se você não especificar esse parâmetro e não especificar o parâmetro *OneTime* , o valor padrão será um (1).</span><span class="sxs-lookup"><span data-stu-id="05737-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="05737-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="05737-134">-DayOfWeek</span></span>
<span data-ttu-id="05737-135">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="05737-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="05737-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="05737-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="05737-137">Especifica a ocorrência da semana no mês em que a agenda é executada.</span><span class="sxs-lookup"><span data-stu-id="05737-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="05737-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="05737-138">psdx_paramvalues</span></span>
- <span data-ttu-id="05737-139">um</span><span class="sxs-lookup"><span data-stu-id="05737-139">1</span></span>
- <span data-ttu-id="05737-140">2</span><span class="sxs-lookup"><span data-stu-id="05737-140">2</span></span>
- <span data-ttu-id="05737-141">3D</span><span class="sxs-lookup"><span data-stu-id="05737-141">3</span></span>
- <span data-ttu-id="05737-142">4</span><span class="sxs-lookup"><span data-stu-id="05737-142">4</span></span>
- <span data-ttu-id="05737-143">-1</span><span class="sxs-lookup"><span data-stu-id="05737-143">-1</span></span>
- <span data-ttu-id="05737-144">Primeiros</span><span class="sxs-lookup"><span data-stu-id="05737-144">First</span></span>
- <span data-ttu-id="05737-145">Secundária</span><span class="sxs-lookup"><span data-stu-id="05737-145">Second</span></span>
- <span data-ttu-id="05737-146">Terceiriza</span><span class="sxs-lookup"><span data-stu-id="05737-146">Third</span></span>
- <span data-ttu-id="05737-147">Fourth</span><span class="sxs-lookup"><span data-stu-id="05737-147">Fourth</span></span>
- <span data-ttu-id="05737-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="05737-148">LastDay</span></span>

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

### <span data-ttu-id="05737-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="05737-149">-DaysOfMonth</span></span>
<span data-ttu-id="05737-150">Especifica uma lista de dias do mês para o cronograma mensal.</span><span class="sxs-lookup"><span data-stu-id="05737-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="05737-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="05737-151">-DaysOfWeek</span></span>
<span data-ttu-id="05737-152">Especifica uma lista de dias da semana para o cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="05737-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="05737-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05737-153">-DefaultProfile</span></span>
<span data-ttu-id="05737-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="05737-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05737-155">-Descrição</span><span class="sxs-lookup"><span data-stu-id="05737-155">-Description</span></span>
<span data-ttu-id="05737-156">Especifica uma descrição para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="05737-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="05737-157">-ExpiryTime</span></span>
<span data-ttu-id="05737-158">Especifica o tempo de expiração de um cronograma como um objeto **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="05737-158">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="05737-159">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="05737-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="05737-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="05737-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="05737-161">Indica que esse objeto de agendamento será usado para agendar uma configuração de atualização de software</span><span class="sxs-lookup"><span data-stu-id="05737-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="05737-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="05737-162">-HourInterval</span></span>
<span data-ttu-id="05737-163">Especifica um intervalo, em horas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="05737-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="05737-164">-MonthInterval</span></span>
<span data-ttu-id="05737-165">Especifica um intervalo, em meses, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="05737-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="05737-166">-Name</span></span>
<span data-ttu-id="05737-167">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="05737-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="05737-168">-OneTime</span></span>
<span data-ttu-id="05737-169">Especifica que o cmdlet cria um agendamento de uma vez.</span><span class="sxs-lookup"><span data-stu-id="05737-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="05737-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05737-170">-ResourceGroupName</span></span>
<span data-ttu-id="05737-171">Especifica o nome de um grupo de recursos para o qual esse cmdlet cria um cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="05737-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05737-172">-StartTime</span></span>
<span data-ttu-id="05737-173">Especifica a hora de início de um cronograma como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="05737-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="05737-174">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="05737-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="05737-175">Se o parâmetro *timezone* for especificado, o deslocamento será ignorado e o fuso horário especificado será usado.</span><span class="sxs-lookup"><span data-stu-id="05737-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="05737-176">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="05737-176">-TimeZone</span></span>
<span data-ttu-id="05737-177">Especifica o fuso horário do cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="05737-178">Esta cadeia de caracteres pode ser a ID da IANA ou a ID do fuso horário do Windows.</span><span class="sxs-lookup"><span data-stu-id="05737-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="05737-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="05737-179">-WeekInterval</span></span>
<span data-ttu-id="05737-180">Especifica um intervalo, em semanas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="05737-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="05737-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05737-181">CommonParameters</span></span>
<span data-ttu-id="05737-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05737-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05737-183">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05737-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05737-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05737-184">INPUTS</span></span>

### <span data-ttu-id="05737-185">System. String</span><span class="sxs-lookup"><span data-stu-id="05737-185">System.String</span></span>

### <span data-ttu-id="05737-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="05737-186">System.DateTimeOffset</span></span>

## <span data-ttu-id="05737-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05737-187">OUTPUTS</span></span>

### <span data-ttu-id="05737-188">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="05737-188">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="05737-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05737-189">NOTES</span></span>

## <span data-ttu-id="05737-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05737-190">RELATED LINKS</span></span>

[<span data-ttu-id="05737-191">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05737-191">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="05737-192">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05737-192">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="05737-193">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05737-193">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)

