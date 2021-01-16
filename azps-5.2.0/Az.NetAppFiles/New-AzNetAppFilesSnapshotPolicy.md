---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262611"
---
# <span data-ttu-id="52b5a-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="52b5a-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="52b5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="52b5a-103">Cria uma nova política de instantâneo do Azure NetApp Files (ANF) para uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="52b5a-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="52b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52b5a-104">SYNTAX</span></span>

### <span data-ttu-id="52b5a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="52b5a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b5a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b5a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b5a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="52b5a-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova política de instantâneo para uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="52b5a-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="52b5a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="52b5a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52b5a-110">Example 1</span></span>
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

<span data-ttu-id="52b5a-111">Esse comando cria a nova ANF política de instantâneo para ANF conta denominada conta "myaccount".</span><span class="sxs-lookup"><span data-stu-id="52b5a-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="52b5a-112">OS</span><span class="sxs-lookup"><span data-stu-id="52b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="52b5a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52b5a-113">-AccountName</span></span>
<span data-ttu-id="52b5a-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="52b5a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="52b5a-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="52b5a-115">-AccountObject</span></span>
<span data-ttu-id="52b5a-116">A conta para o novo objeto de política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="52b5a-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="52b5a-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="52b5a-117">-DailySchedule</span></span>
<span data-ttu-id="52b5a-118">Uma matriz de Hashtable que representa o cronograma diário</span><span class="sxs-lookup"><span data-stu-id="52b5a-118">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="52b5a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b5a-119">-DefaultProfile</span></span>
<span data-ttu-id="52b5a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52b5a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b5a-121">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="52b5a-121">-Enabled</span></span>
<span data-ttu-id="52b5a-122">A propriedade para decidir se política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="52b5a-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="52b5a-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="52b5a-123">-HourlySchedule</span></span>
<span data-ttu-id="52b5a-124">Uma matriz de Hashtable que representa o agendamento por hora</span><span class="sxs-lookup"><span data-stu-id="52b5a-124">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="52b5a-125">-Local</span><span class="sxs-lookup"><span data-stu-id="52b5a-125">-Location</span></span>
<span data-ttu-id="52b5a-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="52b5a-126">The location of the resource</span></span>

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

### <span data-ttu-id="52b5a-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="52b5a-127">-MonthlySchedule</span></span>
<span data-ttu-id="52b5a-128">Uma matriz de Hashtable que representa a agenda mensal</span><span class="sxs-lookup"><span data-stu-id="52b5a-128">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="52b5a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b5a-129">-Name</span></span>
<span data-ttu-id="52b5a-130">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="52b5a-130">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="52b5a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b5a-131">-ResourceGroupName</span></span>
<span data-ttu-id="52b5a-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="52b5a-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="52b5a-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="52b5a-133">-Tag</span></span>
<span data-ttu-id="52b5a-134">Uma matriz de Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="52b5a-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="52b5a-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="52b5a-135">-WeeklySchedule</span></span>
<span data-ttu-id="52b5a-136">Uma matriz de Hashtable que representa a agenda mensal</span><span class="sxs-lookup"><span data-stu-id="52b5a-136">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="52b5a-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52b5a-137">-Confirm</span></span>
<span data-ttu-id="52b5a-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b5a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b5a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b5a-139">-WhatIf</span></span>
<span data-ttu-id="52b5a-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52b5a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b5a-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52b5a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b5a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b5a-142">CommonParameters</span></span>
<span data-ttu-id="52b5a-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b5a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b5a-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52b5a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b5a-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52b5a-145">INPUTS</span></span>

### <span data-ttu-id="52b5a-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="52b5a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="52b5a-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52b5a-147">OUTPUTS</span></span>

### <span data-ttu-id="52b5a-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="52b5a-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="52b5a-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52b5a-149">NOTES</span></span>

## <span data-ttu-id="52b5a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52b5a-150">RELATED LINKS</span></span>
