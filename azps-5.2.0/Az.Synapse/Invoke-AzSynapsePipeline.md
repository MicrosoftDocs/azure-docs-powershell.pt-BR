---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264128"
---
# <span data-ttu-id="2e4a9-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="2e4a9-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="2e4a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4a9-103">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="2e4a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e4a9-104">SYNTAX</span></span>

### <span data-ttu-id="2e4a9-105">NewByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e4a9-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e4a9-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e4a9-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e4a9-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="2e4a9-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e4a9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e4a9-108">DESCRIPTION</span></span>
<span data-ttu-id="2e4a9-109">O comando **Invoke-AzSynapsePipeline** inicia uma execução no pipeline especificado e retorna uma ID para essa execução.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="2e4a9-110">Esse GUID pode ser passado para **Get-AzSynapsePipelineRun** ou **Get-AzSynapseActivityRun** para obter mais detalhes sobre essa execução.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="2e4a9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e4a9-111">EXAMPLES</span></span>

### <span data-ttu-id="2e4a9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e4a9-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="2e4a9-113">Esse comando inicia uma execução para o pipeline chamado ContosoPipeline na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2e4a9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e4a9-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="2e4a9-115">Esse comando inicia uma execução para o pipeline chamado ContosoPipeline no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2e4a9-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2e4a9-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="2e4a9-117">Esse comando inicia uma execução para o pipeline chamado ContosoPipeline no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2e4a9-118">OS</span><span class="sxs-lookup"><span data-stu-id="2e4a9-118">PARAMETERS</span></span>

### <span data-ttu-id="2e4a9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e4a9-119">-AsJob</span></span>
<span data-ttu-id="2e4a9-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2e4a9-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4a9-121">-DefaultProfile</span></span>
<span data-ttu-id="2e4a9-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e4a9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e4a9-123">-InputObject</span></span>
<span data-ttu-id="2e4a9-124">As informações sobre o pipeline são executadas.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="2e4a9-125">-IsRecovery</span></span>
<span data-ttu-id="2e4a9-126">Sinalizador do modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-126">Recovery mode flag.</span></span>
<span data-ttu-id="2e4a9-127">Se o modo de recuperação for definido como verdadeiro, o pipeline Referenciado especificado e a nova execução serão agrupados sob o mesmo GroupId.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e4a9-128">-Parameter</span></span>
<span data-ttu-id="2e4a9-129">Parâmetros para a execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-130">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="2e4a9-130">-ParameterFile</span></span>
<span data-ttu-id="2e4a9-131">O nome do arquivo com parâmetros para execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="2e4a9-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="2e4a9-132">-PipelineName</span></span>
<span data-ttu-id="2e4a9-133">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2e4a9-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="2e4a9-135">A ID de execução do pipeline para executar novamente.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="2e4a9-136">Se a ID de execução for especificada, os parâmetros da execução especificada serão usados para criar uma nova execução.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="2e4a9-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="2e4a9-137">-StartActivityName</span></span>
<span data-ttu-id="2e4a9-138">No modo de recuperação, o reinício será iniciado a partir dessa atividade.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="2e4a9-139">Se não for especificado, todas as atividades serão executadas.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="2e4a9-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e4a9-140">-WorkspaceName</span></span>
<span data-ttu-id="2e4a9-141">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-142">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2e4a9-142">-WorkspaceObject</span></span>
<span data-ttu-id="2e4a9-143">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e4a9-144">-Confirm</span></span>
<span data-ttu-id="2e4a9-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e4a9-146">-WhatIf</span></span>
<span data-ttu-id="2e4a9-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e4a9-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4a9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4a9-149">CommonParameters</span></span>
<span data-ttu-id="2e4a9-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4a9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4a9-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e4a9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4a9-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e4a9-152">INPUTS</span></span>

### <span data-ttu-id="2e4a9-153">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="2e4a9-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="2e4a9-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e4a9-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2e4a9-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e4a9-155">OUTPUTS</span></span>

### <span data-ttu-id="2e4a9-156">Microsoft. Azure. Commands. Synapse. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="2e4a9-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="2e4a9-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e4a9-157">NOTES</span></span>

## <span data-ttu-id="2e4a9-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e4a9-158">RELATED LINKS</span></span>
