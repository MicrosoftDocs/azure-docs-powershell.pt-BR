---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272338"
---
# <span data-ttu-id="3a8b5-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3a8b5-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="3a8b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8b5-103">Cancele a assinatura do gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3a8b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a8b5-104">SYNTAX</span></span>

### <span data-ttu-id="3a8b5-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8b5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3a8b5-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8b5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a8b5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8b5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a8b5-108">DESCRIPTION</span></span>
<span data-ttu-id="3a8b5-109">O cmdlet **Remove-AzSynapseTriggerSubscription** cancela a assinatura do gatilho de evento para os eventos do serviço externo especificado da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3a8b5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a8b5-110">EXAMPLES</span></span>

### <span data-ttu-id="3a8b5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a8b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3a8b5-112">Esse comando irá cancelar a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do disparador.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="3a8b5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3a8b5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="3a8b5-114">Esse comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="3a8b5-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3a8b5-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="3a8b5-116">Esse comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="3a8b5-117">OS</span><span class="sxs-lookup"><span data-stu-id="3a8b5-117">PARAMETERS</span></span>

### <span data-ttu-id="3a8b5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8b5-118">-AsJob</span></span>
<span data-ttu-id="3a8b5-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3a8b5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a8b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8b5-120">-DefaultProfile</span></span>
<span data-ttu-id="3a8b5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8b5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3a8b5-122">-Force</span></span>
<span data-ttu-id="3a8b5-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a8b5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8b5-124">-InputObject</span></span>
<span data-ttu-id="3a8b5-125">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-125">The trigger object.</span></span>

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

### <span data-ttu-id="3a8b5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a8b5-126">-Name</span></span>
<span data-ttu-id="3a8b5-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-127">The trigger name.</span></span>

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

### <span data-ttu-id="3a8b5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a8b5-128">-PassThru</span></span>
<span data-ttu-id="3a8b5-129">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3a8b5-130">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a8b5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a8b5-131">-WorkspaceName</span></span>
<span data-ttu-id="3a8b5-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a8b5-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3a8b5-133">-WorkspaceObject</span></span>
<span data-ttu-id="3a8b5-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a8b5-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a8b5-135">-Confirm</span></span>
<span data-ttu-id="3a8b5-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8b5-137">-WhatIf</span></span>
<span data-ttu-id="3a8b5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a8b5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8b5-140">CommonParameters</span></span>
<span data-ttu-id="3a8b5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8b5-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8b5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a8b5-143">INPUTS</span></span>

### <span data-ttu-id="3a8b5-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a8b5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3a8b5-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3a8b5-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3a8b5-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a8b5-146">OUTPUTS</span></span>

### <span data-ttu-id="3a8b5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a8b5-147">System.Boolean</span></span>

## <span data-ttu-id="3a8b5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a8b5-148">NOTES</span></span>

## <span data-ttu-id="3a8b5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a8b5-149">RELATED LINKS</span></span>
