---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 21fe2cfb9a9022cad2ce9947b1e5919a6ebc268b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426447"
---
# <span data-ttu-id="915d2-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="915d2-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="915d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="915d2-102">SYNOPSIS</span></span>
<span data-ttu-id="915d2-103">Implanta uma configuração de nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="915d2-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="915d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="915d2-104">SYNTAX</span></span>

### <span data-ttu-id="915d2-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="915d2-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="915d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="915d2-106">ByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="915d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="915d2-107">DESCRIPTION</span></span>
<span data-ttu-id="915d2-108">O cmdlet **Start-AzureRmAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó de configuração de estado desejada (DSC) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="915d2-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="915d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="915d2-109">EXAMPLES</span></span>

### <span data-ttu-id="915d2-110">Exemplo 1: implantar uma configuração de nó DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="915d2-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="915d2-111">O comando acima implanta a configuração do nó DSC chamada "Config01. Node1" para a matriz bidimensional fornecida dos nomes dos nós.</span><span class="sxs-lookup"><span data-stu-id="915d2-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="915d2-112">A implantação ocorre em uma maneira em estágios.</span><span class="sxs-lookup"><span data-stu-id="915d2-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="915d2-113">Exemplo 2: agendar uma implantação de configuração do nó DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="915d2-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="915d2-114">O comando acima agenda uma implantação de uma configuração de nó DSC chamada "Config01. Node1" para a matriz bidimensional fornecida dos nomes de nó.</span><span class="sxs-lookup"><span data-stu-id="915d2-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="915d2-115">A implantação ocorre em uma maneira em estágios e será executada com base no cronograma.</span><span class="sxs-lookup"><span data-stu-id="915d2-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="915d2-116">OS</span><span class="sxs-lookup"><span data-stu-id="915d2-116">PARAMETERS</span></span>

### <span data-ttu-id="915d2-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="915d2-117">-AutomationAccountName</span></span>
<span data-ttu-id="915d2-118">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="915d2-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="915d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915d2-119">-DefaultProfile</span></span>
<span data-ttu-id="915d2-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="915d2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="915d2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="915d2-121">-Force</span></span>
<span data-ttu-id="915d2-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="915d2-122">ps_force</span></span>

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

### <span data-ttu-id="915d2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="915d2-123">-InputObject</span></span>
<span data-ttu-id="915d2-124">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="915d2-124">Input object for Piping</span></span>

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

### <span data-ttu-id="915d2-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="915d2-125">-NodeConfigurationName</span></span>
<span data-ttu-id="915d2-126">Especifica o nome da configuração do nó DSC que este cmdlet implanta.</span><span class="sxs-lookup"><span data-stu-id="915d2-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="915d2-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="915d2-127">-NodeName</span></span>
<span data-ttu-id="915d2-128">Especifica os nomes dos nós para os quais a configuração de nó será implantada.</span><span class="sxs-lookup"><span data-stu-id="915d2-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="915d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="915d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="915d2-130">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="915d2-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="915d2-131">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="915d2-131">-Schedule</span></span>
<span data-ttu-id="915d2-132">Objeto de cronograma de automação para agendar o trabalho de implantação.</span><span class="sxs-lookup"><span data-stu-id="915d2-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="915d2-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="915d2-133">-Confirm</span></span>
<span data-ttu-id="915d2-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="915d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915d2-135">-WhatIf</span></span>
<span data-ttu-id="915d2-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="915d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="915d2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="915d2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915d2-138">CommonParameters</span></span>
<span data-ttu-id="915d2-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="915d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915d2-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="915d2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915d2-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="915d2-141">INPUTS</span></span>

### <span data-ttu-id="915d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="915d2-142">System.String</span></span>

### <span data-ttu-id="915d2-143">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="915d2-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="915d2-144">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="915d2-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="915d2-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="915d2-145">OUTPUTS</span></span>

### <span data-ttu-id="915d2-146">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="915d2-146">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="915d2-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="915d2-147">NOTES</span></span>

## <span data-ttu-id="915d2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="915d2-148">RELATED LINKS</span></span>

[<span data-ttu-id="915d2-149">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="915d2-149">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="915d2-150">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="915d2-150">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="915d2-151">Parar-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="915d2-151">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="915d2-152">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="915d2-152">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="915d2-153">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="915d2-153">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="915d2-154">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="915d2-154">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)