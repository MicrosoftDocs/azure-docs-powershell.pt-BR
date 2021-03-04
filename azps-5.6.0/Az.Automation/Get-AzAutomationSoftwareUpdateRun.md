---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: 49c8693984dc695f3d47b8066228cf2f82d5b267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901347"
---
# <span data-ttu-id="22e61-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="22e61-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="22e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e61-102">SYNOPSIS</span></span>
<span data-ttu-id="22e61-103">Obtém uma lista de atualizações de software de automação do azure executados.</span><span class="sxs-lookup"><span data-stu-id="22e61-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="22e61-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="22e61-104">SYNTAX</span></span>

### <span data-ttu-id="22e61-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="22e61-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e61-106">ById</span><span class="sxs-lookup"><span data-stu-id="22e61-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e61-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="22e61-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e61-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="22e61-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e61-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="22e61-109">DESCRIPTION</span></span>
<span data-ttu-id="22e61-110">O Get-AzAutomationSoftwareUpdateRun cmdlet retorna uma lista de executações de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="22e61-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="22e61-111">Como uma configuração de atualização de software tem uma agenda associada, ela pode ser disparada várias vezes.</span><span class="sxs-lookup"><span data-stu-id="22e61-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="22e61-112">Cada vez que um agendamento for disparado, uma atualização será criada.</span><span class="sxs-lookup"><span data-stu-id="22e61-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="22e61-113">A atualização é um agregado do resultado de todas as executações de máquina.</span><span class="sxs-lookup"><span data-stu-id="22e61-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="22e61-114">Você pode obter execução para configuração de atualização de software específica passando o parâmetro SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="22e61-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="22e61-115">Para obter uma correção específica, você precisa passar o parâmetro name.</span><span class="sxs-lookup"><span data-stu-id="22e61-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="22e61-116">Você também pode listar executados com status específico, executando o sistema operacional específico ou executados iniciados após um horário específico passando o parâmetro apropriado.</span><span class="sxs-lookup"><span data-stu-id="22e61-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="22e61-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22e61-117">EXAMPLES</span></span>

### <span data-ttu-id="22e61-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22e61-118">Example 1</span></span>
<span data-ttu-id="22e61-119">Este exemplo lista todas as atualizações disparadas por uma configuração de atualização de software específica.</span><span class="sxs-lookup"><span data-stu-id="22e61-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="22e61-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="22e61-120">PARAMETERS</span></span>

### <span data-ttu-id="22e61-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22e61-121">-AutomationAccountName</span></span>
<span data-ttu-id="22e61-122">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="22e61-122">The automation account name.</span></span>

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

### <span data-ttu-id="22e61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e61-123">-DefaultProfile</span></span>
<span data-ttu-id="22e61-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22e61-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e61-125">-Id</span><span class="sxs-lookup"><span data-stu-id="22e61-125">-Id</span></span>
<span data-ttu-id="22e61-126">ID da configuração de atualização de software em execução.</span><span class="sxs-lookup"><span data-stu-id="22e61-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="22e61-127">-OperatingSystem</span></span>
<span data-ttu-id="22e61-128">O sistema operacional da operação.</span><span class="sxs-lookup"><span data-stu-id="22e61-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e61-129">-ResourceGroupName</span></span>
<span data-ttu-id="22e61-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22e61-130">The resource group name.</span></span>

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

### <span data-ttu-id="22e61-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="22e61-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="22e61-132">A configuração de atualização de software disparou a execução.</span><span class="sxs-lookup"><span data-stu-id="22e61-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="22e61-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="22e61-134">O nome da configuração de atualização de software disparou a execução.</span><span class="sxs-lookup"><span data-stu-id="22e61-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="22e61-135">-StartTime</span></span>
<span data-ttu-id="22e61-136">Tempo mínimo de início da executar.</span><span class="sxs-lookup"><span data-stu-id="22e61-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-137">-Status</span><span class="sxs-lookup"><span data-stu-id="22e61-137">-Status</span></span>
<span data-ttu-id="22e61-138">Status da executar.</span><span class="sxs-lookup"><span data-stu-id="22e61-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e61-139">CommonParameters</span></span>
<span data-ttu-id="22e61-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e61-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e61-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e61-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22e61-142">INPUTS</span></span>

### <span data-ttu-id="22e61-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="22e61-143">System.Guid</span></span>

### <span data-ttu-id="22e61-144">System.String</span><span class="sxs-lookup"><span data-stu-id="22e61-144">System.String</span></span>

### <span data-ttu-id="22e61-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="22e61-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="22e61-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="22e61-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22e61-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="22e61-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22e61-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="22e61-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="22e61-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="22e61-149">OUTPUTS</span></span>

### <span data-ttu-id="22e61-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="22e61-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="22e61-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="22e61-151">NOTES</span></span>

## <span data-ttu-id="22e61-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22e61-152">RELATED LINKS</span></span>
