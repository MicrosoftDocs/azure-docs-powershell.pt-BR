---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 1f8b68ac04a563dbec44b0ed43bca0a54015154d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887440"
---
# <span data-ttu-id="6e1e9-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="6e1e9-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="6e1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1e9-103">Cria uma nova política de instantâneo do Azure NetApp Files (ANF) para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="6e1e9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e1e9-104">SYNTAX</span></span>

### <span data-ttu-id="6e1e9-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e1e9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e1e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e1e9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e1e9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e1e9-107">DESCRIPTION</span></span>
<span data-ttu-id="6e1e9-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova política de instantâneo para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="6e1e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-109">EXAMPLES</span></span>

### <span data-ttu-id="6e1e9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e1e9-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="6e1e9-111">Este comando cria a nova política de instantâneo ANF para a conta ANF denominada "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="6e1e9-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="6e1e9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-112">PARAMETERS</span></span>

### <span data-ttu-id="6e1e9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e1e9-113">-AccountName</span></span>
<span data-ttu-id="6e1e9-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6e1e9-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6e1e9-115">-AccountObject</span></span>
<span data-ttu-id="6e1e9-116">A conta do novo objeto De política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="6e1e9-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="6e1e9-117">-DailySchedule</span></span>
<span data-ttu-id="6e1e9-118">Uma matriz hashtable que representa o agendamento diário</span><span class="sxs-lookup"><span data-stu-id="6e1e9-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1e9-119">-DefaultProfile</span></span>
<span data-ttu-id="6e1e9-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1e9-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6e1e9-121">-Enabled</span></span>
<span data-ttu-id="6e1e9-122">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="6e1e9-122">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="6e1e9-123">-HourlySchedule</span></span>
<span data-ttu-id="6e1e9-124">Uma matriz hashtable que representa o agendamento por hora</span><span class="sxs-lookup"><span data-stu-id="6e1e9-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="6e1e9-125">-Location</span></span>
<span data-ttu-id="6e1e9-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="6e1e9-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="6e1e9-127">-MonthlySchedule</span></span>
<span data-ttu-id="6e1e9-128">Uma matriz hashtable que representa o agendamento montly</span><span class="sxs-lookup"><span data-stu-id="6e1e9-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6e1e9-129">-Name</span></span>
<span data-ttu-id="6e1e9-130">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="6e1e9-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="6e1e9-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="6e1e9-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e1e9-133">-Tag</span></span>
<span data-ttu-id="6e1e9-134">Uma matriz hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="6e1e9-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="6e1e9-135">-WeeklySchedule</span></span>
<span data-ttu-id="6e1e9-136">Uma matriz hashtable que representa o agendamento montly</span><span class="sxs-lookup"><span data-stu-id="6e1e9-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e1e9-137">-Confirm</span></span>
<span data-ttu-id="6e1e9-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1e9-139">-WhatIf</span></span>
<span data-ttu-id="6e1e9-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e1e9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1e9-142">CommonParameters</span></span>
<span data-ttu-id="6e1e9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1e9-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e1e9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1e9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-145">INPUTS</span></span>

### <span data-ttu-id="6e1e9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6e1e9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6e1e9-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-147">OUTPUTS</span></span>

### <span data-ttu-id="6e1e9-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="6e1e9-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="6e1e9-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e1e9-149">NOTES</span></span>

## <span data-ttu-id="6e1e9-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e1e9-150">RELATED LINKS</span></span>
