---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118534"
---
# <span data-ttu-id="3d56a-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="3d56a-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="3d56a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d56a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d56a-103">Cria um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3d56a-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="3d56a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d56a-104">SYNTAX</span></span>

### <span data-ttu-id="3d56a-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d56a-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d56a-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="3d56a-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d56a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d56a-107">DESCRIPTION</span></span>
<span data-ttu-id="3d56a-108">O **cmdlet Set-AzSynapseTrishot cria** um gatilho em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3d56a-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="3d56a-109">Os gatilhos são criados no estado "Parado", o que significa que eles não começam imediatamente a invocar pipelines referenciados.</span><span class="sxs-lookup"><span data-stu-id="3d56a-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="3d56a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d56a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d56a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d56a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="3d56a-112">Crie um novo gatilho chamado ContosoTrição no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3d56a-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="3d56a-113">O gatilho é criado no estado "Parado", o que significa que ele não inicia imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3d56a-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="3d56a-114">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d56a-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="3d56a-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d56a-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="3d56a-116">Crie um novo gatilho chamado ContosoTri pipeline no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3d56a-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="3d56a-117">O gatilho é criado no estado "Parado", o que significa que ele não inicia imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3d56a-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="3d56a-118">Um gatilho pode ser iniciado usando o `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d56a-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="3d56a-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d56a-119">PARAMETERS</span></span>

### <span data-ttu-id="3d56a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d56a-120">-AsJob</span></span>
<span data-ttu-id="3d56a-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3d56a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d56a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d56a-122">-DefaultProfile</span></span>
<span data-ttu-id="3d56a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d56a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d56a-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3d56a-124">-DefinitionFile</span></span>
<span data-ttu-id="3d56a-125">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="3d56a-125">The JSON file path.</span></span>

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

### <span data-ttu-id="3d56a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d56a-126">-Name</span></span>
<span data-ttu-id="3d56a-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3d56a-127">The trigger name.</span></span>

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

### <span data-ttu-id="3d56a-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="3d56a-128">-WorkspaceName</span></span>
<span data-ttu-id="3d56a-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3d56a-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3d56a-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3d56a-130">-WorkspaceObject</span></span>
<span data-ttu-id="3d56a-131">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d56a-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3d56a-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3d56a-132">-Confirm</span></span>
<span data-ttu-id="3d56a-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d56a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d56a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d56a-134">-WhatIf</span></span>
<span data-ttu-id="3d56a-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3d56a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d56a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d56a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d56a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d56a-137">CommonParameters</span></span>
<span data-ttu-id="3d56a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d56a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d56a-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d56a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d56a-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="3d56a-140">INPUTS</span></span>

### <span data-ttu-id="3d56a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d56a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3d56a-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="3d56a-142">OUTPUTS</span></span>

### <span data-ttu-id="3d56a-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3d56a-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3d56a-144">Notas</span><span class="sxs-lookup"><span data-stu-id="3d56a-144">NOTES</span></span>

## <span data-ttu-id="3d56a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d56a-145">RELATED LINKS</span></span>
