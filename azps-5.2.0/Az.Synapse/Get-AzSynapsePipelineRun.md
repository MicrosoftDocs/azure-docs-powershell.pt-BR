---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259237"
---
# <span data-ttu-id="2e4f2-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="2e4f2-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="2e4f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4f2-103">Obtém informações sobre execuções de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="2e4f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e4f2-104">SYNTAX</span></span>

### <span data-ttu-id="2e4f2-105">GetByNameAndId (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e4f2-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e4f2-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="2e4f2-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e4f2-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="2e4f2-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e4f2-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="2e4f2-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e4f2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e4f2-109">DESCRIPTION</span></span>
<span data-ttu-id="2e4f2-110">O comando **Get-AzSynapsePipelineRun** retorna informações sobre execuções para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="2e4f2-111">Se PipelineRunId for especificado, exibirá detalhes para a execução com essa ID.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="2e4f2-112">Se o PipelineRunId não for especificado, ele exibirá informações sobre todas as execuções dos pipelines que ocorreram entre os valores de RunStartedAfter e RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="2e4f2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e4f2-113">EXAMPLES</span></span>

### <span data-ttu-id="2e4f2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e4f2-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="2e4f2-115">Esse comando obtém detalhes sobre o pipeline executado com ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="2e4f2-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="2e4f2-116">OS</span><span class="sxs-lookup"><span data-stu-id="2e4f2-116">PARAMETERS</span></span>

### <span data-ttu-id="2e4f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4f2-117">-DefaultProfile</span></span>
<span data-ttu-id="2e4f2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e4f2-119">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="2e4f2-119">-PipelineName</span></span>
<span data-ttu-id="2e4f2-120">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2e4f2-121">-PipelineRunId</span></span>
<span data-ttu-id="2e4f2-122">O identificador de execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2e4f2-123">-RunStartedAfter</span></span>
<span data-ttu-id="2e4f2-124">A hora em ou após a qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2e4f2-125">-RunStartedBefore</span></span>
<span data-ttu-id="2e4f2-126">A hora em ou antes da qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e4f2-127">-WorkspaceName</span></span>
<span data-ttu-id="2e4f2-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2e4f2-129">-WorkspaceObject</span></span>
<span data-ttu-id="2e4f2-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e4f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4f2-131">CommonParameters</span></span>
<span data-ttu-id="2e4f2-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4f2-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e4f2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4f2-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e4f2-134">INPUTS</span></span>

### <span data-ttu-id="2e4f2-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e4f2-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2e4f2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e4f2-136">OUTPUTS</span></span>

### <span data-ttu-id="2e4f2-137">Microsoft. Azure. Commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="2e4f2-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="2e4f2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e4f2-138">NOTES</span></span>

## <span data-ttu-id="2e4f2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e4f2-139">RELATED LINKS</span></span>
