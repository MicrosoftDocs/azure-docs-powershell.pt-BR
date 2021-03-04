---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 94773a882a4bb2d29712fff6796d34cff6254df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890516"
---
# <span data-ttu-id="b275e-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="b275e-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="b275e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b275e-102">SYNOPSIS</span></span>
<span data-ttu-id="b275e-103">Interrompe um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b275e-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="b275e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b275e-104">SYNTAX</span></span>

### <span data-ttu-id="b275e-105">StopByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b275e-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b275e-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="b275e-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b275e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="b275e-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b275e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b275e-108">DESCRIPTION</span></span>
<span data-ttu-id="b275e-109">O cmdlet **Stop-AzSynapseTrigger** interrompe um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b275e-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="b275e-110">Se o gatilho estiver no estado 'Iniciado', o cmdlet interrompe o gatilho e não invoca mais pipelines.</span><span class="sxs-lookup"><span data-stu-id="b275e-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="b275e-111">Se o gatilho já estiver no estado 'Parado', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="b275e-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="b275e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b275e-112">EXAMPLES</span></span>

### <span data-ttu-id="b275e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b275e-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b275e-114">Interrompe um gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b275e-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b275e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b275e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="b275e-116">Interrompe um gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b275e-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b275e-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b275e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="b275e-118">Pare um gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b275e-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b275e-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b275e-119">PARAMETERS</span></span>

### <span data-ttu-id="b275e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b275e-120">-AsJob</span></span>
<span data-ttu-id="b275e-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b275e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b275e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b275e-122">-DefaultProfile</span></span>
<span data-ttu-id="b275e-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b275e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b275e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b275e-124">-InputObject</span></span>
<span data-ttu-id="b275e-125">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="b275e-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b275e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b275e-126">-Name</span></span>
<span data-ttu-id="b275e-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="b275e-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b275e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b275e-128">-PassThru</span></span>
<span data-ttu-id="b275e-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="b275e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b275e-130">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="b275e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b275e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b275e-131">-WorkspaceName</span></span>
<span data-ttu-id="b275e-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b275e-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b275e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b275e-133">-WorkspaceObject</span></span>
<span data-ttu-id="b275e-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b275e-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b275e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b275e-135">-Confirm</span></span>
<span data-ttu-id="b275e-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b275e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b275e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b275e-137">-WhatIf</span></span>
<span data-ttu-id="b275e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b275e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b275e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b275e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b275e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b275e-140">CommonParameters</span></span>
<span data-ttu-id="b275e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b275e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b275e-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b275e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b275e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b275e-143">INPUTS</span></span>

### <span data-ttu-id="b275e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b275e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b275e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b275e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b275e-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b275e-146">OUTPUTS</span></span>

### <span data-ttu-id="b275e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b275e-147">System.Boolean</span></span>

## <span data-ttu-id="b275e-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="b275e-148">NOTES</span></span>

## <span data-ttu-id="b275e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b275e-149">RELATED LINKS</span></span>
