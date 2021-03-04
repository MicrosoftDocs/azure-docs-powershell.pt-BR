---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: f331cad857fba20d72ffdd34f84f70a5d6392bff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891918"
---
# <span data-ttu-id="0e67b-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="0e67b-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="0e67b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e67b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e67b-103">Cancelar a assinatura do gatilho de eventos para eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="0e67b-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="0e67b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0e67b-104">SYNTAX</span></span>

### <span data-ttu-id="0e67b-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e67b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e67b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0e67b-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e67b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e67b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e67b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0e67b-108">DESCRIPTION</span></span>
<span data-ttu-id="0e67b-109">O cmdlet **Remove-AzSynapseTriggerSubscription** cancela a assinatura do gatilho de eventos para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="0e67b-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="0e67b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e67b-110">EXAMPLES</span></span>

### <span data-ttu-id="0e67b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e67b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="0e67b-112">Este comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="0e67b-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="0e67b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0e67b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="0e67b-114">Este comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados a partir da definição do gatilho pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e67b-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="0e67b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0e67b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="0e67b-116">Este comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados a partir da definição do gatilho pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e67b-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="0e67b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0e67b-117">PARAMETERS</span></span>

### <span data-ttu-id="0e67b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e67b-118">-AsJob</span></span>
<span data-ttu-id="0e67b-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0e67b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e67b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e67b-120">-DefaultProfile</span></span>
<span data-ttu-id="0e67b-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e67b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e67b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0e67b-122">-Force</span></span>
<span data-ttu-id="0e67b-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0e67b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0e67b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e67b-124">-InputObject</span></span>
<span data-ttu-id="0e67b-125">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="0e67b-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e67b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0e67b-126">-Name</span></span>
<span data-ttu-id="0e67b-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="0e67b-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e67b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e67b-128">-PassThru</span></span>
<span data-ttu-id="0e67b-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="0e67b-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0e67b-130">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="0e67b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0e67b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e67b-131">-WorkspaceName</span></span>
<span data-ttu-id="0e67b-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0e67b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0e67b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0e67b-133">-WorkspaceObject</span></span>
<span data-ttu-id="0e67b-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e67b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0e67b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e67b-135">-Confirm</span></span>
<span data-ttu-id="0e67b-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e67b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e67b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e67b-137">-WhatIf</span></span>
<span data-ttu-id="0e67b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e67b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e67b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e67b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e67b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e67b-140">CommonParameters</span></span>
<span data-ttu-id="0e67b-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e67b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e67b-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e67b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e67b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e67b-143">INPUTS</span></span>

### <span data-ttu-id="0e67b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e67b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0e67b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="0e67b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="0e67b-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0e67b-146">OUTPUTS</span></span>

### <span data-ttu-id="0e67b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e67b-147">System.Boolean</span></span>

## <span data-ttu-id="0e67b-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="0e67b-148">NOTES</span></span>

## <span data-ttu-id="0e67b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e67b-149">RELATED LINKS</span></span>
