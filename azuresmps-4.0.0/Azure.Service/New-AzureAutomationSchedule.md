---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946219"
---
# <span data-ttu-id="6fe36-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe36-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="6fe36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fe36-102">SYNOPSIS</span></span>

<span data-ttu-id="6fe36-103">Cria um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="6fe36-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="6fe36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fe36-104">SYNTAX</span></span>

### <span data-ttu-id="6fe36-105">ByDaily (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fe36-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fe36-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="6fe36-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6fe36-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="6fe36-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6fe36-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fe36-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6fe36-109">O cmdlet **New-AzureAutomationSchedule** cria um cronograma na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe36-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6fe36-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fe36-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe36-111">Exemplo 1: criar uma agenda de uso único</span><span class="sxs-lookup"><span data-stu-id="6fe36-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="6fe36-112">O comando a seguir cria uma agenda que é executada uma vez na data atual às 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="6fe36-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="6fe36-113">Exemplo 2: criar um cronograma recorrente</span><span class="sxs-lookup"><span data-stu-id="6fe36-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="6fe36-114">Os comandos a seguir criam um novo cronograma que é executado às 1:00 PM todos os dias para um ano a partir do dia atual.</span><span class="sxs-lookup"><span data-stu-id="6fe36-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="6fe36-115">OS</span><span class="sxs-lookup"><span data-stu-id="6fe36-115">PARAMETERS</span></span>

### <span data-ttu-id="6fe36-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6fe36-116">-AutomationAccountName</span></span>
<span data-ttu-id="6fe36-117">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="6fe36-117">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="6fe36-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="6fe36-118">-DayInterval</span></span>
<span data-ttu-id="6fe36-119">Especifica um intervalo, em dias, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="6fe36-119">Specifies an interval, in days, for the schedule.</span></span>

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

### <span data-ttu-id="6fe36-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6fe36-120">-Description</span></span>
<span data-ttu-id="6fe36-121">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="6fe36-121">Specifies a description.</span></span>

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

### <span data-ttu-id="6fe36-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6fe36-122">-ExpiryTime</span></span>
<span data-ttu-id="6fe36-123">Especifica o tempo de expiração de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6fe36-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="6fe36-124">Uma cadeia de caracteres pode ser fornecida se puder ser convertida em um **DateTime** válido.</span><span class="sxs-lookup"><span data-stu-id="6fe36-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe36-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="6fe36-125">-HourInterval</span></span>
<span data-ttu-id="6fe36-126">Especifica um intervalo, em horas, para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="6fe36-126">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="6fe36-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fe36-127">-Name</span></span>
<span data-ttu-id="6fe36-128">Especifica um nome para o cronograma.</span><span class="sxs-lookup"><span data-stu-id="6fe36-128">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="6fe36-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="6fe36-129">-OneTime</span></span>
<span data-ttu-id="6fe36-130">Indica que essa operação cria uma agenda única.</span><span class="sxs-lookup"><span data-stu-id="6fe36-130">Indicates that this operation creates a one-time schedule.</span></span>

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

### <span data-ttu-id="6fe36-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6fe36-131">-Profile</span></span>
<span data-ttu-id="6fe36-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6fe36-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6fe36-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6fe36-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe36-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6fe36-134">-StartTime</span></span>
<span data-ttu-id="6fe36-135">Especifica a hora de início de um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6fe36-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="6fe36-136">Uma cadeia de caracteres pode ser fornecida se puder ser convertida em um **DateTime** válido.</span><span class="sxs-lookup"><span data-stu-id="6fe36-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe36-137">CommonParameters</span></span>
<span data-ttu-id="6fe36-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe36-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe36-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe36-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fe36-140">INPUTS</span></span>

## <span data-ttu-id="6fe36-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fe36-141">OUTPUTS</span></span>

### <span data-ttu-id="6fe36-142">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6fe36-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6fe36-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fe36-143">NOTES</span></span>

## <span data-ttu-id="6fe36-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fe36-144">RELATED LINKS</span></span>

[<span data-ttu-id="6fe36-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe36-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="6fe36-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe36-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="6fe36-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe36-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


