---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261790"
---
# <span data-ttu-id="8ff14-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="8ff14-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="8ff14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ff14-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff14-103">Obtém informações sobre execuções de atividades para uma execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ff14-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="8ff14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ff14-104">SYNTAX</span></span>

### <span data-ttu-id="8ff14-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ff14-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ff14-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8ff14-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ff14-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ff14-107">DESCRIPTION</span></span>
<span data-ttu-id="8ff14-108">O cmdlet **Get-AzDataFactoryV2ActivityRun** Obtém informações sobre execuções na fábrica de dados do Azure para a execução de pipeline especificada que aconteceu no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="8ff14-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="8ff14-109">Além disso, você pode especificar filtros para nome da atividade, nome do serviço vinculado que executou a execução e o status da execução.</span><span class="sxs-lookup"><span data-stu-id="8ff14-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="8ff14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ff14-110">EXAMPLES</span></span>

### <span data-ttu-id="8ff14-111">Exemplo 1: obter todas as execuções de atividades para uma execução de pipeline</span><span class="sxs-lookup"><span data-stu-id="8ff14-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="8ff14-112">Esse comando obtém detalhes sobre as execuções de todas as atividades no pipeline executadas com o ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="8ff14-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="8ff14-113">OS</span><span class="sxs-lookup"><span data-stu-id="8ff14-113">PARAMETERS</span></span>

### <span data-ttu-id="8ff14-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="8ff14-114">-ActivityName</span></span>
<span data-ttu-id="8ff14-115">O nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="8ff14-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="8ff14-116">-DataFactory</span></span>
<span data-ttu-id="8ff14-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8ff14-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8ff14-118">-DataFactoryName</span></span>
<span data-ttu-id="8ff14-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8ff14-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff14-120">-DefaultProfile</span></span>
<span data-ttu-id="8ff14-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ff14-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8ff14-122">-PipelineRunId</span></span>
<span data-ttu-id="8ff14-123">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ff14-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff14-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ff14-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ff14-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="8ff14-126">-RunStartedAfter</span></span>
<span data-ttu-id="8ff14-127">A hora em ou após a qual a execução do pipeline começou a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8ff14-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="8ff14-128">-RunStartedBefore</span></span>
<span data-ttu-id="8ff14-129">O horário em ou antes do qual a execução do pipeline começou a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8ff14-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-130">-Status</span><span class="sxs-lookup"><span data-stu-id="8ff14-130">-Status</span></span>
<span data-ttu-id="8ff14-131">O status da execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ff14-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ff14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff14-132">CommonParameters</span></span>
<span data-ttu-id="8ff14-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff14-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ff14-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff14-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ff14-135">INPUTS</span></span>

### <span data-ttu-id="8ff14-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8ff14-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="8ff14-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8ff14-137">System.String</span></span>

## <span data-ttu-id="8ff14-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ff14-138">OUTPUTS</span></span>

### <span data-ttu-id="8ff14-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="8ff14-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="8ff14-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ff14-140">NOTES</span></span>

## <span data-ttu-id="8ff14-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ff14-141">RELATED LINKS</span></span>

[<span data-ttu-id="8ff14-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8ff14-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8ff14-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8ff14-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

