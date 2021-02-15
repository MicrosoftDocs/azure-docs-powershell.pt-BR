---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112419"
---
# <span data-ttu-id="8044d-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="8044d-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="8044d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8044d-102">SYNOPSIS</span></span>
<span data-ttu-id="8044d-103">Assine o gatilho do evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="8044d-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="8044d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8044d-104">SYNTAX</span></span>

### <span data-ttu-id="8044d-105">AddByName (Default)</span><span class="sxs-lookup"><span data-stu-id="8044d-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8044d-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="8044d-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8044d-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="8044d-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8044d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8044d-108">DESCRIPTION</span></span>
<span data-ttu-id="8044d-109">O cmdlet **Add-AzSynapseTriscriptionSubscription** assina o gatilho de evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="8044d-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="8044d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8044d-110">EXAMPLES</span></span>

### <span data-ttu-id="8044d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8044d-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="8044d-112">Esse comando assinará o gatilho chamado ContosoTrifique para os eventos especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="8044d-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="8044d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8044d-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="8044d-114">Esse comando assinará o gatilho chamado ContosoTri pipeline para os eventos especificados a partir da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8044d-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="8044d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8044d-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="8044d-116">Esse comando assinará o gatilho chamado ContosoTri pipeline para os eventos especificados a partir da definição do gatilho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8044d-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="8044d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8044d-117">PARAMETERS</span></span>

### <span data-ttu-id="8044d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8044d-118">-AsJob</span></span>
<span data-ttu-id="8044d-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8044d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8044d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8044d-120">-DefaultProfile</span></span>
<span data-ttu-id="8044d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8044d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8044d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8044d-122">-InputObject</span></span>
<span data-ttu-id="8044d-123">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="8044d-123">The trigger object.</span></span>

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

### <span data-ttu-id="8044d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8044d-124">-Name</span></span>
<span data-ttu-id="8044d-125">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="8044d-125">The trigger name.</span></span>

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

### <span data-ttu-id="8044d-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8044d-126">-WorkspaceName</span></span>
<span data-ttu-id="8044d-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8044d-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8044d-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8044d-128">-WorkspaceObject</span></span>
<span data-ttu-id="8044d-129">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8044d-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8044d-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8044d-130">-Confirm</span></span>
<span data-ttu-id="8044d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8044d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8044d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8044d-132">-WhatIf</span></span>
<span data-ttu-id="8044d-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8044d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8044d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8044d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8044d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8044d-135">CommonParameters</span></span>
<span data-ttu-id="8044d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8044d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8044d-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8044d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8044d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="8044d-138">INPUTS</span></span>

### <span data-ttu-id="8044d-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8044d-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8044d-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="8044d-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="8044d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="8044d-141">OUTPUTS</span></span>

### <span data-ttu-id="8044d-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="8044d-142">System.Object</span></span>
## <span data-ttu-id="8044d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="8044d-143">NOTES</span></span>

## <span data-ttu-id="8044d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8044d-144">RELATED LINKS</span></span>
