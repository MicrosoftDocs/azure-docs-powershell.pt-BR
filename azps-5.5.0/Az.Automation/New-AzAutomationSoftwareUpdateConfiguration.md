---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116972"
---
# <span data-ttu-id="d17fd-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d17fd-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d17fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d17fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d17fd-103">Cria uma configuração agendada de atualização de software de automação do azure.</span><span class="sxs-lookup"><span data-stu-id="d17fd-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="d17fd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d17fd-104">SYNTAX</span></span>

### <span data-ttu-id="d17fd-105">Windows (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d17fd-105">Windows (Default)</span></span>
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

### <span data-ttu-id="d17fd-106">Linux</span><span class="sxs-lookup"><span data-stu-id="d17fd-106">Linux</span></span>
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

## <span data-ttu-id="d17fd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d17fd-107">DESCRIPTION</span></span>
<span data-ttu-id="d17fd-108">Cria uma configuração de atualização de software que é executado em um cronograma para atualizar uma lista de computadores.</span><span class="sxs-lookup"><span data-stu-id="d17fd-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="d17fd-109">Os computadores incluem máquinas virtuais do Azure ou computadores não az.</span><span class="sxs-lookup"><span data-stu-id="d17fd-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="d17fd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d17fd-110">EXAMPLES</span></span>

### <span data-ttu-id="d17fd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d17fd-111">Example 1</span></span>
<span data-ttu-id="d17fd-112">Cria uma configuração de atualização de software para instalar atualizações críticas em duas máquinas virtuais do Windows azure uma vez a cada sábado às 21h.</span><span class="sxs-lookup"><span data-stu-id="d17fd-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="d17fd-113">A duração da atualização está definida como 2 horas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="d17fd-113">Update duration is set to 2 hours in this example.</span></span>

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

## <span data-ttu-id="d17fd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d17fd-114">PARAMETERS</span></span>

### <span data-ttu-id="d17fd-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d17fd-115">-AutomationAccountName</span></span>
<span data-ttu-id="d17fd-116">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="d17fd-116">The automation account name.</span></span>

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

### <span data-ttu-id="d17fd-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="d17fd-117">-AzureQuery</span></span>
<span data-ttu-id="d17fd-118">Consulta dinâmica do azure de grupo.</span><span class="sxs-lookup"><span data-stu-id="d17fd-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="d17fd-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="d17fd-119">-AzureVMResourceId</span></span>
<span data-ttu-id="d17fd-120">Ids de recursos para máquinas virtuais do azure.</span><span class="sxs-lookup"><span data-stu-id="d17fd-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="d17fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17fd-121">-DefaultProfile</span></span>
<span data-ttu-id="d17fd-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d17fd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17fd-123">-Duração</span><span class="sxs-lookup"><span data-stu-id="d17fd-123">-Duration</span></span>
<span data-ttu-id="d17fd-124">Duração máxima da atualização.</span><span class="sxs-lookup"><span data-stu-id="d17fd-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="d17fd-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d17fd-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="d17fd-126">Números de KB de atualizações excluídas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="d17fd-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d17fd-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="d17fd-128">Máscaras de pacote do Linux excluídas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="d17fd-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d17fd-129">-IncludedKbNumber</span></span>
<span data-ttu-id="d17fd-130">Números de KB de atualizações incluídas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="d17fd-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="d17fd-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="d17fd-132">Classificações de pacote do Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="d17fd-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d17fd-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="d17fd-134">Máscaras de pacote do Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="d17fd-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="d17fd-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="d17fd-136">Classificações incluídas do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d17fd-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="d17fd-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="d17fd-137">-Linux</span></span>
<span data-ttu-id="d17fd-138">Indica que a configuração de atualização de software que visa máquinas de sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="d17fd-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="d17fd-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="d17fd-139">-NonAzureComputer</span></span>
<span data-ttu-id="d17fd-140">Nomes de computador que não são do Az.</span><span class="sxs-lookup"><span data-stu-id="d17fd-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="d17fd-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="d17fd-141">-NonAzureQuery</span></span>
<span data-ttu-id="d17fd-142">Consulta de grupo dinâmico que não é do Azure.</span><span class="sxs-lookup"><span data-stu-id="d17fd-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="d17fd-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="d17fd-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="d17fd-144">Postar tarefa.</span><span class="sxs-lookup"><span data-stu-id="d17fd-144">Post task.</span></span>

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

### <span data-ttu-id="d17fd-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="d17fd-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="d17fd-146">Postar parâmetro da tarefa.</span><span class="sxs-lookup"><span data-stu-id="d17fd-146">Post task parameter.</span></span>

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

### <span data-ttu-id="d17fd-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="d17fd-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="d17fd-148">Pré-tarefa.</span><span class="sxs-lookup"><span data-stu-id="d17fd-148">Pre task.</span></span>

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

### <span data-ttu-id="d17fd-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="d17fd-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="d17fd-150">Parâmetro de pré-tarefa.</span><span class="sxs-lookup"><span data-stu-id="d17fd-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="d17fd-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="d17fd-151">-RebootOnly</span></span>
<span data-ttu-id="d17fd-152">Indica que a configuração de atualização de software reiniciará apenas os máquinas.</span><span class="sxs-lookup"><span data-stu-id="d17fd-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="d17fd-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="d17fd-153">-RebootSetting</span></span>
<span data-ttu-id="d17fd-154">Configuração de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="d17fd-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="d17fd-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17fd-155">-ResourceGroupName</span></span>
<span data-ttu-id="d17fd-156">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d17fd-156">The resource group name.</span></span>

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

### <span data-ttu-id="d17fd-157">-Agendar</span><span class="sxs-lookup"><span data-stu-id="d17fd-157">-Schedule</span></span>
<span data-ttu-id="d17fd-158">Agendar objeto usado para configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="d17fd-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="d17fd-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="d17fd-159">-Windows</span></span>
<span data-ttu-id="d17fd-160">Indica que a configuração de atualização de software destinado a computadores de sistema operacional windows.</span><span class="sxs-lookup"><span data-stu-id="d17fd-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="d17fd-161">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d17fd-161">-Confirm</span></span>
<span data-ttu-id="d17fd-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d17fd-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17fd-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17fd-163">-WhatIf</span></span>
<span data-ttu-id="d17fd-164">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d17fd-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d17fd-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d17fd-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17fd-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17fd-166">CommonParameters</span></span>
<span data-ttu-id="d17fd-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17fd-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17fd-168">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17fd-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17fd-169">Entradas</span><span class="sxs-lookup"><span data-stu-id="d17fd-169">INPUTS</span></span>

### <span data-ttu-id="d17fd-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="d17fd-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="d17fd-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d17fd-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d17fd-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d17fd-172">System.String[]</span></span>

### <span data-ttu-id="d17fd-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d17fd-173">System.TimeSpan</span></span>

### <span data-ttu-id="d17fd-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="d17fd-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="d17fd-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="d17fd-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="d17fd-176">System.String</span><span class="sxs-lookup"><span data-stu-id="d17fd-176">System.String</span></span>

## <span data-ttu-id="d17fd-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="d17fd-177">OUTPUTS</span></span>

### <span data-ttu-id="d17fd-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d17fd-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d17fd-179">Notas</span><span class="sxs-lookup"><span data-stu-id="d17fd-179">NOTES</span></span>

## <span data-ttu-id="d17fd-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d17fd-180">RELATED LINKS</span></span>
