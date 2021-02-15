---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118027"
---
# <span data-ttu-id="e38b0-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e38b0-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="e38b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e38b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e38b0-103">Obtém implantações de configuração de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="e38b0-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="e38b0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e38b0-104">SYNTAX</span></span>

### <span data-ttu-id="e38b0-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e38b0-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e38b0-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="e38b0-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e38b0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e38b0-107">DESCRIPTION</span></span>
<span data-ttu-id="e38b0-108">O cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (Configuração de Estado Desejado) APS na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e38b0-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="e38b0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e38b0-109">EXAMPLES</span></span>

### <span data-ttu-id="e38b0-110">Exemplo 1: Obter uma implantação de configuração de nó</span><span class="sxs-lookup"><span data-stu-id="e38b0-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="e38b0-111">O comando acima implanta a configuração de nó DSC chamada "Config01.Node1" para a determinada matriz bidimensional de Nomes de Nó.</span><span class="sxs-lookup"><span data-stu-id="e38b0-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="e38b0-112">A implantação acontece em estágios.</span><span class="sxs-lookup"><span data-stu-id="e38b0-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="e38b0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e38b0-113">PARAMETERS</span></span>

### <span data-ttu-id="e38b0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e38b0-114">-AutomationAccountName</span></span>
<span data-ttu-id="e38b0-115">Especifica o nome da conta automação que contém a configuração DSC compilada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e38b0-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="e38b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38b0-116">-DefaultProfile</span></span>
<span data-ttu-id="e38b0-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e38b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e38b0-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e38b0-118">-EndTime</span></span>
<span data-ttu-id="e38b0-119">Filtro de hora de término.</span><span class="sxs-lookup"><span data-stu-id="e38b0-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b0-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="e38b0-120">-JobId</span></span>
<span data-ttu-id="e38b0-121">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="e38b0-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e38b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="e38b0-123">Especifica o nome de um grupo de recursos no qual este cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="e38b0-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="e38b0-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e38b0-124">-StartTime</span></span>
<span data-ttu-id="e38b0-125">Filtro de hora de início.</span><span class="sxs-lookup"><span data-stu-id="e38b0-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b0-126">-Status</span><span class="sxs-lookup"><span data-stu-id="e38b0-126">-Status</span></span>
<span data-ttu-id="e38b0-127">Status do filtro Trabalho.</span><span class="sxs-lookup"><span data-stu-id="e38b0-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38b0-128">CommonParameters</span></span>
<span data-ttu-id="e38b0-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38b0-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38b0-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="e38b0-131">INPUTS</span></span>

### <span data-ttu-id="e38b0-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e38b0-132">System.Guid</span></span>

### <span data-ttu-id="e38b0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e38b0-133">System.String</span></span>

## <span data-ttu-id="e38b0-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="e38b0-134">OUTPUTS</span></span>

### <span data-ttu-id="e38b0-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e38b0-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="e38b0-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e38b0-136">NOTES</span></span>

## <span data-ttu-id="e38b0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e38b0-137">RELATED LINKS</span></span>

[<span data-ttu-id="e38b0-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e38b0-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="e38b0-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e38b0-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="e38b0-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e38b0-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e38b0-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e38b0-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e38b0-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="e38b0-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
