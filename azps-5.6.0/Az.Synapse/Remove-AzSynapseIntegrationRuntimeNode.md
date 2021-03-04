---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893065"
---
# <span data-ttu-id="e9f5c-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="e9f5c-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="e9f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f5c-103">Remova um nó com o nome dado em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="e9f5c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e9f5c-104">SYNTAX</span></span>

### <span data-ttu-id="e9f5c-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9f5c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f5c-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f5c-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f5c-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f5c-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f5c-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f5c-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f5c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e9f5c-109">DESCRIPTION</span></span>
<span data-ttu-id="e9f5c-110">O cmdlet **Remove-AzSynapseIntegrationRuntimeNode** remove um nó em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="e9f5c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-111">EXAMPLES</span></span>

### <span data-ttu-id="e9f5c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9f5c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="e9f5c-113">Remova um nó com o nome dado em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="e9f5c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-114">PARAMETERS</span></span>

### <span data-ttu-id="e9f5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f5c-115">-DefaultProfile</span></span>
<span data-ttu-id="e9f5c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f5c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e9f5c-117">-Force</span></span>
<span data-ttu-id="e9f5c-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e9f5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9f5c-119">-InputObject</span></span>
<span data-ttu-id="e9f5c-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e9f5c-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e9f5c-122">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="e9f5c-123">-NodeName</span></span>
<span data-ttu-id="e9f5c-124">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f5c-125">-ResourceGroupName</span></span>
<span data-ttu-id="e9f5c-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f5c-127">-ResourceId</span></span>
<span data-ttu-id="e9f5c-128">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9f5c-129">-WorkspaceName</span></span>
<span data-ttu-id="e9f5c-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9f5c-131">-WorkspaceObject</span></span>
<span data-ttu-id="e9f5c-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f5c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9f5c-133">-Confirm</span></span>
<span data-ttu-id="e9f5c-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f5c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f5c-135">-WhatIf</span></span>
<span data-ttu-id="e9f5c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f5c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f5c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f5c-138">CommonParameters</span></span>
<span data-ttu-id="e9f5c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f5c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f5c-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9f5c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f5c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-141">INPUTS</span></span>

### <span data-ttu-id="e9f5c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9f5c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e9f5c-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e9f5c-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="e9f5c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f5c-144">System.String</span></span>

## <span data-ttu-id="e9f5c-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-145">OUTPUTS</span></span>

### <span data-ttu-id="e9f5c-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="e9f5c-146">System.Void</span></span>

## <span data-ttu-id="e9f5c-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="e9f5c-147">NOTES</span></span>

## <span data-ttu-id="e9f5c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9f5c-148">RELATED LINKS</span></span>
