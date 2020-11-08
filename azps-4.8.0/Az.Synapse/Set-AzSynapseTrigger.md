---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112483"
---
# <span data-ttu-id="6bd21-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="6bd21-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="6bd21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bd21-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd21-103">Cria um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6bd21-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="6bd21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bd21-104">SYNTAX</span></span>

### <span data-ttu-id="6bd21-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6bd21-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd21-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="6bd21-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd21-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bd21-107">DESCRIPTION</span></span>
<span data-ttu-id="6bd21-108">O cmdlet **set-AzSynapseTrigger** cria um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6bd21-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="6bd21-109">Os gatilhos são criados no estado "interrompido", o que significa que eles não começam a invocar imediatamente os pipelines referenciados.</span><span class="sxs-lookup"><span data-stu-id="6bd21-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="6bd21-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bd21-110">EXAMPLES</span></span>

### <span data-ttu-id="6bd21-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bd21-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="6bd21-112">Crie um novo gatilho chamado ContosoTrigger na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6bd21-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="6bd21-113">O gatilho é criado no estado "parado", o que significa que ele não é iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6bd21-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="6bd21-114">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd21-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="6bd21-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6bd21-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="6bd21-116">Crie um novo gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6bd21-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="6bd21-117">O gatilho é criado no estado "parado", o que significa que ele não é iniciado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6bd21-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="6bd21-118">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd21-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="6bd21-119">OS</span><span class="sxs-lookup"><span data-stu-id="6bd21-119">PARAMETERS</span></span>

### <span data-ttu-id="6bd21-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bd21-120">-AsJob</span></span>
<span data-ttu-id="6bd21-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6bd21-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bd21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd21-122">-DefaultProfile</span></span>
<span data-ttu-id="6bd21-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bd21-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bd21-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6bd21-124">-DefinitionFile</span></span>
<span data-ttu-id="6bd21-125">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="6bd21-125">The JSON file path.</span></span>

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

### <span data-ttu-id="6bd21-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bd21-126">-Name</span></span>
<span data-ttu-id="6bd21-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="6bd21-127">The trigger name.</span></span>

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

### <span data-ttu-id="6bd21-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6bd21-128">-WorkspaceName</span></span>
<span data-ttu-id="6bd21-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="6bd21-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6bd21-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6bd21-130">-WorkspaceObject</span></span>
<span data-ttu-id="6bd21-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6bd21-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6bd21-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6bd21-132">-Confirm</span></span>
<span data-ttu-id="6bd21-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd21-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd21-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd21-134">-WhatIf</span></span>
<span data-ttu-id="6bd21-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bd21-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd21-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bd21-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd21-137">CommonParameters</span></span>
<span data-ttu-id="6bd21-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd21-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bd21-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd21-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bd21-140">INPUTS</span></span>

### <span data-ttu-id="6bd21-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6bd21-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6bd21-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bd21-142">OUTPUTS</span></span>

### <span data-ttu-id="6bd21-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="6bd21-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="6bd21-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bd21-144">NOTES</span></span>

## <span data-ttu-id="6bd21-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bd21-145">RELATED LINKS</span></span>
