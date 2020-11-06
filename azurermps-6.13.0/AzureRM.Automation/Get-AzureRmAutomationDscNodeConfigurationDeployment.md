---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 0c918328eb0b578eae31994c949210d62eba337b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429604"
---
# <span data-ttu-id="c4aa9-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c4aa9-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c4aa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4aa9-103">Obtém implantações de configuração do nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4aa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4aa9-104">SYNTAX</span></span>

### <span data-ttu-id="c4aa9-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4aa9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4aa9-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c4aa9-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4aa9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4aa9-107">DESCRIPTION</span></span>
<span data-ttu-id="c4aa9-108">O cmdlet **Get-AzureRmAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (configuração de estado Desired) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="c4aa9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-109">EXAMPLES</span></span>

### <span data-ttu-id="c4aa9-110">Exemplo 1: obter uma implantação de configuração de nó</span><span class="sxs-lookup"><span data-stu-id="c4aa9-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="c4aa9-111">O comando acima implanta a configuração do nó DSC chamada "Config01. Node1" para a matriz bidimensional fornecida dos nomes dos nós.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c4aa9-112">A implantação ocorre em uma maneira em estágios.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="c4aa9-113">OS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-113">PARAMETERS</span></span>

### <span data-ttu-id="c4aa9-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4aa9-114">-AutomationAccountName</span></span>
<span data-ttu-id="c4aa9-115">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="c4aa9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4aa9-116">-DefaultProfile</span></span>
<span data-ttu-id="c4aa9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c4aa9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4aa9-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c4aa9-118">-EndTime</span></span>
<span data-ttu-id="c4aa9-119">Filtro de hora de término.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-119">End time filter.</span></span>

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

### <span data-ttu-id="c4aa9-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="c4aa9-120">-JobId</span></span>
<span data-ttu-id="c4aa9-121">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="c4aa9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4aa9-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4aa9-123">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="c4aa9-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c4aa9-124">-StartTime</span></span>
<span data-ttu-id="c4aa9-125">Filtro de hora de início.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-125">Start time filter.</span></span>

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

### <span data-ttu-id="c4aa9-126">-Status</span><span class="sxs-lookup"><span data-stu-id="c4aa9-126">-Status</span></span>
<span data-ttu-id="c4aa9-127">Status do filtro de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="c4aa9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4aa9-128">CommonParameters</span></span>
<span data-ttu-id="c4aa9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4aa9-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4aa9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4aa9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4aa9-131">INPUTS</span></span>

### <span data-ttu-id="c4aa9-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c4aa9-132">System.Guid</span></span>

### <span data-ttu-id="c4aa9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c4aa9-133">System.String</span></span>

## <span data-ttu-id="c4aa9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4aa9-134">OUTPUTS</span></span>

### <span data-ttu-id="c4aa9-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c4aa9-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c4aa9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4aa9-136">NOTES</span></span>

## <span data-ttu-id="c4aa9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4aa9-138">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c4aa9-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="c4aa9-139">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4aa9-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c4aa9-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c4aa9-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c4aa9-141">Parar-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c4aa9-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c4aa9-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c4aa9-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
