---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116965"
---
# <span data-ttu-id="aad37-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aad37-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="aad37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aad37-102">SYNOPSIS</span></span>
<span data-ttu-id="aad37-103">Implanta uma configuração de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="aad37-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="aad37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aad37-104">SYNTAX</span></span>

### <span data-ttu-id="aad37-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aad37-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad37-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aad37-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad37-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aad37-107">DESCRIPTION</span></span>
<span data-ttu-id="aad37-108">O cmdlet **Start-AzAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (Configuração de Estado Desejado) na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="aad37-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="aad37-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aad37-109">EXAMPLES</span></span>

### <span data-ttu-id="aad37-110">Exemplo 1: Implantar uma configuração de nó DSC do Azure em Automação</span><span class="sxs-lookup"><span data-stu-id="aad37-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="aad37-111">O comando acima implanta a configuração de nó DSC chamada "Config01.Node1" para a determinada matriz bidimensional de Nomes de Nó.</span><span class="sxs-lookup"><span data-stu-id="aad37-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="aad37-112">A implantação acontece em estágios.</span><span class="sxs-lookup"><span data-stu-id="aad37-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="aad37-113">Exemplo 2: Agendar uma implantação de configuração de nó DSC do Azure em Automação</span><span class="sxs-lookup"><span data-stu-id="aad37-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="aad37-114">O comando acima agenda uma implantação de uma configuração de nó DSC chamada "Config01.Node1" para a determinada matriz bidimensional de Nomes de Nó.</span><span class="sxs-lookup"><span data-stu-id="aad37-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="aad37-115">A implantação acontece em estágios e será executada com base no cronograma.</span><span class="sxs-lookup"><span data-stu-id="aad37-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="aad37-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aad37-116">PARAMETERS</span></span>

### <span data-ttu-id="aad37-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aad37-117">-AutomationAccountName</span></span>
<span data-ttu-id="aad37-118">Especifica o nome da conta automação que contém a configuração DSC compilada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad37-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="aad37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad37-119">-DefaultProfile</span></span>
<span data-ttu-id="aad37-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aad37-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aad37-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="aad37-121">-Force</span></span>
<span data-ttu-id="aad37-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="aad37-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aad37-123">-InputObject</span></span>
<span data-ttu-id="aad37-124">Objeto de entrada para Piping</span><span class="sxs-lookup"><span data-stu-id="aad37-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aad37-125">-NodeConfigurationName</span></span>
<span data-ttu-id="aad37-126">Especifica o nome da configuração do nó DSC que este cmdlet implanta.</span><span class="sxs-lookup"><span data-stu-id="aad37-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="aad37-127">-NodeName</span></span>
<span data-ttu-id="aad37-128">Especifica os nomes dos nós para os quais a Configuração do Nó seria implantada.</span><span class="sxs-lookup"><span data-stu-id="aad37-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad37-129">-ResourceGroupName</span></span>
<span data-ttu-id="aad37-130">Especifica o nome de um grupo de recursos no qual este cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="aad37-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="aad37-131">-Agendar</span><span class="sxs-lookup"><span data-stu-id="aad37-131">-Schedule</span></span>
<span data-ttu-id="aad37-132">Objeto Agendamento de Automação para agendar o trabalho de implantação.</span><span class="sxs-lookup"><span data-stu-id="aad37-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aad37-133">-Confirm</span></span>
<span data-ttu-id="aad37-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad37-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad37-135">-WhatIf</span></span>
<span data-ttu-id="aad37-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aad37-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aad37-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aad37-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad37-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad37-138">CommonParameters</span></span>
<span data-ttu-id="aad37-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad37-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad37-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad37-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad37-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="aad37-141">INPUTS</span></span>

### <span data-ttu-id="aad37-142">System.String</span><span class="sxs-lookup"><span data-stu-id="aad37-142">System.String</span></span>

### <span data-ttu-id="aad37-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aad37-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="aad37-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="aad37-144">OUTPUTS</span></span>

### <span data-ttu-id="aad37-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aad37-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="aad37-146">Notas</span><span class="sxs-lookup"><span data-stu-id="aad37-146">NOTES</span></span>

## <span data-ttu-id="aad37-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aad37-147">RELATED LINKS</span></span>

[<span data-ttu-id="aad37-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="aad37-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="aad37-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="aad37-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="aad37-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aad37-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="aad37-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="aad37-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="aad37-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="aad37-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="aad37-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aad37-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
