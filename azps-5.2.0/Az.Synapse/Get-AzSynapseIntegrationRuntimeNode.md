---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259244"
---
# <span data-ttu-id="44fc4-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="44fc4-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="44fc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="44fc4-103">Obtém informações sobre o nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="44fc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44fc4-104">SYNTAX</span></span>

### <span data-ttu-id="44fc4-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="44fc4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44fc4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fc4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fc4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc4-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44fc4-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44fc4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44fc4-109">DESCRIPTION</span></span>
<span data-ttu-id="44fc4-110">O cmdlet **Get-AzSynapseIntegrationRuntimeNode** Obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="44fc4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44fc4-111">EXAMPLES</span></span>

### <span data-ttu-id="44fc4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44fc4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="44fc4-113">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="44fc4-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="44fc4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44fc4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="44fc4-115">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' no espaço de trabalho ' test-DF-EU2 ', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="44fc4-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="44fc4-116">OS</span><span class="sxs-lookup"><span data-stu-id="44fc4-116">PARAMETERS</span></span>

### <span data-ttu-id="44fc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fc4-117">-DefaultProfile</span></span>
<span data-ttu-id="44fc4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44fc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fc4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44fc4-119">-InputObject</span></span>
<span data-ttu-id="44fc4-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="44fc4-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="44fc4-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="44fc4-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="44fc4-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="44fc4-123">-IpAddress</span></span>
<span data-ttu-id="44fc4-124">O endereço IP do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="44fc4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="44fc4-125">-Name</span></span>
<span data-ttu-id="44fc4-126">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="44fc4-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="44fc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="44fc4-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44fc4-128">Resource group name.</span></span>

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

### <span data-ttu-id="44fc4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fc4-129">-ResourceId</span></span>
<span data-ttu-id="44fc4-130">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="44fc4-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="44fc4-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44fc4-131">-WorkspaceName</span></span>
<span data-ttu-id="44fc4-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="44fc4-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="44fc4-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="44fc4-133">-WorkspaceObject</span></span>
<span data-ttu-id="44fc4-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="44fc4-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44fc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fc4-135">CommonParameters</span></span>
<span data-ttu-id="44fc4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fc4-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44fc4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fc4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44fc4-138">INPUTS</span></span>

### <span data-ttu-id="44fc4-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="44fc4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="44fc4-140">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="44fc4-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="44fc4-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44fc4-141">OUTPUTS</span></span>

### <span data-ttu-id="44fc4-142">Microsoft. Azure. Commands. Synapse. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="44fc4-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="44fc4-143">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="44fc4-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="44fc4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44fc4-144">NOTES</span></span>

## <span data-ttu-id="44fc4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44fc4-145">RELATED LINKS</span></span>
