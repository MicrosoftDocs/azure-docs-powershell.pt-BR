---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272309"
---
# <span data-ttu-id="e8800-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="e8800-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="e8800-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8800-102">SYNOPSIS</span></span>
<span data-ttu-id="e8800-103">Interrompe uma execução de pipeline em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8800-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="e8800-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8800-104">SYNTAX</span></span>

### <span data-ttu-id="e8800-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8800-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8800-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e8800-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8800-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8800-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8800-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8800-108">DESCRIPTION</span></span>
<span data-ttu-id="e8800-109">O cmdlet **Stop-AzSynapsePipelineRun** interrompe uma execução de pipeline em um espaço de trabalho especificado com a ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8800-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="e8800-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8800-110">EXAMPLES</span></span>

### <span data-ttu-id="e8800-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8800-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="e8800-112">Esse comando interrompe o pipeline executado com ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8800-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e8800-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8800-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="e8800-114">Esse comando interrompe o pipeline executado com ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8800-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e8800-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e8800-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="e8800-116">Esse comando interrompe o pipeline executado com ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8800-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e8800-117">OS</span><span class="sxs-lookup"><span data-stu-id="e8800-117">PARAMETERS</span></span>

### <span data-ttu-id="e8800-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8800-118">-AsJob</span></span>
<span data-ttu-id="e8800-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e8800-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8800-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8800-120">-DefaultProfile</span></span>
<span data-ttu-id="e8800-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8800-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8800-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8800-122">-InputObject</span></span>
<span data-ttu-id="e8800-123">As informações sobre o pipeline são executadas.</span><span class="sxs-lookup"><span data-stu-id="e8800-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="e8800-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8800-124">-PassThru</span></span>
<span data-ttu-id="e8800-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e8800-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e8800-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8800-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e8800-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e8800-127">-PipelineRunId</span></span>
<span data-ttu-id="e8800-128">O identificador de execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8800-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="e8800-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e8800-129">-WorkspaceName</span></span>
<span data-ttu-id="e8800-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e8800-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e8800-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e8800-131">-WorkspaceObject</span></span>
<span data-ttu-id="e8800-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8800-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e8800-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8800-133">-Confirm</span></span>
<span data-ttu-id="e8800-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8800-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8800-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8800-135">-WhatIf</span></span>
<span data-ttu-id="e8800-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8800-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8800-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8800-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8800-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8800-138">CommonParameters</span></span>
<span data-ttu-id="e8800-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8800-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8800-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8800-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8800-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8800-141">INPUTS</span></span>

### <span data-ttu-id="e8800-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8800-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e8800-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e8800-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="e8800-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8800-144">OUTPUTS</span></span>

### <span data-ttu-id="e8800-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8800-145">System.Boolean</span></span>

## <span data-ttu-id="e8800-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8800-146">NOTES</span></span>

## <span data-ttu-id="e8800-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8800-147">RELATED LINKS</span></span>
