---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431206"
---
# <span data-ttu-id="c1732-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c1732-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c1732-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1732-102">SYNOPSIS</span></span>
<span data-ttu-id="c1732-103">Obtém implantações de configuração do nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="c1732-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1732-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1732-104">SYNTAX</span></span>

### <span data-ttu-id="c1732-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1732-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1732-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c1732-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1732-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1732-107">DESCRIPTION</span></span>
<span data-ttu-id="c1732-108">O cmdlet **Get-AzureRmAutomationDscNodeConfigurationDeployment** implanta uma configuração de nó DSC (configuração de estado Desired) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1732-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="c1732-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1732-109">EXAMPLES</span></span>

### <span data-ttu-id="c1732-110">Exemplo 1: obter uma implantação de configuração de nó</span><span class="sxs-lookup"><span data-stu-id="c1732-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="c1732-111">O comando acima implanta a configuração do nó DSC chamada "Config01. Node1" para a matriz bidimensional fornecida dos nomes dos nós.</span><span class="sxs-lookup"><span data-stu-id="c1732-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c1732-112">A implantação ocorre em uma maneira em estágios.</span><span class="sxs-lookup"><span data-stu-id="c1732-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="c1732-113">OS</span><span class="sxs-lookup"><span data-stu-id="c1732-113">PARAMETERS</span></span>

### <span data-ttu-id="c1732-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="c1732-114">-JobId</span></span>
<span data-ttu-id="c1732-115">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="c1732-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="c1732-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1732-116">-ResourceGroupName</span></span>
<span data-ttu-id="c1732-117">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="c1732-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="c1732-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c1732-118">-AutomationAccountName</span></span>
<span data-ttu-id="c1732-119">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="c1732-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="c1732-120">-Status</span><span class="sxs-lookup"><span data-stu-id="c1732-120">-Status</span></span>
<span data-ttu-id="c1732-121">Status do filtro de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1732-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1732-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c1732-122">-StartTime</span></span>
<span data-ttu-id="c1732-123">Filtro de hora de início.</span><span class="sxs-lookup"><span data-stu-id="c1732-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1732-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c1732-124">-EndTime</span></span>
<span data-ttu-id="c1732-125">Filtro de hora de término.</span><span class="sxs-lookup"><span data-stu-id="c1732-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1732-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1732-126">-DefaultProfile</span></span>
<span data-ttu-id="c1732-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1732-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1732-128">CommonParameters</span></span>
<span data-ttu-id="c1732-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1732-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1732-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1732-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1732-131">INPUTS</span></span>

## <span data-ttu-id="c1732-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1732-132">OUTPUTS</span></span>

### <span data-ttu-id="c1732-133">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c1732-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c1732-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1732-134">NOTES</span></span>

## <span data-ttu-id="c1732-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1732-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1732-136">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c1732-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="c1732-137">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1732-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c1732-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c1732-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c1732-139">Parar-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c1732-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c1732-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c1732-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
