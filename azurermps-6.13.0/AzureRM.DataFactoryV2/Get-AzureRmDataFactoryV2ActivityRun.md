---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430336"
---
# <span data-ttu-id="9ad60-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="9ad60-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="9ad60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ad60-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad60-103">Obtém informações sobre execuções de atividades para uma execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ad60-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ad60-104">SYNTAX</span></span>

### <span data-ttu-id="9ad60-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ad60-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad60-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9ad60-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad60-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ad60-107">DESCRIPTION</span></span>
<span data-ttu-id="9ad60-108">O cmdlet **Get-AzureRmDataFactoryV2ActivityRun** Obtém informações sobre execuções na fábrica de dados do Azure para a execução de pipeline especificada que aconteceu no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="9ad60-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="9ad60-109">Além disso, você pode especificar filtros para nome da atividade, nome do serviço vinculado que executou a execução e o status da execução.</span><span class="sxs-lookup"><span data-stu-id="9ad60-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="9ad60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ad60-110">EXAMPLES</span></span>

### <span data-ttu-id="9ad60-111">Exemplo 1: obter todas as execuções de atividades para uma execução de pipeline</span><span class="sxs-lookup"><span data-stu-id="9ad60-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="9ad60-112">Esse comando obtém detalhes sobre as execuções de todas as atividades no pipeline executadas com o ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2017-09-01" e "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="9ad60-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="9ad60-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ad60-113">PARAMETERS</span></span>

### <span data-ttu-id="9ad60-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="9ad60-114">-ActivityName</span></span>
<span data-ttu-id="9ad60-115">O nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="9ad60-115">The name of the activity.</span></span>

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

### <span data-ttu-id="9ad60-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="9ad60-116">-DataFactory</span></span>
<span data-ttu-id="9ad60-117">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9ad60-117">The data factory object.</span></span>

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

### <span data-ttu-id="9ad60-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9ad60-118">-DataFactoryName</span></span>
<span data-ttu-id="9ad60-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="9ad60-119">The data factory name.</span></span>

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

### <span data-ttu-id="9ad60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad60-120">-DefaultProfile</span></span>
<span data-ttu-id="9ad60-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad60-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad60-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="9ad60-122">-LinkedServiceName</span></span>
<span data-ttu-id="9ad60-123">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="9ad60-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad60-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="9ad60-124">-PipelineRunId</span></span>
<span data-ttu-id="9ad60-125">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ad60-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="9ad60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad60-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ad60-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ad60-127">The resource group name.</span></span>

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

### <span data-ttu-id="9ad60-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="9ad60-128">-RunStartedAfter</span></span>
<span data-ttu-id="9ad60-129">A hora em ou após a qual a execução do pipeline começou a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9ad60-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="9ad60-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="9ad60-130">-RunStartedBefore</span></span>
<span data-ttu-id="9ad60-131">O horário em ou antes do qual a execução do pipeline começou a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9ad60-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="9ad60-132">-Status</span><span class="sxs-lookup"><span data-stu-id="9ad60-132">-Status</span></span>
<span data-ttu-id="9ad60-133">O status da execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ad60-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="9ad60-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad60-134">CommonParameters</span></span>
<span data-ttu-id="9ad60-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad60-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad60-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad60-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad60-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ad60-137">INPUTS</span></span>

### <span data-ttu-id="9ad60-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9ad60-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9ad60-139">Parâmetros: datafactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ad60-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="9ad60-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad60-140">System.String</span></span>

## <span data-ttu-id="9ad60-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ad60-141">OUTPUTS</span></span>

### <span data-ttu-id="9ad60-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="9ad60-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="9ad60-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ad60-143">NOTES</span></span>

## <span data-ttu-id="9ad60-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ad60-144">RELATED LINKS</span></span>

[<span data-ttu-id="9ad60-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9ad60-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9ad60-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="9ad60-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()
