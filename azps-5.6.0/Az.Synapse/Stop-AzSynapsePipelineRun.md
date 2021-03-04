---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: 607b251deff02ae6a74f0ceb5fc4f88a9c899688
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890522"
---
# <span data-ttu-id="21512-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="21512-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="21512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21512-102">SYNOPSIS</span></span>
<span data-ttu-id="21512-103">Interrompe um pipeline executado em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="21512-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="21512-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="21512-104">SYNTAX</span></span>

### <span data-ttu-id="21512-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="21512-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21512-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="21512-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21512-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="21512-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21512-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="21512-108">DESCRIPTION</span></span>
<span data-ttu-id="21512-109">O cmdlet **Stop-AzSynapsePipelineRun** interrompe um pipeline executado em um espaço de trabalho especificado com a ID de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="21512-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="21512-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21512-110">EXAMPLES</span></span>

### <span data-ttu-id="21512-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21512-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="21512-112">Este comando interrompe a operação do pipeline com a id b9730a13-aa12-4926-a8b3-8e3a974ab0bd no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="21512-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="21512-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21512-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="21512-114">Este comando interrompe o pipeline executado com a id b9730a13-aa12-4926-a8b3-8e3a974ab0bd no espaço de trabalho ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="21512-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="21512-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="21512-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="21512-116">Este comando interrompe o pipeline executado com a id b9730a13-aa12-4926-a8b3-8e3a974ab0bd no espaço de trabalho ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="21512-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="21512-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="21512-117">PARAMETERS</span></span>

### <span data-ttu-id="21512-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21512-118">-AsJob</span></span>
<span data-ttu-id="21512-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21512-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21512-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21512-120">-DefaultProfile</span></span>
<span data-ttu-id="21512-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21512-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21512-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21512-122">-InputObject</span></span>
<span data-ttu-id="21512-123">As informações sobre o pipeline são executados.</span><span class="sxs-lookup"><span data-stu-id="21512-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21512-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21512-124">-PassThru</span></span>
<span data-ttu-id="21512-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="21512-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="21512-126">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="21512-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="21512-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="21512-127">-PipelineRunId</span></span>
<span data-ttu-id="21512-128">O identificador de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="21512-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21512-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21512-129">-WorkspaceName</span></span>
<span data-ttu-id="21512-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="21512-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21512-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="21512-131">-WorkspaceObject</span></span>
<span data-ttu-id="21512-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="21512-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21512-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21512-133">-Confirm</span></span>
<span data-ttu-id="21512-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21512-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21512-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21512-135">-WhatIf</span></span>
<span data-ttu-id="21512-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21512-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21512-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21512-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21512-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21512-138">CommonParameters</span></span>
<span data-ttu-id="21512-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21512-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21512-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21512-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21512-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21512-141">INPUTS</span></span>

### <span data-ttu-id="21512-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="21512-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="21512-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="21512-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="21512-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="21512-144">OUTPUTS</span></span>

### <span data-ttu-id="21512-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21512-145">System.Boolean</span></span>

## <span data-ttu-id="21512-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="21512-146">NOTES</span></span>

## <span data-ttu-id="21512-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21512-147">RELATED LINKS</span></span>
