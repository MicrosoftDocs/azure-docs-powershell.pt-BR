---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272459"
---
# <span data-ttu-id="335a5-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="335a5-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="335a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="335a5-102">SYNOPSIS</span></span>
<span data-ttu-id="335a5-103">Assine o gatilho de evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="335a5-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="335a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="335a5-104">SYNTAX</span></span>

### <span data-ttu-id="335a5-105">AddByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="335a5-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335a5-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="335a5-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="335a5-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="335a5-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="335a5-108">DESCRIPTION</span></span>
<span data-ttu-id="335a5-109">O cmdlet **Add-AzSynapseTriggerSubscription** assina o gatilho de evento para os eventos do serviço externo especificado da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="335a5-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="335a5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="335a5-110">EXAMPLES</span></span>

### <span data-ttu-id="335a5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="335a5-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="335a5-112">Esse comando inscreverá o gatilho chamado ContosoTrigger para os eventos especificados da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="335a5-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="335a5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="335a5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="335a5-114">Esse comando inscreverá o gatilho chamado ContosoTrigger para os eventos especificados da definição do disparador por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="335a5-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="335a5-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="335a5-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="335a5-116">Esse comando inscreverá o gatilho chamado ContosoTrigger para os eventos especificados da definição do disparador por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="335a5-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="335a5-117">OS</span><span class="sxs-lookup"><span data-stu-id="335a5-117">PARAMETERS</span></span>

### <span data-ttu-id="335a5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="335a5-118">-AsJob</span></span>
<span data-ttu-id="335a5-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="335a5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="335a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335a5-120">-DefaultProfile</span></span>
<span data-ttu-id="335a5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="335a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="335a5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="335a5-122">-InputObject</span></span>
<span data-ttu-id="335a5-123">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="335a5-123">The trigger object.</span></span>

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

### <span data-ttu-id="335a5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="335a5-124">-Name</span></span>
<span data-ttu-id="335a5-125">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="335a5-125">The trigger name.</span></span>

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

### <span data-ttu-id="335a5-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="335a5-126">-WorkspaceName</span></span>
<span data-ttu-id="335a5-127">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="335a5-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="335a5-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="335a5-128">-WorkspaceObject</span></span>
<span data-ttu-id="335a5-129">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="335a5-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="335a5-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="335a5-130">-Confirm</span></span>
<span data-ttu-id="335a5-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="335a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335a5-132">-WhatIf</span></span>
<span data-ttu-id="335a5-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="335a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335a5-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="335a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335a5-135">CommonParameters</span></span>
<span data-ttu-id="335a5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335a5-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="335a5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335a5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="335a5-138">INPUTS</span></span>

### <span data-ttu-id="335a5-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="335a5-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="335a5-140">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="335a5-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="335a5-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="335a5-141">OUTPUTS</span></span>

### <span data-ttu-id="335a5-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="335a5-142">System.Object</span></span>
## <span data-ttu-id="335a5-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="335a5-143">NOTES</span></span>

## <span data-ttu-id="335a5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="335a5-144">RELATED LINKS</span></span>
