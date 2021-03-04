---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889058"
---
# <span data-ttu-id="6409b-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="6409b-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="6409b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6409b-102">SYNOPSIS</span></span>
<span data-ttu-id="6409b-103">Assine o gatilho do evento para eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="6409b-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="6409b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6409b-104">SYNTAX</span></span>

### <span data-ttu-id="6409b-105">AddByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6409b-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6409b-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="6409b-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6409b-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="6409b-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6409b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6409b-108">DESCRIPTION</span></span>
<span data-ttu-id="6409b-109">O cmdlet **Add-AzSynapseTriggerSubscription** assina o gatilho de eventos para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="6409b-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="6409b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6409b-110">EXAMPLES</span></span>

### <span data-ttu-id="6409b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6409b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="6409b-112">Este comando assinará o gatilho chamado ContosoTrigger para os eventos especificados na definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="6409b-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="6409b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6409b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="6409b-114">Este comando assinará o gatilho chamado ContosoTrigger para os eventos especificados a partir da definição do gatilho por pipeline.</span><span class="sxs-lookup"><span data-stu-id="6409b-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="6409b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6409b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="6409b-116">Este comando assinará o gatilho chamado ContosoTrigger para os eventos especificados a partir da definição do gatilho por pipeline.</span><span class="sxs-lookup"><span data-stu-id="6409b-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="6409b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6409b-117">PARAMETERS</span></span>

### <span data-ttu-id="6409b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6409b-118">-AsJob</span></span>
<span data-ttu-id="6409b-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6409b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6409b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6409b-120">-DefaultProfile</span></span>
<span data-ttu-id="6409b-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6409b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6409b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6409b-122">-InputObject</span></span>
<span data-ttu-id="6409b-123">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="6409b-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6409b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6409b-124">-Name</span></span>
<span data-ttu-id="6409b-125">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="6409b-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6409b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6409b-126">-WorkspaceName</span></span>
<span data-ttu-id="6409b-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="6409b-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6409b-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6409b-128">-WorkspaceObject</span></span>
<span data-ttu-id="6409b-129">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6409b-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6409b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6409b-130">-Confirm</span></span>
<span data-ttu-id="6409b-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6409b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6409b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6409b-132">-WhatIf</span></span>
<span data-ttu-id="6409b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6409b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6409b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6409b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6409b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6409b-135">CommonParameters</span></span>
<span data-ttu-id="6409b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6409b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6409b-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6409b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6409b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6409b-138">INPUTS</span></span>

### <span data-ttu-id="6409b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6409b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6409b-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="6409b-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="6409b-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6409b-141">OUTPUTS</span></span>

### <span data-ttu-id="6409b-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="6409b-142">System.Object</span></span>
## <span data-ttu-id="6409b-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="6409b-143">NOTES</span></span>

## <span data-ttu-id="6409b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6409b-144">RELATED LINKS</span></span>
