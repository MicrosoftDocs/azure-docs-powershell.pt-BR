---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432608"
---
# <span data-ttu-id="225c4-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="225c4-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="225c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="225c4-102">SYNOPSIS</span></span>
<span data-ttu-id="225c4-103">Obtém um agendamento de trabalho de implantação de configuração de nó DSC em automação.</span><span class="sxs-lookup"><span data-stu-id="225c4-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="225c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="225c4-104">SYNTAX</span></span>

### <span data-ttu-id="225c4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="225c4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="225c4-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="225c4-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="225c4-107">DESCRIPTION</span></span>
<span data-ttu-id="225c4-108">O cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (configuração de estado Desired) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="225c4-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="225c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="225c4-109">EXAMPLES</span></span>

### <span data-ttu-id="225c4-110">Exemplo 1: obter todos os cronogramas de implantação</span><span class="sxs-lookup"><span data-stu-id="225c4-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="225c4-111">Exemplo 2: obter um cronograma de implantação</span><span class="sxs-lookup"><span data-stu-id="225c4-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="225c4-112">O comando acima implanta a configuração do nó DSC chamada "Config01. Node1" para a matriz bidimensional fornecida dos nomes dos nós.</span><span class="sxs-lookup"><span data-stu-id="225c4-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="225c4-113">A implantação ocorre em uma maneira em estágios.</span><span class="sxs-lookup"><span data-stu-id="225c4-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="225c4-114">OS</span><span class="sxs-lookup"><span data-stu-id="225c4-114">PARAMETERS</span></span>

### <span data-ttu-id="225c4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="225c4-115">-AutomationAccountName</span></span>
<span data-ttu-id="225c4-116">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="225c4-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="225c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225c4-117">-DefaultProfile</span></span>
<span data-ttu-id="225c4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="225c4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="225c4-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="225c4-119">-JobScheduleId</span></span>
<span data-ttu-id="225c4-120">Especifica a ID de agendamento do trabalho de um trabalho de implantação agendado existente.</span><span class="sxs-lookup"><span data-stu-id="225c4-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="225c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="225c4-122">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="225c4-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="225c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225c4-123">CommonParameters</span></span>
<span data-ttu-id="225c4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225c4-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225c4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225c4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="225c4-126">INPUTS</span></span>

### <span data-ttu-id="225c4-127">System. GUID</span><span class="sxs-lookup"><span data-stu-id="225c4-127">System.Guid</span></span>

### <span data-ttu-id="225c4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="225c4-128">System.String</span></span>

## <span data-ttu-id="225c4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="225c4-129">OUTPUTS</span></span>

### <span data-ttu-id="225c4-130">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="225c4-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="225c4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="225c4-131">NOTES</span></span>

## <span data-ttu-id="225c4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="225c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="225c4-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="225c4-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="225c4-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="225c4-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="225c4-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="225c4-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="225c4-136">Parar-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="225c4-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="225c4-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="225c4-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
