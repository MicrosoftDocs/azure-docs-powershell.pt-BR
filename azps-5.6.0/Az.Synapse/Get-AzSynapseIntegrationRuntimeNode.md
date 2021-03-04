---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890913"
---
# <span data-ttu-id="59111-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="59111-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="59111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59111-102">SYNOPSIS</span></span>
<span data-ttu-id="59111-103">Obtém informações de nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="59111-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="59111-104">SYNTAX</span></span>

### <span data-ttu-id="59111-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="59111-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59111-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59111-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59111-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59111-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59111-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59111-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59111-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="59111-109">DESCRIPTION</span></span>
<span data-ttu-id="59111-110">O cmdlet **Get-AzSynapseIntegrationRuntimeNode** obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="59111-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59111-111">EXAMPLES</span></span>

### <span data-ttu-id="59111-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59111-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="59111-113">O cmdlet obtém informações do nó chamado "Node_1" no tempo de execução de integração auto-hospedado 'test-selfhost-ir' no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="59111-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="59111-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="59111-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="59111-115">O cmdlet obtém informações do nó chamado 'Node_1' no tempo de execução de integração auto-hospedado 'test-selfhost-ir' no espaço de trabalho 'test-df-eu2', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="59111-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="59111-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="59111-116">PARAMETERS</span></span>

### <span data-ttu-id="59111-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59111-117">-DefaultProfile</span></span>
<span data-ttu-id="59111-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59111-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59111-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59111-119">-InputObject</span></span>
<span data-ttu-id="59111-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59111-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="59111-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="59111-122">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59111-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="59111-123">-IpAddress</span></span>
<span data-ttu-id="59111-124">O endereço IP do nó tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="59111-125">-Name</span><span class="sxs-lookup"><span data-stu-id="59111-125">-Name</span></span>
<span data-ttu-id="59111-126">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="59111-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="59111-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59111-127">-ResourceGroupName</span></span>
<span data-ttu-id="59111-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59111-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59111-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59111-129">-ResourceId</span></span>
<span data-ttu-id="59111-130">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="59111-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59111-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59111-131">-WorkspaceName</span></span>
<span data-ttu-id="59111-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="59111-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59111-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59111-133">-WorkspaceObject</span></span>
<span data-ttu-id="59111-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="59111-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59111-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59111-135">CommonParameters</span></span>
<span data-ttu-id="59111-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59111-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59111-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59111-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59111-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59111-138">INPUTS</span></span>

### <span data-ttu-id="59111-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="59111-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="59111-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="59111-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="59111-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="59111-141">OUTPUTS</span></span>

### <span data-ttu-id="59111-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="59111-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="59111-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="59111-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="59111-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="59111-144">NOTES</span></span>

## <span data-ttu-id="59111-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59111-145">RELATED LINKS</span></span>
