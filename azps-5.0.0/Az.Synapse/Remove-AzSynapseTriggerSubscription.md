---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117134"
---
# <span data-ttu-id="c5255-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="c5255-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="c5255-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5255-102">SYNOPSIS</span></span>
<span data-ttu-id="c5255-103">Cancele a assinatura do gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="c5255-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="c5255-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5255-104">SYNTAX</span></span>

### <span data-ttu-id="c5255-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5255-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5255-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c5255-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5255-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5255-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5255-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5255-108">DESCRIPTION</span></span>
<span data-ttu-id="c5255-109">O cmdlet **Remove-AzSynapseTriggerSubscription** cancela a assinatura do gatilho de evento para os eventos do serviço externo especificado da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="c5255-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="c5255-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5255-110">EXAMPLES</span></span>

### <span data-ttu-id="c5255-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5255-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c5255-112">Esse comando irá cancelar a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do disparador.</span><span class="sxs-lookup"><span data-stu-id="c5255-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="c5255-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5255-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="c5255-114">Esse comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5255-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="c5255-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5255-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="c5255-116">Esse comando cancelará a assinatura do gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5255-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="c5255-117">OS</span><span class="sxs-lookup"><span data-stu-id="c5255-117">PARAMETERS</span></span>

### <span data-ttu-id="c5255-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5255-118">-AsJob</span></span>
<span data-ttu-id="c5255-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c5255-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5255-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5255-120">-DefaultProfile</span></span>
<span data-ttu-id="c5255-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5255-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5255-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5255-122">-InputObject</span></span>
<span data-ttu-id="c5255-123">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="c5255-123">The trigger object.</span></span>

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

### <span data-ttu-id="c5255-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5255-124">-Name</span></span>
<span data-ttu-id="c5255-125">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="c5255-125">The trigger name.</span></span>

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

### <span data-ttu-id="c5255-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5255-126">-PassThru</span></span>
<span data-ttu-id="c5255-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="c5255-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c5255-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5255-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c5255-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5255-129">-WorkspaceName</span></span>
<span data-ttu-id="c5255-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="c5255-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c5255-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c5255-131">-WorkspaceObject</span></span>
<span data-ttu-id="c5255-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5255-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c5255-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5255-133">-Confirm</span></span>
<span data-ttu-id="c5255-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5255-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5255-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5255-135">-WhatIf</span></span>
<span data-ttu-id="c5255-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5255-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5255-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5255-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5255-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5255-138">CommonParameters</span></span>
<span data-ttu-id="c5255-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5255-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5255-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5255-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5255-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5255-141">INPUTS</span></span>

### <span data-ttu-id="c5255-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5255-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5255-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c5255-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c5255-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5255-144">OUTPUTS</span></span>

### <span data-ttu-id="c5255-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5255-145">System.Boolean</span></span>

## <span data-ttu-id="c5255-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5255-146">NOTES</span></span>

## <span data-ttu-id="c5255-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5255-147">RELATED LINKS</span></span>
