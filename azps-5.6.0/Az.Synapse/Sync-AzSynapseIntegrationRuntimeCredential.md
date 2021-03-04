---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: d183506538bb2063a21eaf33df088ba613a2d3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893060"
---
# <span data-ttu-id="2b959-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="2b959-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="2b959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b959-102">SYNOPSIS</span></span>
<span data-ttu-id="2b959-103">Sincroniza credenciais entre nós de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2b959-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="2b959-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b959-104">SYNTAX</span></span>

### <span data-ttu-id="2b959-105">StopByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b959-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b959-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b959-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b959-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b959-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b959-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b959-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b959-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b959-109">DESCRIPTION</span></span>
<span data-ttu-id="2b959-110">O cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** sincroniza credenciais locais entre nós de tempo de execução de integração, o que força as credenciais a serem idênticas em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="2b959-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="2b959-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b959-111">EXAMPLES</span></span>

### <span data-ttu-id="2b959-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b959-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="2b959-113">Sincroniza credenciais entre nós de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2b959-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="2b959-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b959-114">PARAMETERS</span></span>

### <span data-ttu-id="2b959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b959-115">-DefaultProfile</span></span>
<span data-ttu-id="2b959-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b959-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b959-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2b959-117">-Force</span></span>
<span data-ttu-id="2b959-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2b959-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2b959-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b959-119">-InputObject</span></span>
<span data-ttu-id="2b959-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2b959-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2b959-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2b959-122">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2b959-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b959-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b959-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b959-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b959-125">-ResourceId</span></span>
<span data-ttu-id="2b959-126">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="2b959-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b959-127">-WorkspaceName</span></span>
<span data-ttu-id="2b959-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b959-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2b959-129">-WorkspaceObject</span></span>
<span data-ttu-id="2b959-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b959-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b959-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b959-131">-Confirm</span></span>
<span data-ttu-id="2b959-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b959-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b959-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b959-133">-WhatIf</span></span>
<span data-ttu-id="2b959-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b959-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b959-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b959-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b959-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b959-136">CommonParameters</span></span>
<span data-ttu-id="2b959-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b959-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b959-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b959-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b959-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b959-139">INPUTS</span></span>

### <span data-ttu-id="2b959-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b959-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2b959-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2b959-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2b959-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b959-142">OUTPUTS</span></span>

### <span data-ttu-id="2b959-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="2b959-143">System.Void</span></span>

## <span data-ttu-id="2b959-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b959-144">NOTES</span></span>

## <span data-ttu-id="2b959-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b959-145">RELATED LINKS</span></span>
