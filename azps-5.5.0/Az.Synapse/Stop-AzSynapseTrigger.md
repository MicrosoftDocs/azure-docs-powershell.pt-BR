---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116044"
---
# <span data-ttu-id="e8aec-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="e8aec-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="e8aec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8aec-102">SYNOPSIS</span></span>
<span data-ttu-id="e8aec-103">Interrompe um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8aec-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="e8aec-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8aec-104">SYNTAX</span></span>

### <span data-ttu-id="e8aec-105">StopByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8aec-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8aec-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="e8aec-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8aec-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8aec-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8aec-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8aec-108">DESCRIPTION</span></span>
<span data-ttu-id="e8aec-109">O **cmdlet Stop-AzSynapseTrishot** interrompe um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8aec-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="e8aec-110">Se o gatilho estiver no estado "Iniciado", o cmdlet parará o gatilho e não invocará mais os pipelines.</span><span class="sxs-lookup"><span data-stu-id="e8aec-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="e8aec-111">Se o gatilho já estiver no estado "Parado", esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="e8aec-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="e8aec-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8aec-112">EXAMPLES</span></span>

### <span data-ttu-id="e8aec-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8aec-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="e8aec-114">Interrompe um gatilho chamado ContosoTrição no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8aec-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e8aec-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8aec-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="e8aec-116">Interrompe um gatilho chamado ContosoTri pipeline no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8aec-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e8aec-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e8aec-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="e8aec-118">Parar um gatilho chamado ContosoTri pipeline no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e8aec-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e8aec-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8aec-119">PARAMETERS</span></span>

### <span data-ttu-id="e8aec-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8aec-120">-AsJob</span></span>
<span data-ttu-id="e8aec-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e8aec-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8aec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8aec-122">-DefaultProfile</span></span>
<span data-ttu-id="e8aec-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8aec-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8aec-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8aec-124">-InputObject</span></span>
<span data-ttu-id="e8aec-125">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="e8aec-125">The trigger object.</span></span>

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

### <span data-ttu-id="e8aec-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8aec-126">-Name</span></span>
<span data-ttu-id="e8aec-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="e8aec-127">The trigger name.</span></span>

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

### <span data-ttu-id="e8aec-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8aec-128">-PassThru</span></span>
<span data-ttu-id="e8aec-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e8aec-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e8aec-130">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8aec-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e8aec-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="e8aec-131">-WorkspaceName</span></span>
<span data-ttu-id="e8aec-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e8aec-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e8aec-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e8aec-133">-WorkspaceObject</span></span>
<span data-ttu-id="e8aec-134">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8aec-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e8aec-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e8aec-135">-Confirm</span></span>
<span data-ttu-id="e8aec-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8aec-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8aec-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8aec-137">-WhatIf</span></span>
<span data-ttu-id="e8aec-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e8aec-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8aec-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8aec-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8aec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8aec-140">CommonParameters</span></span>
<span data-ttu-id="e8aec-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8aec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8aec-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8aec-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8aec-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="e8aec-143">INPUTS</span></span>

### <span data-ttu-id="e8aec-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8aec-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e8aec-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="e8aec-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="e8aec-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="e8aec-146">OUTPUTS</span></span>

### <span data-ttu-id="e8aec-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8aec-147">System.Boolean</span></span>

## <span data-ttu-id="e8aec-148">Notas</span><span class="sxs-lookup"><span data-stu-id="e8aec-148">NOTES</span></span>

## <span data-ttu-id="e8aec-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8aec-149">RELATED LINKS</span></span>
