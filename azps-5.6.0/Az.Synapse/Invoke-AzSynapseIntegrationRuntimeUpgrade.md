---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: ad5b23e29eb2d13fcad6aaf2659940dace83f4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889391"
---
# <span data-ttu-id="11d62-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="11d62-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="11d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d62-102">SYNOPSIS</span></span>
<span data-ttu-id="11d62-103">Atualiza o tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="11d62-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="11d62-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11d62-104">SYNTAX</span></span>

### <span data-ttu-id="11d62-105">InvokeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11d62-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d62-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d62-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d62-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d62-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d62-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d62-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d62-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11d62-109">DESCRIPTION</span></span>
<span data-ttu-id="11d62-110">O cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** atualiza o tempo de execução de integração auto-hospedado se a nova versão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="11d62-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="11d62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11d62-111">EXAMPLES</span></span>

### <span data-ttu-id="11d62-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11d62-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="11d62-113">O cmdlet atualiza o tempo de execução de integração auto-hospedado chamado "test-selfhost-ir" no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="11d62-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="11d62-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11d62-114">PARAMETERS</span></span>

### <span data-ttu-id="11d62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d62-115">-DefaultProfile</span></span>
<span data-ttu-id="11d62-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11d62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d62-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d62-117">-InputObject</span></span>
<span data-ttu-id="11d62-118">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="11d62-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-119">-Name</span><span class="sxs-lookup"><span data-stu-id="11d62-119">-Name</span></span>
<span data-ttu-id="11d62-120">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="11d62-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d62-121">-ResourceGroupName</span></span>
<span data-ttu-id="11d62-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11d62-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d62-123">-ResourceId</span></span>
<span data-ttu-id="11d62-124">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="11d62-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11d62-125">-WorkspaceName</span></span>
<span data-ttu-id="11d62-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="11d62-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11d62-127">-WorkspaceObject</span></span>
<span data-ttu-id="11d62-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="11d62-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11d62-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11d62-129">-Confirm</span></span>
<span data-ttu-id="11d62-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d62-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d62-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d62-131">-WhatIf</span></span>
<span data-ttu-id="11d62-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11d62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d62-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11d62-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d62-134">CommonParameters</span></span>
<span data-ttu-id="11d62-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d62-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d62-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d62-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11d62-137">INPUTS</span></span>

### <span data-ttu-id="11d62-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11d62-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="11d62-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="11d62-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="11d62-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11d62-140">OUTPUTS</span></span>

### <span data-ttu-id="11d62-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="11d62-141">System.Void</span></span>

## <span data-ttu-id="11d62-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="11d62-142">NOTES</span></span>

## <span data-ttu-id="11d62-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11d62-143">RELATED LINKS</span></span>
