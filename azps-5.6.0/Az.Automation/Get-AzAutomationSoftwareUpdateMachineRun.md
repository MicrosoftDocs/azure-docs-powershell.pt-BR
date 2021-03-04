---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 9a9a79dbd09c91a77af8982ea367498061b2ee1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901349"
---
# <span data-ttu-id="8cbc5-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="8cbc5-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="8cbc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbc5-103">Obtém uma lista de máquinas de configuração de atualização de software de automação do azure executados.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="8cbc5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8cbc5-104">SYNTAX</span></span>

### <span data-ttu-id="8cbc5-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8cbc5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cbc5-106">ById</span><span class="sxs-lookup"><span data-stu-id="8cbc5-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbc5-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="8cbc5-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbc5-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="8cbc5-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cbc5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8cbc5-109">DESCRIPTION</span></span>
<span data-ttu-id="8cbc5-110">Este cmdlet retorna uma lista de executações de máquina.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="8cbc5-111">Cada execução de atualização de software disparará uma máquina em execução para cada um dos dispositivos de destino de configuração de atualização de software.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="8cbc5-112">Para executar uma máquina específica, passe o parâmetro Id.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="8cbc5-113">Você pode listar todas as executações do computador, todas as executados para um computador específico, todas são executados com status específico passando os parâmetros correspondentes.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="8cbc5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-114">EXAMPLES</span></span>

### <span data-ttu-id="8cbc5-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cbc5-115">Example 1</span></span>
<span data-ttu-id="8cbc5-116">Este exemplo retorna todas as executações de máquina com falha para a máquina virtual do azure especificada.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="8cbc5-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-117">PARAMETERS</span></span>

### <span data-ttu-id="8cbc5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cbc5-118">-AutomationAccountName</span></span>
<span data-ttu-id="8cbc5-119">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-119">The automation account name.</span></span>

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

### <span data-ttu-id="8cbc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbc5-120">-DefaultProfile</span></span>
<span data-ttu-id="8cbc5-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbc5-122">-Id</span><span class="sxs-lookup"><span data-stu-id="8cbc5-122">-Id</span></span>
<span data-ttu-id="8cbc5-123">Id do computador de atualização de software executado.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="8cbc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cbc5-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-125">The resource group name.</span></span>

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

### <span data-ttu-id="8cbc5-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8cbc5-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="8cbc5-127">A atualização de software é executado.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbc5-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="8cbc5-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="8cbc5-129">Id da atualização de software executado.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbc5-130">-Status</span><span class="sxs-lookup"><span data-stu-id="8cbc5-130">-Status</span></span>
<span data-ttu-id="8cbc5-131">Status do computador executado.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbc5-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="8cbc5-132">-TargetComputer</span></span>
<span data-ttu-id="8cbc5-133">computador de destino para a operação do computador.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-133">target computer for the machine run.</span></span>
<span data-ttu-id="8cbc5-134">Pode ser um nome de computador não az ou uma ID de recurso VM do azure.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbc5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbc5-135">CommonParameters</span></span>
<span data-ttu-id="8cbc5-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbc5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbc5-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbc5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbc5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-138">INPUTS</span></span>

### <span data-ttu-id="8cbc5-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8cbc5-139">System.Guid</span></span>

### <span data-ttu-id="8cbc5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8cbc5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="8cbc5-141">System.Nullable'1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8cbc5-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8cbc5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8cbc5-142">System.String</span></span>

## <span data-ttu-id="8cbc5-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-143">OUTPUTS</span></span>

### <span data-ttu-id="8cbc5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="8cbc5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="8cbc5-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="8cbc5-145">NOTES</span></span>

## <span data-ttu-id="8cbc5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cbc5-146">RELATED LINKS</span></span>
