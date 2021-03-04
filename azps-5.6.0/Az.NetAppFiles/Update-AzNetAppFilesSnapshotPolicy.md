---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cf099afe95eec37e070cc2b09d30b7f4b2766b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887396"
---
# <span data-ttu-id="693ab-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="693ab-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="693ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="693ab-102">SYNOPSIS</span></span>
<span data-ttu-id="693ab-103">Atualiza uma política de instantâneo do Azure NetApp Files (ANF) para os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="693ab-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="693ab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="693ab-104">SYNTAX</span></span>

### <span data-ttu-id="693ab-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="693ab-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="693ab-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693ab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="693ab-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693ab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="693ab-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="693ab-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="693ab-109">DESCRIPTION</span></span>
<span data-ttu-id="693ab-110">O cmdlet **Update-AzNetAppFilesSnapshotPolicy** modifica uma política de instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="693ab-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="693ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="693ab-111">EXAMPLES</span></span>

### <span data-ttu-id="693ab-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="693ab-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="693ab-113">Este comando altera a política de backup da ANF "MySnapshotPolicy" para ter o hourlySchedule determinado.</span><span class="sxs-lookup"><span data-stu-id="693ab-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="693ab-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="693ab-114">PARAMETERS</span></span>

### <span data-ttu-id="693ab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="693ab-115">-AccountName</span></span>
<span data-ttu-id="693ab-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="693ab-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="693ab-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="693ab-117">-AccountObject</span></span>
<span data-ttu-id="693ab-118">A conta do novo objeto De política de instantâneo</span><span class="sxs-lookup"><span data-stu-id="693ab-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="693ab-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="693ab-119">-DailySchedule</span></span>
<span data-ttu-id="693ab-120">Uma matriz hashtable que representa o agendamento diário</span><span class="sxs-lookup"><span data-stu-id="693ab-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693ab-121">-DefaultProfile</span></span>
<span data-ttu-id="693ab-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="693ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="693ab-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="693ab-123">-Enabled</span></span>
<span data-ttu-id="693ab-124">A propriedade para decidir a política está habilitada ou não</span><span class="sxs-lookup"><span data-stu-id="693ab-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="693ab-125">-HourlySchedule</span></span>
<span data-ttu-id="693ab-126">Uma matriz hashtable que representa o agendamento por hora</span><span class="sxs-lookup"><span data-stu-id="693ab-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="693ab-127">-InputObject</span></span>
<span data-ttu-id="693ab-128">O objeto instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="693ab-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-129">-Location</span><span class="sxs-lookup"><span data-stu-id="693ab-129">-Location</span></span>
<span data-ttu-id="693ab-130">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="693ab-130">The location of the resource</span></span>

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

### <span data-ttu-id="693ab-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="693ab-131">-MonthlySchedule</span></span>
<span data-ttu-id="693ab-132">Uma matriz hashtable que representa o agendamento montly</span><span class="sxs-lookup"><span data-stu-id="693ab-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-133">-Name</span><span class="sxs-lookup"><span data-stu-id="693ab-133">-Name</span></span>
<span data-ttu-id="693ab-134">O nome da política de instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="693ab-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693ab-135">-ResourceGroupName</span></span>
<span data-ttu-id="693ab-136">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="693ab-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="693ab-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="693ab-137">-ResourceId</span></span>
<span data-ttu-id="693ab-138">A id de recurso da Política de Instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="693ab-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="693ab-139">-Tag</span></span>
<span data-ttu-id="693ab-140">Uma matriz hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="693ab-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="693ab-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="693ab-141">-WeeklySchedule</span></span>
<span data-ttu-id="693ab-142">Uma matriz hashtable que representa o agendamento montly</span><span class="sxs-lookup"><span data-stu-id="693ab-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693ab-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="693ab-143">-Confirm</span></span>
<span data-ttu-id="693ab-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="693ab-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="693ab-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="693ab-145">-WhatIf</span></span>
<span data-ttu-id="693ab-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="693ab-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="693ab-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="693ab-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="693ab-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693ab-148">CommonParameters</span></span>
<span data-ttu-id="693ab-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="693ab-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693ab-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="693ab-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693ab-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="693ab-151">INPUTS</span></span>

### <span data-ttu-id="693ab-152">System.String</span><span class="sxs-lookup"><span data-stu-id="693ab-152">System.String</span></span>

### <span data-ttu-id="693ab-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="693ab-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="693ab-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="693ab-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="693ab-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="693ab-155">OUTPUTS</span></span>

### <span data-ttu-id="693ab-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="693ab-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="693ab-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="693ab-157">NOTES</span></span>

## <span data-ttu-id="693ab-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="693ab-158">RELATED LINKS</span></span>
