---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609429"
---
# <span data-ttu-id="46741-101">Get-AzureRmAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="46741-101">Get-AzureRmAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="46741-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46741-102">SYNOPSIS</span></span>
<span data-ttu-id="46741-103">Obtém uma lista de execuções de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="46741-103">Gets a list of azure automation software update runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46741-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46741-104">SYNTAX</span></span>

### <span data-ttu-id="46741-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="46741-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46741-106">ById</span><span class="sxs-lookup"><span data-stu-id="46741-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46741-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="46741-107">BySucName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46741-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="46741-108">BySuc</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46741-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46741-109">DESCRIPTION</span></span>
<span data-ttu-id="46741-110">O cmdlet Get-AzureRmAutomationSoftwareUpdateRun retorna uma lista de execuções de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="46741-110">The Get-AzureRmAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="46741-111">Como uma configuração de atualização de software tem um cronograma associado, ela pode ser disparada várias vezes.</span><span class="sxs-lookup"><span data-stu-id="46741-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="46741-112">Cada vez que um cronograma for disparado, o resultado será a execução de uma atualização criada.</span><span class="sxs-lookup"><span data-stu-id="46741-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="46741-113">A execução de atualização é uma agregação do resultado de todas as execuções do computador.</span><span class="sxs-lookup"><span data-stu-id="46741-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="46741-114">Você pode obter execuções para configuração de atualização de software específica passando o parâmetro SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="46741-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="46741-115">Para obter uma execução específica, você precisa passar o parâmetro Name.</span><span class="sxs-lookup"><span data-stu-id="46741-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="46741-116">Você também pode listar execuções com status específico, executar direcionamento de sistema específico do Operatins ou iniciado após um tempo específico passando o parâmetro apropriado.</span><span class="sxs-lookup"><span data-stu-id="46741-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="46741-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46741-117">EXAMPLES</span></span>

### <span data-ttu-id="46741-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46741-118">Example 1</span></span>
<span data-ttu-id="46741-119">Este exemplo lista todas as execuções de atualização disparadas por uma configuração de atualização de software específica.</span><span class="sxs-lookup"><span data-stu-id="46741-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
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

## <span data-ttu-id="46741-120">OS</span><span class="sxs-lookup"><span data-stu-id="46741-120">PARAMETERS</span></span>

### <span data-ttu-id="46741-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="46741-121">-AutomationAccountName</span></span>
<span data-ttu-id="46741-122">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="46741-122">The automation account name.</span></span>

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

### <span data-ttu-id="46741-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46741-123">-DefaultProfile</span></span>
<span data-ttu-id="46741-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46741-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46741-125">-ID</span><span class="sxs-lookup"><span data-stu-id="46741-125">-Id</span></span>
<span data-ttu-id="46741-126">ID da execução da configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="46741-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="46741-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="46741-127">-OperatingSystem</span></span>
<span data-ttu-id="46741-128">O sistema operacional da execução.</span><span class="sxs-lookup"><span data-stu-id="46741-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="46741-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46741-129">-ResourceGroupName</span></span>
<span data-ttu-id="46741-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46741-130">The resource group name.</span></span>

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

### <span data-ttu-id="46741-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="46741-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="46741-132">A configuração de atualização de software acionou a execução.</span><span class="sxs-lookup"><span data-stu-id="46741-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="46741-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="46741-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="46741-134">Nome da configuração de atualização de software acionou a execução.</span><span class="sxs-lookup"><span data-stu-id="46741-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="46741-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="46741-135">-StartTime</span></span>
<span data-ttu-id="46741-136">Hora de início mínima da execução.</span><span class="sxs-lookup"><span data-stu-id="46741-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="46741-137">-Status</span><span class="sxs-lookup"><span data-stu-id="46741-137">-Status</span></span>
<span data-ttu-id="46741-138">Status da execução.</span><span class="sxs-lookup"><span data-stu-id="46741-138">Status of the run.</span></span>

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

### <span data-ttu-id="46741-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46741-139">CommonParameters</span></span>
<span data-ttu-id="46741-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46741-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46741-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46741-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46741-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46741-142">INPUTS</span></span>

### <span data-ttu-id="46741-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="46741-143">System.Guid</span></span>

### <span data-ttu-id="46741-144">System. String</span><span class="sxs-lookup"><span data-stu-id="46741-144">System.String</span></span>

### <span data-ttu-id="46741-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="46741-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="46741-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46741-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="46741-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46741-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="46741-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46741-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="46741-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46741-149">OUTPUTS</span></span>

### <span data-ttu-id="46741-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="46741-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="46741-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46741-151">NOTES</span></span>

## <span data-ttu-id="46741-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46741-152">RELATED LINKS</span></span>
