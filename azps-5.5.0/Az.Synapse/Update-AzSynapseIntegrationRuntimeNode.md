---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112380"
---
# <span data-ttu-id="8cf54-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8cf54-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="8cf54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cf54-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf54-103">Atualiza o nó de tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="8cf54-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="8cf54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cf54-104">SYNTAX</span></span>

### <span data-ttu-id="8cf54-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8cf54-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf54-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf54-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf54-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf54-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf54-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cf54-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cf54-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cf54-109">DESCRIPTION</span></span>
<span data-ttu-id="8cf54-110">O cmdlet **Update-AzSynapseIntegrationRuntimeNode** atualiza as propriedades do nó de tempo de execução de integração auto-hospedado em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8cf54-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="8cf54-111">Atualmente, só há suporte para a atualização de 'ConcurrentJobsLimit'.</span><span class="sxs-lookup"><span data-stu-id="8cf54-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="8cf54-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8cf54-112">EXAMPLES</span></span>

### <span data-ttu-id="8cf54-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cf54-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="8cf54-114">O cmdlet atualiza 'ConcurrentJobsLimit' para 3 para nó 'Node_1' em tempo de execução de integração hospedada auto-hospedado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="8cf54-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8cf54-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cf54-115">PARAMETERS</span></span>

### <span data-ttu-id="8cf54-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="8cf54-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="8cf54-117">O número de trabalhos simultâneos permitidos para execução no nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8cf54-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="8cf54-118">Valores entre 1 e maxConcurrentJobs são permitidos.</span><span class="sxs-lookup"><span data-stu-id="8cf54-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf54-119">-DefaultProfile</span></span>
<span data-ttu-id="8cf54-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf54-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf54-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf54-121">-InputObject</span></span>
<span data-ttu-id="8cf54-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8cf54-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8cf54-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8cf54-124">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="8cf54-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cf54-125">-Name</span></span>
<span data-ttu-id="8cf54-126">O nome do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8cf54-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf54-127">-ResourceGroupName</span></span>
<span data-ttu-id="8cf54-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cf54-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf54-129">-ResourceId</span></span>
<span data-ttu-id="8cf54-130">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="8cf54-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8cf54-131">-WorkspaceName</span></span>
<span data-ttu-id="8cf54-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cf54-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8cf54-133">-WorkspaceObject</span></span>
<span data-ttu-id="8cf54-134">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cf54-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf54-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8cf54-135">-Confirm</span></span>
<span data-ttu-id="8cf54-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf54-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf54-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf54-137">-WhatIf</span></span>
<span data-ttu-id="8cf54-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8cf54-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf54-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cf54-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf54-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf54-140">CommonParameters</span></span>
<span data-ttu-id="8cf54-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf54-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf54-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cf54-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf54-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="8cf54-143">INPUTS</span></span>

### <span data-ttu-id="8cf54-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cf54-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8cf54-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8cf54-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8cf54-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="8cf54-146">OUTPUTS</span></span>

### <span data-ttu-id="8cf54-147">Microsoft.Azure.Commands.Synapse.Models.PSHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="8cf54-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="8cf54-148">Notas</span><span class="sxs-lookup"><span data-stu-id="8cf54-148">NOTES</span></span>

## <span data-ttu-id="8cf54-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cf54-149">RELATED LINKS</span></span>
