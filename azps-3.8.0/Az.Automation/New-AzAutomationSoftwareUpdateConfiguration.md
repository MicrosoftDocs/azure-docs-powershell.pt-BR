---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944958"
---
# <span data-ttu-id="13106-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13106-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="13106-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13106-102">SYNOPSIS</span></span>
<span data-ttu-id="13106-103">Cria uma configuração agendada de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="13106-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="13106-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13106-104">SYNTAX</span></span>

### <span data-ttu-id="13106-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="13106-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13106-106">Linux</span><span class="sxs-lookup"><span data-stu-id="13106-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13106-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13106-107">DESCRIPTION</span></span>
<span data-ttu-id="13106-108">Cria uma configuração de atualização de software que é executada em um cronograma para atualizar uma lista de computadores.</span><span class="sxs-lookup"><span data-stu-id="13106-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="13106-109">Os computadores incluem máquinas virtuais do Azure ou computadores não AZ.</span><span class="sxs-lookup"><span data-stu-id="13106-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="13106-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13106-110">EXAMPLES</span></span>

### <span data-ttu-id="13106-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13106-111">Example 1</span></span>
<span data-ttu-id="13106-112">Cria uma configuração de atualização de software para instalar atualizações críticas em duas máquinas virtuais do Windows Azure a cada sábado 9PM.</span><span class="sxs-lookup"><span data-stu-id="13106-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="13106-113">A duração da atualização é definida como 2 horas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="13106-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="13106-114">OS</span><span class="sxs-lookup"><span data-stu-id="13106-114">PARAMETERS</span></span>

### <span data-ttu-id="13106-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13106-115">-AutomationAccountName</span></span>
<span data-ttu-id="13106-116">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="13106-116">The automation account name.</span></span>

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

### <span data-ttu-id="13106-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="13106-117">-AzureQuery</span></span>
<span data-ttu-id="13106-118">Consulta do Azure em grupo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="13106-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="13106-119">-AzureVMResourceId</span></span>
<span data-ttu-id="13106-120">IDs de recursos para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="13106-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13106-121">-DefaultProfile</span></span>
<span data-ttu-id="13106-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13106-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-123">-Duração</span><span class="sxs-lookup"><span data-stu-id="13106-123">-Duration</span></span>
<span data-ttu-id="13106-124">Duração máxima da atualização.</span><span class="sxs-lookup"><span data-stu-id="13106-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="13106-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="13106-126">KB número de atualizações excluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="13106-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="13106-128">Máscaras de pacotes Linux excluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="13106-129">-IncludedKbNumber</span></span>
<span data-ttu-id="13106-130">KB número de atualizações incluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="13106-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="13106-132">Classificações de pacotes Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="13106-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="13106-134">Máscaras de pacotes Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="13106-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="13106-136">Classificações de atualização do Windows incluídas.</span><span class="sxs-lookup"><span data-stu-id="13106-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="13106-137">-Linux</span></span>
<span data-ttu-id="13106-138">Indica que a configuração de atualização de software está direcionada para computadores com sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="13106-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="13106-139">-NonAzureComputer</span></span>
<span data-ttu-id="13106-140">Nomes de computador não AZ.</span><span class="sxs-lookup"><span data-stu-id="13106-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="13106-141">-NonAzureQuery</span></span>
<span data-ttu-id="13106-142">Grupo dinâmico não consulta do Azure.</span><span class="sxs-lookup"><span data-stu-id="13106-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="13106-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="13106-144">Publicar tarefa.</span><span class="sxs-lookup"><span data-stu-id="13106-144">Post task.</span></span>

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

### <span data-ttu-id="13106-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="13106-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="13106-146">Postar parâmetro de tarefa.</span><span class="sxs-lookup"><span data-stu-id="13106-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="13106-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="13106-148">Pré tarefa.</span><span class="sxs-lookup"><span data-stu-id="13106-148">Pre task.</span></span>

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

### <span data-ttu-id="13106-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="13106-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="13106-150">Parâmetro pre-Task.</span><span class="sxs-lookup"><span data-stu-id="13106-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="13106-151">-RebootOnly</span></span>
<span data-ttu-id="13106-152">Indica que a configuração da atualização de software somente reinicializará as máquinas.</span><span class="sxs-lookup"><span data-stu-id="13106-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="13106-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="13106-153">-RebootSetting</span></span>
<span data-ttu-id="13106-154">Configuração de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="13106-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13106-155">-ResourceGroupName</span></span>
<span data-ttu-id="13106-156">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13106-156">The resource group name.</span></span>

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

### <span data-ttu-id="13106-157">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="13106-157">-Schedule</span></span>
<span data-ttu-id="13106-158">Agendar objeto usado para configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="13106-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="13106-159">-Windows</span></span>
<span data-ttu-id="13106-160">Indica que a configuração de atualização de software está direcionada para máquinas do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="13106-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13106-161">-Confirm</span></span>
<span data-ttu-id="13106-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13106-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13106-163">-WhatIf</span></span>
<span data-ttu-id="13106-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13106-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13106-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13106-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13106-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13106-166">CommonParameters</span></span>
<span data-ttu-id="13106-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13106-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13106-168">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13106-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13106-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13106-169">INPUTS</span></span>

### <span data-ttu-id="13106-170">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="13106-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="13106-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13106-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="13106-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="13106-172">System.String[]</span></span>

### <span data-ttu-id="13106-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="13106-173">System.TimeSpan</span></span>

### <span data-ttu-id="13106-174">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="13106-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="13106-175">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="13106-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="13106-176">System. String</span><span class="sxs-lookup"><span data-stu-id="13106-176">System.String</span></span>

## <span data-ttu-id="13106-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13106-177">OUTPUTS</span></span>

### <span data-ttu-id="13106-178">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="13106-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="13106-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13106-179">NOTES</span></span>

## <span data-ttu-id="13106-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13106-180">RELATED LINKS</span></span>
