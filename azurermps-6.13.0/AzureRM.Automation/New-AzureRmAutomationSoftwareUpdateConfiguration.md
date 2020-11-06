---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431449"
---
# <span data-ttu-id="d3aa8-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3aa8-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d3aa8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d3aa8-103">Cria uma configuração agendada de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3aa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3aa8-104">SYNTAX</span></span>

### <span data-ttu-id="d3aa8-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3aa8-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3aa8-106">Linux</span><span class="sxs-lookup"><span data-stu-id="d3aa8-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3aa8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="d3aa8-108">Cria uma configuração de atualização de software que é executada em um cronograma para atualizar uma lista de computadores.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="d3aa8-109">Os computadores incluem máquinas virtuais do Azure ou computadores não pertencentes ao Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="d3aa8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3aa8-110">EXAMPLES</span></span>

### <span data-ttu-id="d3aa8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3aa8-111">Example 1</span></span>
<span data-ttu-id="d3aa8-112">Cria uma configuração de atualização de software para instalar atualizações críticas em duas máquinas virtuais do Windows Azure a cada sábado 9PM.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="d3aa8-113">A duração da atualização é definida como 2 horas neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="d3aa8-114">OS</span><span class="sxs-lookup"><span data-stu-id="d3aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="d3aa8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3aa8-115">-AutomationAccountName</span></span>
<span data-ttu-id="d3aa8-116">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-116">The automation account name.</span></span>

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

### <span data-ttu-id="d3aa8-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="d3aa8-117">-AzureVMResourceId</span></span>
<span data-ttu-id="d3aa8-118">IDs de recursos para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="d3aa8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3aa8-119">-DefaultProfile</span></span>
<span data-ttu-id="d3aa8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3aa8-121">-Duração</span><span class="sxs-lookup"><span data-stu-id="d3aa8-121">-Duration</span></span>
<span data-ttu-id="d3aa8-122">Duração máxima da atualização.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="d3aa8-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d3aa8-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="d3aa8-124">KB número de atualizações excluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="d3aa8-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d3aa8-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="d3aa8-126">Máscaras de pacotes Linux excluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="d3aa8-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d3aa8-127">-IncludedKbNumber</span></span>
<span data-ttu-id="d3aa8-128">KB número de atualizações incluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="d3aa8-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="d3aa8-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="d3aa8-130">Classificações de pacotes Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="d3aa8-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d3aa8-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="d3aa8-132">Máscaras de pacotes Linux incluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="d3aa8-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="d3aa8-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="d3aa8-134">Classificações de atualização do Windows incluídas.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="d3aa8-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="d3aa8-135">-Linux</span></span>
<span data-ttu-id="d3aa8-136">Indica que a configuração de atualização de software está direcionada para computadores com sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="d3aa8-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="d3aa8-137">-NonAzureComputer</span></span>
<span data-ttu-id="d3aa8-138">Nomes de computador não Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="d3aa8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3aa8-139">-ResourceGroupName</span></span>
<span data-ttu-id="d3aa8-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-140">The resource group name.</span></span>

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

### <span data-ttu-id="d3aa8-141">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="d3aa8-141">-Schedule</span></span>
<span data-ttu-id="d3aa8-142">Agendar objeto usado para configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="d3aa8-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="d3aa8-143">-Windows</span></span>
<span data-ttu-id="d3aa8-144">Indica que a configuração de atualização de software está direcionada para máquinas do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="d3aa8-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3aa8-145">-Confirm</span></span>
<span data-ttu-id="d3aa8-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3aa8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3aa8-147">-WhatIf</span></span>
<span data-ttu-id="d3aa8-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3aa8-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3aa8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3aa8-150">CommonParameters</span></span>
<span data-ttu-id="d3aa8-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3aa8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3aa8-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3aa8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3aa8-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3aa8-153">INPUTS</span></span>

### <span data-ttu-id="d3aa8-154">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="d3aa8-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="d3aa8-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3aa8-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d3aa8-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="d3aa8-156">System.String[]</span></span>

### <span data-ttu-id="d3aa8-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d3aa8-157">System.TimeSpan</span></span>

### <span data-ttu-id="d3aa8-158">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="d3aa8-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="d3aa8-159">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="d3aa8-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="d3aa8-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d3aa8-160">System.String</span></span>

## <span data-ttu-id="d3aa8-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3aa8-161">OUTPUTS</span></span>

### <span data-ttu-id="d3aa8-162">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3aa8-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d3aa8-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3aa8-163">NOTES</span></span>

## <span data-ttu-id="d3aa8-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3aa8-164">RELATED LINKS</span></span>
