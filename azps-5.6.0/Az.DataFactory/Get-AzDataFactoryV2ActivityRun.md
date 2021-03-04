---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5262e5b9d1229905c80a7a2f83c71d9a77840ece
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888298"
---
# <span data-ttu-id="d3ebe-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d3ebe-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="d3ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ebe-103">Obtém informações sobre as atividades executados para uma operação de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="d3ebe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3ebe-104">SYNTAX</span></span>

### <span data-ttu-id="d3ebe-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3ebe-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ebe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3ebe-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ebe-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="d3ebe-108">O cmdlet **Get-AzDataFactoryV2ActivityRun** obtém informações sobre as executações no Azure Data Factory para a duração do pipeline especificada que aconteceu no determinado período de tempo.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="d3ebe-109">Além disso, você pode especificar filtros para nome da atividade, nome de serviço vinculado que executou a execução e o status da execução.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="d3ebe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-110">EXAMPLES</span></span>

### <span data-ttu-id="d3ebe-111">Exemplo 1: Executar todas as atividades para uma operação de pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ebe-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="d3ebe-112">Este comando obtém detalhes sobre todas as atividades executados no pipeline executado com a ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="d3ebe-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="d3ebe-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-113">PARAMETERS</span></span>

### <span data-ttu-id="d3ebe-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="d3ebe-114">-ActivityName</span></span>
<span data-ttu-id="d3ebe-115">O nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-115">The name of the activity.</span></span>

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

### <span data-ttu-id="d3ebe-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3ebe-116">-DataFactory</span></span>
<span data-ttu-id="d3ebe-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-117">The data factory object.</span></span>

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

### <span data-ttu-id="d3ebe-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3ebe-118">-DataFactoryName</span></span>
<span data-ttu-id="d3ebe-119">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-119">The data factory name.</span></span>

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

### <span data-ttu-id="d3ebe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ebe-120">-DefaultProfile</span></span>
<span data-ttu-id="d3ebe-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ebe-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d3ebe-122">-PipelineRunId</span></span>
<span data-ttu-id="d3ebe-123">A ID de executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="d3ebe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3ebe-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3ebe-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-125">The resource group name.</span></span>

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

### <span data-ttu-id="d3ebe-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d3ebe-126">-RunStartedAfter</span></span>
<span data-ttu-id="d3ebe-127">O momento em que a execução do pipeline começou a ser executada.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="d3ebe-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d3ebe-128">-RunStartedBefore</span></span>
<span data-ttu-id="d3ebe-129">O momento em que o pipeline de execução começou a ser executado.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="d3ebe-130">-Status</span><span class="sxs-lookup"><span data-stu-id="d3ebe-130">-Status</span></span>
<span data-ttu-id="d3ebe-131">O status do pipeline executado.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="d3ebe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ebe-132">CommonParameters</span></span>
<span data-ttu-id="d3ebe-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ebe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ebe-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ebe-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ebe-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-135">INPUTS</span></span>

### <span data-ttu-id="d3ebe-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3ebe-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="d3ebe-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d3ebe-137">System.String</span></span>

## <span data-ttu-id="d3ebe-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-138">OUTPUTS</span></span>

### <span data-ttu-id="d3ebe-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="d3ebe-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="d3ebe-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3ebe-140">NOTES</span></span>

## <span data-ttu-id="d3ebe-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3ebe-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3ebe-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ebe-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d3ebe-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d3ebe-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

