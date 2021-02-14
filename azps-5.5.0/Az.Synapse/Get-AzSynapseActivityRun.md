---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115629"
---
# <span data-ttu-id="b31ea-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="b31ea-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="b31ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b31ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b31ea-103">Obtém informações sobre atividades em uma operação de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="b31ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b31ea-104">SYNTAX</span></span>

### <span data-ttu-id="b31ea-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b31ea-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31ea-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b31ea-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31ea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b31ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b31ea-108">O cmdlet **Get-AzSynapseActivityRun** obtém informações sobre as executados no espaço de trabalho para a operação de pipeline especificada que ocorreu no prazo determinado.</span><span class="sxs-lookup"><span data-stu-id="b31ea-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="b31ea-109">Além disso, você pode especificar filtros para o nome da atividade e o status da executar.</span><span class="sxs-lookup"><span data-stu-id="b31ea-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="b31ea-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b31ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b31ea-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b31ea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="b31ea-112">Este comando obtém detalhes sobre todas as atividades realizadas no pipeline chamado Contoso Pipeline run com ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "2018-09-01T21:00" e "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="b31ea-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="b31ea-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b31ea-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="b31ea-114">Este comando obtém detalhes sobre todas as atividades realizadas no pipeline chamado Contoso Pipeline run com ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" que aconteceu entre "09/09/2018-01T21:00" e "2018-09-30T21:00" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="b31ea-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b31ea-115">PARAMETERS</span></span>

### <span data-ttu-id="b31ea-116">-Nomeda Atividade</span><span class="sxs-lookup"><span data-stu-id="b31ea-116">-ActivityName</span></span>
<span data-ttu-id="b31ea-117">O nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="b31ea-117">The name of the activity.</span></span>

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

### <span data-ttu-id="b31ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31ea-118">-DefaultProfile</span></span>
<span data-ttu-id="b31ea-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b31ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b31ea-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="b31ea-120">-PipelineName</span></span>
<span data-ttu-id="b31ea-121">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-121">The pipeline name.</span></span>

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

### <span data-ttu-id="b31ea-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="b31ea-122">-PipelineRunId</span></span>
<span data-ttu-id="b31ea-123">O identificador de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="b31ea-124">-ExecutarStartedAfter</span><span class="sxs-lookup"><span data-stu-id="b31ea-124">-RunStartedAfter</span></span>
<span data-ttu-id="b31ea-125">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="b31ea-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="b31ea-126">-ExecutarStartedBefore</span><span class="sxs-lookup"><span data-stu-id="b31ea-126">-RunStartedBefore</span></span>
<span data-ttu-id="b31ea-127">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="b31ea-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="b31ea-128">-Status</span><span class="sxs-lookup"><span data-stu-id="b31ea-128">-Status</span></span>
<span data-ttu-id="b31ea-129">O status da executar o pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="b31ea-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="b31ea-130">-WorkspaceName</span></span>
<span data-ttu-id="b31ea-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b31ea-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b31ea-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b31ea-132">-WorkspaceObject</span></span>
<span data-ttu-id="b31ea-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b31ea-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b31ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31ea-134">CommonParameters</span></span>
<span data-ttu-id="b31ea-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31ea-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b31ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31ea-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b31ea-137">INPUTS</span></span>

### <span data-ttu-id="b31ea-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b31ea-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b31ea-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="b31ea-139">OUTPUTS</span></span>

### <span data-ttu-id="b31ea-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="b31ea-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="b31ea-141">Notas</span><span class="sxs-lookup"><span data-stu-id="b31ea-141">NOTES</span></span>

## <span data-ttu-id="b31ea-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b31ea-142">RELATED LINKS</span></span>
