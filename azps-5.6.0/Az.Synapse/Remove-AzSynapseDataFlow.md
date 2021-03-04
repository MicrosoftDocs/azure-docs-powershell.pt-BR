---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: f5ed25a663f6f1841c4c2b6ca901d726a047eabd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886819"
---
# <span data-ttu-id="db914-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="db914-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="db914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db914-102">SYNOPSIS</span></span>
<span data-ttu-id="db914-103">Remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="db914-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="db914-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db914-104">SYNTAX</span></span>

### <span data-ttu-id="db914-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db914-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db914-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="db914-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db914-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="db914-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db914-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db914-108">DESCRIPTION</span></span>
<span data-ttu-id="db914-109">O cmdlet **Remove-AzSynapseDataFlow** remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="db914-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="db914-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db914-110">EXAMPLES</span></span>

### <span data-ttu-id="db914-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db914-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="db914-112">Este comando remove o fluxo de dados chamado ContosoDataFlow do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="db914-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="db914-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db914-113">PARAMETERS</span></span>

### <span data-ttu-id="db914-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db914-114">-AsJob</span></span>
<span data-ttu-id="db914-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="db914-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db914-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db914-116">-DefaultProfile</span></span>
<span data-ttu-id="db914-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db914-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db914-118">-Force</span><span class="sxs-lookup"><span data-stu-id="db914-118">-Force</span></span>
<span data-ttu-id="db914-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="db914-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="db914-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db914-120">-InputObject</span></span>
<span data-ttu-id="db914-121">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="db914-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db914-122">-Name</span><span class="sxs-lookup"><span data-stu-id="db914-122">-Name</span></span>
<span data-ttu-id="db914-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="db914-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db914-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db914-124">-PassThru</span></span>
<span data-ttu-id="db914-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="db914-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="db914-126">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="db914-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="db914-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db914-127">-WorkspaceName</span></span>
<span data-ttu-id="db914-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="db914-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="db914-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db914-129">-WorkspaceObject</span></span>
<span data-ttu-id="db914-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="db914-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="db914-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db914-131">-Confirm</span></span>
<span data-ttu-id="db914-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db914-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db914-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db914-133">-WhatIf</span></span>
<span data-ttu-id="db914-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db914-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db914-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db914-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db914-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db914-136">CommonParameters</span></span>
<span data-ttu-id="db914-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db914-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db914-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db914-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db914-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db914-139">INPUTS</span></span>

### <span data-ttu-id="db914-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db914-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="db914-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="db914-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="db914-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db914-142">OUTPUTS</span></span>

### <span data-ttu-id="db914-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db914-143">System.Boolean</span></span>

## <span data-ttu-id="db914-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="db914-144">NOTES</span></span>

## <span data-ttu-id="db914-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db914-145">RELATED LINKS</span></span>
