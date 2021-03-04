---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: bf15d0f533f54de589ef354d92c4cf2f600b12cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886521"
---
# <span data-ttu-id="a7ff7-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7ff7-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="a7ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ff7-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="a7ff7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7ff7-104">SYNTAX</span></span>

### <span data-ttu-id="a7ff7-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7ff7-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ff7-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7ff7-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ff7-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7ff7-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ff7-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7ff7-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ff7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7ff7-109">DESCRIPTION</span></span>
<span data-ttu-id="a7ff7-110">O cmdlet **Remove-AzSynapseIntegrationRuntime** remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="a7ff7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-111">EXAMPLES</span></span>

### <span data-ttu-id="a7ff7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7ff7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="a7ff7-113">Este comando remove o tempo de execução de integração chamado 'test-reserved-ir' do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a7ff7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-114">PARAMETERS</span></span>

### <span data-ttu-id="a7ff7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ff7-115">-DefaultProfile</span></span>
<span data-ttu-id="a7ff7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ff7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7ff7-117">-Force</span></span>
<span data-ttu-id="a7ff7-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a7ff7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7ff7-119">-InputObject</span></span>
<span data-ttu-id="a7ff7-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a7ff7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a7ff7-121">-Name</span></span>
<span data-ttu-id="a7ff7-122">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ff7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ff7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7ff7-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-124">Resource group name.</span></span>

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

### <span data-ttu-id="a7ff7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7ff7-125">-ResourceId</span></span>
<span data-ttu-id="a7ff7-126">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a7ff7-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a7ff7-127">-WorkspaceName</span></span>
<span data-ttu-id="a7ff7-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a7ff7-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a7ff7-129">-WorkspaceObject</span></span>
<span data-ttu-id="a7ff7-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a7ff7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7ff7-131">-Confirm</span></span>
<span data-ttu-id="a7ff7-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ff7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ff7-133">-WhatIf</span></span>
<span data-ttu-id="a7ff7-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ff7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ff7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ff7-136">CommonParameters</span></span>
<span data-ttu-id="a7ff7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ff7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ff7-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7ff7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ff7-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-139">INPUTS</span></span>

### <span data-ttu-id="a7ff7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a7ff7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a7ff7-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7ff7-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a7ff7-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-142">OUTPUTS</span></span>

### <span data-ttu-id="a7ff7-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7ff7-143">System.Void</span></span>

## <span data-ttu-id="a7ff7-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7ff7-144">NOTES</span></span>

## <span data-ttu-id="a7ff7-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7ff7-145">RELATED LINKS</span></span>
