---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115160"
---
# <span data-ttu-id="54755-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="54755-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="54755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54755-102">SYNOPSIS</span></span>
<span data-ttu-id="54755-103">Sincroniza as credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="54755-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="54755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54755-104">SYNTAX</span></span>

### <span data-ttu-id="54755-105">StopByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="54755-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54755-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54755-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54755-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54755-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54755-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54755-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54755-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54755-109">DESCRIPTION</span></span>
<span data-ttu-id="54755-110">O cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** sincroniza as credenciais locais entre nós do tempo de execução de integração, o que obriga as credenciais a serem idênticas em todos os nós.</span><span class="sxs-lookup"><span data-stu-id="54755-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="54755-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54755-111">EXAMPLES</span></span>

### <span data-ttu-id="54755-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54755-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="54755-113">Sincroniza as credenciais entre nós do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="54755-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="54755-114">OS</span><span class="sxs-lookup"><span data-stu-id="54755-114">PARAMETERS</span></span>

### <span data-ttu-id="54755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54755-115">-DefaultProfile</span></span>
<span data-ttu-id="54755-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54755-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54755-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54755-117">-Force</span></span>
<span data-ttu-id="54755-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="54755-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="54755-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54755-119">-InputObject</span></span>
<span data-ttu-id="54755-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="54755-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="54755-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="54755-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="54755-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="54755-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="54755-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54755-123">-ResourceGroupName</span></span>
<span data-ttu-id="54755-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="54755-124">Resource group name.</span></span>

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

### <span data-ttu-id="54755-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54755-125">-ResourceId</span></span>
<span data-ttu-id="54755-126">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="54755-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="54755-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54755-127">-WorkspaceName</span></span>
<span data-ttu-id="54755-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="54755-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54755-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="54755-129">-WorkspaceObject</span></span>
<span data-ttu-id="54755-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="54755-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="54755-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54755-131">-Confirm</span></span>
<span data-ttu-id="54755-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54755-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54755-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54755-133">-WhatIf</span></span>
<span data-ttu-id="54755-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54755-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54755-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54755-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54755-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54755-136">CommonParameters</span></span>
<span data-ttu-id="54755-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54755-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54755-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54755-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54755-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54755-139">INPUTS</span></span>

### <span data-ttu-id="54755-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54755-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="54755-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="54755-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="54755-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54755-142">OUTPUTS</span></span>

### <span data-ttu-id="54755-143">System. void</span><span class="sxs-lookup"><span data-stu-id="54755-143">System.Void</span></span>

## <span data-ttu-id="54755-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54755-144">NOTES</span></span>

## <span data-ttu-id="54755-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54755-145">RELATED LINKS</span></span>
