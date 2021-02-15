---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116305"
---
# <span data-ttu-id="5c9b6-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="5c9b6-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="5c9b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9b6-103">Remover um nó com o nome determinado em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="5c9b6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c9b6-104">SYNTAX</span></span>

### <span data-ttu-id="5c9b6-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c9b6-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c9b6-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9b6-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c9b6-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9b6-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c9b6-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c9b6-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c9b6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c9b6-109">DESCRIPTION</span></span>
<span data-ttu-id="5c9b6-110">O cmdlet **Remove-AzSynapseIntegrationRuntimeNode** remove um nó em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="5c9b6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c9b6-111">EXAMPLES</span></span>

### <span data-ttu-id="5c9b6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c9b6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="5c9b6-113">Remover um nó com o nome determinado em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="5c9b6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c9b6-114">PARAMETERS</span></span>

### <span data-ttu-id="5c9b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9b6-115">-DefaultProfile</span></span>
<span data-ttu-id="5c9b6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9b6-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="5c9b6-117">-Force</span></span>
<span data-ttu-id="5c9b6-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5c9b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c9b6-119">-InputObject</span></span>
<span data-ttu-id="5c9b6-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="5c9b6-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5c9b6-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5c9b6-122">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="5c9b6-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="5c9b6-123">-NodeName</span></span>
<span data-ttu-id="5c9b6-124">O nome do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="5c9b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c9b6-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-126">Resource group name.</span></span>

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

### <span data-ttu-id="5c9b6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c9b6-127">-ResourceId</span></span>
<span data-ttu-id="5c9b6-128">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="5c9b6-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5c9b6-129">-WorkspaceName</span></span>
<span data-ttu-id="5c9b6-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5c9b6-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5c9b6-131">-WorkspaceObject</span></span>
<span data-ttu-id="5c9b6-132">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c9b6-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5c9b6-133">-Confirm</span></span>
<span data-ttu-id="5c9b6-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c9b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c9b6-135">-WhatIf</span></span>
<span data-ttu-id="5c9b6-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c9b6-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c9b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9b6-138">CommonParameters</span></span>
<span data-ttu-id="5c9b6-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9b6-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c9b6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9b6-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="5c9b6-141">INPUTS</span></span>

### <span data-ttu-id="5c9b6-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c9b6-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5c9b6-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5c9b6-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="5c9b6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5c9b6-144">System.String</span></span>

## <span data-ttu-id="5c9b6-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="5c9b6-145">OUTPUTS</span></span>

### <span data-ttu-id="5c9b6-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="5c9b6-146">System.Void</span></span>

## <span data-ttu-id="5c9b6-147">Notas</span><span class="sxs-lookup"><span data-stu-id="5c9b6-147">NOTES</span></span>

## <span data-ttu-id="5c9b6-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c9b6-148">RELATED LINKS</span></span>
