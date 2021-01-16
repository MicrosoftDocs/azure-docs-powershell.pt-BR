---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259258"
---
# <span data-ttu-id="004cd-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="004cd-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="004cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="004cd-102">SYNOPSIS</span></span>
<span data-ttu-id="004cd-103">Obtém informações sobre execuções de atividades para uma execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="004cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="004cd-104">SYNTAX</span></span>

### <span data-ttu-id="004cd-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="004cd-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="004cd-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="004cd-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="004cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="004cd-107">DESCRIPTION</span></span>
<span data-ttu-id="004cd-108">O cmdlet **Get-AzSynapseActivityRun** Obtém informações sobre execuções em espaço de trabalho para o pipeline especificado executado que aconteceu no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="004cd-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="004cd-109">Além disso, você pode especificar filtros para o nome da atividade e o status da execução.</span><span class="sxs-lookup"><span data-stu-id="004cd-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="004cd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="004cd-110">EXAMPLES</span></span>

### <span data-ttu-id="004cd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="004cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="004cd-112">Esse comando obtém detalhes sobre todas as execuções de atividades no pipeline chamado ContosoPipeline run com ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2018-09-01T21:00" e "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="004cd-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="004cd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="004cd-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="004cd-114">Esse comando obtém detalhes sobre todas as execuções de atividades no pipeline chamado ContosoPipeline run com ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2018-09-01T21:00" e "2018-09-30T21:00" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="004cd-115">OS</span><span class="sxs-lookup"><span data-stu-id="004cd-115">PARAMETERS</span></span>

### <span data-ttu-id="004cd-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="004cd-116">-ActivityName</span></span>
<span data-ttu-id="004cd-117">O nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="004cd-117">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004cd-118">-DefaultProfile</span></span>
<span data-ttu-id="004cd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="004cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="004cd-120">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="004cd-120">-PipelineName</span></span>
<span data-ttu-id="004cd-121">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="004cd-122">-PipelineRunId</span></span>
<span data-ttu-id="004cd-123">O identificador de execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="004cd-124">-RunStartedAfter</span></span>
<span data-ttu-id="004cd-125">A hora em ou após a qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="004cd-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="004cd-126">-RunStartedBefore</span></span>
<span data-ttu-id="004cd-127">A hora em ou antes da qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="004cd-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-128">-Status</span><span class="sxs-lookup"><span data-stu-id="004cd-128">-Status</span></span>
<span data-ttu-id="004cd-129">O status da execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-129">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="004cd-130">-WorkspaceName</span></span>
<span data-ttu-id="004cd-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="004cd-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="004cd-132">-WorkspaceObject</span></span>
<span data-ttu-id="004cd-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="004cd-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004cd-134">CommonParameters</span></span>
<span data-ttu-id="004cd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004cd-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="004cd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004cd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="004cd-137">INPUTS</span></span>

### <span data-ttu-id="004cd-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="004cd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="004cd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="004cd-139">OUTPUTS</span></span>

### <span data-ttu-id="004cd-140">Microsoft. Azure. Commands. Synapse. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="004cd-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="004cd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="004cd-141">NOTES</span></span>

## <span data-ttu-id="004cd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="004cd-142">RELATED LINKS</span></span>
