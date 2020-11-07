---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955279"
---
# <span data-ttu-id="71982-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="71982-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="71982-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71982-102">SYNOPSIS</span></span>
<span data-ttu-id="71982-103">Atualiza o nó do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="71982-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="71982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71982-104">SYNTAX</span></span>

### <span data-ttu-id="71982-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71982-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71982-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71982-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71982-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71982-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71982-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71982-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71982-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71982-109">DESCRIPTION</span></span>
<span data-ttu-id="71982-110">O cmdlet **Update-AzSynapseIntegrationRuntimeNode** atualiza propriedades do nó de tempo de execução de integração de hospedagem interna em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="71982-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="71982-111">Atualmente só dá suporte à atualização de ' ConcurrentJobsLimit '.</span><span class="sxs-lookup"><span data-stu-id="71982-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="71982-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71982-112">EXAMPLES</span></span>

### <span data-ttu-id="71982-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71982-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="71982-114">O cmdlet atualiza ' ConcurrentJobsLimit ' para 3 para o nó ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="71982-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="71982-115">OS</span><span class="sxs-lookup"><span data-stu-id="71982-115">PARAMETERS</span></span>

### <span data-ttu-id="71982-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="71982-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="71982-117">O número de trabalhos simultâneos permitidos para executar no nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="71982-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="71982-118">Valores entre 1 e maxConcurrentJobs são permitidos.</span><span class="sxs-lookup"><span data-stu-id="71982-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="71982-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71982-119">-DefaultProfile</span></span>
<span data-ttu-id="71982-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71982-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71982-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71982-121">-InputObject</span></span>
<span data-ttu-id="71982-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="71982-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="71982-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="71982-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="71982-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="71982-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="71982-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="71982-125">-Name</span></span>
<span data-ttu-id="71982-126">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="71982-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="71982-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71982-127">-ResourceGroupName</span></span>
<span data-ttu-id="71982-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71982-128">Resource group name.</span></span>

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

### <span data-ttu-id="71982-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71982-129">-ResourceId</span></span>
<span data-ttu-id="71982-130">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="71982-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="71982-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71982-131">-WorkspaceName</span></span>
<span data-ttu-id="71982-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="71982-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="71982-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="71982-133">-WorkspaceObject</span></span>
<span data-ttu-id="71982-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="71982-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="71982-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71982-135">-Confirm</span></span>
<span data-ttu-id="71982-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71982-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71982-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71982-137">-WhatIf</span></span>
<span data-ttu-id="71982-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71982-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71982-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71982-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71982-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71982-140">CommonParameters</span></span>
<span data-ttu-id="71982-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71982-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71982-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71982-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71982-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71982-143">INPUTS</span></span>

### <span data-ttu-id="71982-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="71982-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="71982-145">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71982-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="71982-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71982-146">OUTPUTS</span></span>

### <span data-ttu-id="71982-147">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="71982-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="71982-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71982-148">NOTES</span></span>

## <span data-ttu-id="71982-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71982-149">RELATED LINKS</span></span>
