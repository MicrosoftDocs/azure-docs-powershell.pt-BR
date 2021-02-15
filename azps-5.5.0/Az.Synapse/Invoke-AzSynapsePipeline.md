---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112408"
---
# <span data-ttu-id="fde1e-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="fde1e-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="fde1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fde1e-102">SYNOPSIS</span></span>
<span data-ttu-id="fde1e-103">Invoca um pipeline para iniciar uma operação para ele.</span><span class="sxs-lookup"><span data-stu-id="fde1e-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="fde1e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fde1e-104">SYNTAX</span></span>

### <span data-ttu-id="fde1e-105">NewByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fde1e-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde1e-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="fde1e-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde1e-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="fde1e-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde1e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fde1e-108">DESCRIPTION</span></span>
<span data-ttu-id="fde1e-109">O **comando Invoke-AzSynapse Pipelineline** inicia uma operação no pipeline especificado e retorna uma ID para essa executar.</span><span class="sxs-lookup"><span data-stu-id="fde1e-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="fde1e-110">Esse GUID pode ser passado **para Get-AzSynapse GuidlineRun** ou **Get-AzSynapseActivityRun** para obter mais detalhes sobre essa executar.</span><span class="sxs-lookup"><span data-stu-id="fde1e-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="fde1e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fde1e-111">EXAMPLES</span></span>

### <span data-ttu-id="fde1e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fde1e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="fde1e-113">Esse comando inicia uma operação para o pipeline chamado Contoso Pipeline no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fde1e-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="fde1e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fde1e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="fde1e-115">Esse comando inicia uma operação para o pipeline chamado Contoso Pipeline no espaço de trabalho ContosoWorkspace por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="fde1e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fde1e-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="fde1e-117">Esse comando inicia uma operação para o pipeline chamado Contoso Pipeline no espaço de trabalho ContosoWorkspace por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fde1e-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fde1e-118">PARAMETERS</span></span>

### <span data-ttu-id="fde1e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fde1e-119">-AsJob</span></span>
<span data-ttu-id="fde1e-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fde1e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fde1e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde1e-121">-DefaultProfile</span></span>
<span data-ttu-id="fde1e-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fde1e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde1e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde1e-123">-InputObject</span></span>
<span data-ttu-id="fde1e-124">As informações sobre o pipeline são executados.</span><span class="sxs-lookup"><span data-stu-id="fde1e-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="fde1e-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="fde1e-125">-IsRecovery</span></span>
<span data-ttu-id="fde1e-126">Sinalizador do modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fde1e-126">Recovery mode flag.</span></span>
<span data-ttu-id="fde1e-127">Se o modo de recuperação estiver definido como verdadeiro, a operação de pipeline especificada referenciada e a nova executar serão agrupadas sob a mesma ID de grupo.</span><span class="sxs-lookup"><span data-stu-id="fde1e-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="fde1e-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fde1e-128">-Parameter</span></span>
<span data-ttu-id="fde1e-129">Parâmetros para a operação de pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="fde1e-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="fde1e-130">-ParameterFile</span></span>
<span data-ttu-id="fde1e-131">O nome do arquivo com parâmetros para a operação de pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="fde1e-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="fde1e-132">-PipelineName</span></span>
<span data-ttu-id="fde1e-133">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-133">The pipeline name.</span></span>

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

### <span data-ttu-id="fde1e-134">-ReferenceEsqueleRunId</span><span class="sxs-lookup"><span data-stu-id="fde1e-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="fde1e-135">A ID de executar o pipeline para executar de uma nova vez.</span><span class="sxs-lookup"><span data-stu-id="fde1e-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="fde1e-136">Se a ID de executar for especificada, os parâmetros da executar especificada serão usados para criar uma nova executar.</span><span class="sxs-lookup"><span data-stu-id="fde1e-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="fde1e-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="fde1e-137">-StartActivityName</span></span>
<span data-ttu-id="fde1e-138">No modo de recuperação, a reprise iniciará a partir dessa atividade.</span><span class="sxs-lookup"><span data-stu-id="fde1e-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="fde1e-139">Se não especificado, todas as atividades serão executados.</span><span class="sxs-lookup"><span data-stu-id="fde1e-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="fde1e-140">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="fde1e-140">-WorkspaceName</span></span>
<span data-ttu-id="fde1e-141">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="fde1e-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fde1e-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fde1e-142">-WorkspaceObject</span></span>
<span data-ttu-id="fde1e-143">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde1e-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fde1e-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fde1e-144">-Confirm</span></span>
<span data-ttu-id="fde1e-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde1e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde1e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde1e-146">-WhatIf</span></span>
<span data-ttu-id="fde1e-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fde1e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde1e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fde1e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde1e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde1e-149">CommonParameters</span></span>
<span data-ttu-id="fde1e-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde1e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde1e-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fde1e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde1e-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="fde1e-152">INPUTS</span></span>

### <span data-ttu-id="fde1e-153">Microsoft.Azure.Commands.Synapse.Models.PS ElelineResource</span><span class="sxs-lookup"><span data-stu-id="fde1e-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="fde1e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fde1e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fde1e-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="fde1e-155">OUTPUTS</span></span>

### <span data-ttu-id="fde1e-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="fde1e-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="fde1e-157">Notas</span><span class="sxs-lookup"><span data-stu-id="fde1e-157">NOTES</span></span>

## <span data-ttu-id="fde1e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fde1e-158">RELATED LINKS</span></span>
