---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114735"
---
# <span data-ttu-id="50f3b-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="50f3b-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="50f3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="50f3b-103">Cria uma nova política de instantâneo do Azure NetApp Files (ANF) para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="50f3b-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="50f3b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50f3b-104">SYNTAX</span></span>

### <span data-ttu-id="50f3b-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="50f3b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f3b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f3b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f3b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="50f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="50f3b-108">O cmdlet **New-AzNetAppFilesActiveDirectory** cria uma nova política de instantâneo para uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="50f3b-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="50f3b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="50f3b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50f3b-110">Example 1</span></span>
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

<span data-ttu-id="50f3b-111">Esse comando cria a nova política de instantâneo ANF para a conta ANF chamada conta "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="50f3b-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="50f3b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50f3b-112">PARAMETERS</span></span>

### <span data-ttu-id="50f3b-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="50f3b-113">-AccountName</span></span>
<span data-ttu-id="50f3b-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="50f3b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="50f3b-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="50f3b-115">-AccountObject</span></span>
<span data-ttu-id="50f3b-116">A Conta do novo objeto de Política de Instantâneo</span><span class="sxs-lookup"><span data-stu-id="50f3b-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="50f3b-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="50f3b-117">-DailySchedule</span></span>
<span data-ttu-id="50f3b-118">Uma matriz de tabela hash que representa a Agenda diária</span><span class="sxs-lookup"><span data-stu-id="50f3b-118">A hashtable array which represents the daily Schedule</span></span>

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

### <span data-ttu-id="50f3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f3b-119">-DefaultProfile</span></span>
<span data-ttu-id="50f3b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50f3b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f3b-121">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="50f3b-121">-Enabled</span></span>
<span data-ttu-id="50f3b-122">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="50f3b-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="50f3b-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="50f3b-123">-HourlySchedule</span></span>
<span data-ttu-id="50f3b-124">Uma matriz de tabela hash que representa o Cronograma por hora</span><span class="sxs-lookup"><span data-stu-id="50f3b-124">A hashtable array which represents the hourly Schedule</span></span>

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

### <span data-ttu-id="50f3b-125">-Local</span><span class="sxs-lookup"><span data-stu-id="50f3b-125">-Location</span></span>
<span data-ttu-id="50f3b-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="50f3b-126">The location of the resource</span></span>

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

### <span data-ttu-id="50f3b-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="50f3b-127">-MonthlySchedule</span></span>
<span data-ttu-id="50f3b-128">Uma matriz de tabela hash que representa o cronograma montly</span><span class="sxs-lookup"><span data-stu-id="50f3b-128">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="50f3b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="50f3b-129">-Name</span></span>
<span data-ttu-id="50f3b-130">O nome da política de instantâneo da ANF</span><span class="sxs-lookup"><span data-stu-id="50f3b-130">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="50f3b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f3b-131">-ResourceGroupName</span></span>
<span data-ttu-id="50f3b-132">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="50f3b-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="50f3b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="50f3b-133">-Tag</span></span>
<span data-ttu-id="50f3b-134">Uma matriz de tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="50f3b-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="50f3b-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="50f3b-135">-WeeklySchedule</span></span>
<span data-ttu-id="50f3b-136">Uma matriz de tabela hash que representa o cronograma montly</span><span class="sxs-lookup"><span data-stu-id="50f3b-136">A hashtable array which represents the montly Schedule</span></span>

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

### <span data-ttu-id="50f3b-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="50f3b-137">-Confirm</span></span>
<span data-ttu-id="50f3b-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50f3b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f3b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f3b-139">-WhatIf</span></span>
<span data-ttu-id="50f3b-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="50f3b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50f3b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50f3b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f3b-142">CommonParameters</span></span>
<span data-ttu-id="50f3b-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f3b-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50f3b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f3b-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="50f3b-145">INPUTS</span></span>

### <span data-ttu-id="50f3b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="50f3b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="50f3b-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="50f3b-147">OUTPUTS</span></span>

### <span data-ttu-id="50f3b-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="50f3b-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="50f3b-149">Notas</span><span class="sxs-lookup"><span data-stu-id="50f3b-149">NOTES</span></span>

## <span data-ttu-id="50f3b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50f3b-150">RELATED LINKS</span></span>
