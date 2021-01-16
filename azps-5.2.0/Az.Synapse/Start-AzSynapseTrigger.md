---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257394"
---
# <span data-ttu-id="4b3d2-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="4b3d2-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="4b3d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3d2-103">Inicia um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="4b3d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b3d2-104">SYNTAX</span></span>

### <span data-ttu-id="4b3d2-105">StartByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b3d2-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3d2-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="4b3d2-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3d2-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b3d2-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3d2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b3d2-108">DESCRIPTION</span></span>
<span data-ttu-id="4b3d2-109">O cmdlet **Start-AzSynapseTrigger** inicia um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="4b3d2-110">Se o gatilho estiver no estado ' parado ', o cmdlet iniciará o gatilho e eventualmente invocará os pipelines com base em sua definição.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="4b3d2-111">Se o gatilho já estiver no estado ' iniciado ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="4b3d2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b3d2-112">EXAMPLES</span></span>

### <span data-ttu-id="4b3d2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b3d2-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="4b3d2-114">Inicia um gatilho chamado ContosoTrigger na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="4b3d2-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4b3d2-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="4b3d2-116">Inicia um gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4b3d2-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4b3d2-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="4b3d2-118">Inicia um gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4b3d2-119">OS</span><span class="sxs-lookup"><span data-stu-id="4b3d2-119">PARAMETERS</span></span>

### <span data-ttu-id="4b3d2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b3d2-120">-AsJob</span></span>
<span data-ttu-id="4b3d2-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4b3d2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b3d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3d2-122">-DefaultProfile</span></span>
<span data-ttu-id="4b3d2-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b3d2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b3d2-124">-InputObject</span></span>
<span data-ttu-id="4b3d2-125">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3d2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b3d2-126">-Name</span></span>
<span data-ttu-id="4b3d2-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3d2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b3d2-128">-PassThru</span></span>
<span data-ttu-id="4b3d2-129">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4b3d2-130">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4b3d2-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4b3d2-131">-WorkspaceName</span></span>
<span data-ttu-id="4b3d2-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3d2-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4b3d2-133">-WorkspaceObject</span></span>
<span data-ttu-id="4b3d2-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3d2-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b3d2-135">-Confirm</span></span>
<span data-ttu-id="4b3d2-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b3d2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3d2-137">-WhatIf</span></span>
<span data-ttu-id="4b3d2-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b3d2-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b3d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3d2-140">CommonParameters</span></span>
<span data-ttu-id="4b3d2-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3d2-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b3d2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3d2-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b3d2-143">INPUTS</span></span>

### <span data-ttu-id="4b3d2-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b3d2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4b3d2-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="4b3d2-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="4b3d2-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b3d2-146">OUTPUTS</span></span>

### <span data-ttu-id="4b3d2-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b3d2-147">System.Boolean</span></span>

## <span data-ttu-id="4b3d2-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b3d2-148">NOTES</span></span>

## <span data-ttu-id="4b3d2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b3d2-149">RELATED LINKS</span></span>
