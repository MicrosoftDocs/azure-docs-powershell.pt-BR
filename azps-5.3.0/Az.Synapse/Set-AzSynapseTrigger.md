---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429607"
---
# <span data-ttu-id="402fc-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="402fc-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="402fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="402fc-102">SYNOPSIS</span></span>
<span data-ttu-id="402fc-103">Cria um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="402fc-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="402fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="402fc-104">SYNTAX</span></span>

### <span data-ttu-id="402fc-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="402fc-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="402fc-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="402fc-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="402fc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="402fc-107">DESCRIPTION</span></span>
<span data-ttu-id="402fc-108">O cmdlet **set-AzSynapseTrigger** cria um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="402fc-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="402fc-109">Os gatilhos são criados no estado "interrompido", o que significa que eles não começam a invocar imediatamente os pipelines referenciados.</span><span class="sxs-lookup"><span data-stu-id="402fc-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="402fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="402fc-110">EXAMPLES</span></span>

### <span data-ttu-id="402fc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="402fc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="402fc-112">Crie um novo gatilho chamado ContosoTrigger na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="402fc-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="402fc-113">O gatilho é criado no estado "parado", o que significa que ele não é iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="402fc-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="402fc-114">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402fc-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="402fc-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="402fc-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="402fc-116">Crie um novo gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="402fc-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="402fc-117">O gatilho é criado no estado "parado", o que significa que ele não é iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="402fc-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="402fc-118">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402fc-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="402fc-119">OS</span><span class="sxs-lookup"><span data-stu-id="402fc-119">PARAMETERS</span></span>

### <span data-ttu-id="402fc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="402fc-120">-AsJob</span></span>
<span data-ttu-id="402fc-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="402fc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="402fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402fc-122">-DefaultProfile</span></span>
<span data-ttu-id="402fc-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="402fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="402fc-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="402fc-124">-DefinitionFile</span></span>
<span data-ttu-id="402fc-125">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="402fc-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402fc-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="402fc-126">-Name</span></span>
<span data-ttu-id="402fc-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="402fc-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402fc-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="402fc-128">-WorkspaceName</span></span>
<span data-ttu-id="402fc-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="402fc-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402fc-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="402fc-130">-WorkspaceObject</span></span>
<span data-ttu-id="402fc-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="402fc-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="402fc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="402fc-132">-Confirm</span></span>
<span data-ttu-id="402fc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402fc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402fc-134">-WhatIf</span></span>
<span data-ttu-id="402fc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="402fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="402fc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="402fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402fc-137">CommonParameters</span></span>
<span data-ttu-id="402fc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402fc-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="402fc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402fc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="402fc-140">INPUTS</span></span>

### <span data-ttu-id="402fc-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="402fc-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="402fc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="402fc-142">OUTPUTS</span></span>

### <span data-ttu-id="402fc-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="402fc-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="402fc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="402fc-144">NOTES</span></span>

## <span data-ttu-id="402fc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="402fc-145">RELATED LINKS</span></span>
