---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 3bb0f095550394991bb74065e8d1c34c346b0c4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885748"
---
# <span data-ttu-id="a6d14-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a6d14-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="a6d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d14-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d14-103">Obtém um cronograma de trabalho de implantação de configuração de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="a6d14-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="a6d14-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6d14-104">SYNTAX</span></span>

### <span data-ttu-id="a6d14-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6d14-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6d14-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="a6d14-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d14-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6d14-107">DESCRIPTION</span></span>
<span data-ttu-id="a6d14-108">O cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (Configuração de Estado Desejado) do APS na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d14-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="a6d14-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6d14-109">EXAMPLES</span></span>

### <span data-ttu-id="a6d14-110">Exemplo 1: Obter todos os cronogramas de implantação</span><span class="sxs-lookup"><span data-stu-id="a6d14-110">Example 1: Get all the deployment schedules</span></span>
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

### <span data-ttu-id="a6d14-111">Exemplo 2: Obter um cronograma de implantação</span><span class="sxs-lookup"><span data-stu-id="a6d14-111">Example 2: Get a deployment schedule</span></span>
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

<span data-ttu-id="a6d14-112">O comando acima implanta a configuração de nó DSC chamada "Config01.Node1" à matriz bidimensional de Nomes de Nó.</span><span class="sxs-lookup"><span data-stu-id="a6d14-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="a6d14-113">A implantação acontece em estágios.</span><span class="sxs-lookup"><span data-stu-id="a6d14-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="a6d14-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6d14-114">PARAMETERS</span></span>

### <span data-ttu-id="a6d14-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6d14-115">-AutomationAccountName</span></span>
<span data-ttu-id="a6d14-116">Especifica o nome da conta de automação que contém a configuração DSC compilada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6d14-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a6d14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d14-117">-DefaultProfile</span></span>
<span data-ttu-id="a6d14-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a6d14-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6d14-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="a6d14-119">-JobScheduleId</span></span>
<span data-ttu-id="a6d14-120">Especifica a ID do Cronograma de Trabalho de um trabalho de implantação agendado existente.</span><span class="sxs-lookup"><span data-stu-id="a6d14-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="a6d14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d14-121">-ResourceGroupName</span></span>
<span data-ttu-id="a6d14-122">Especifica o nome de um grupo de recursos no qual este cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="a6d14-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a6d14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d14-123">CommonParameters</span></span>
<span data-ttu-id="a6d14-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d14-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d14-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d14-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6d14-126">INPUTS</span></span>

### <span data-ttu-id="a6d14-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a6d14-127">System.Guid</span></span>

### <span data-ttu-id="a6d14-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a6d14-128">System.String</span></span>

## <span data-ttu-id="a6d14-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6d14-129">OUTPUTS</span></span>

### <span data-ttu-id="a6d14-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="a6d14-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="a6d14-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6d14-131">NOTES</span></span>

## <span data-ttu-id="a6d14-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6d14-132">RELATED LINKS</span></span>

[<span data-ttu-id="a6d14-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a6d14-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="a6d14-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6d14-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="a6d14-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a6d14-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a6d14-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a6d14-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="a6d14-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="a6d14-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
