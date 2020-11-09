---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282337"
---
# <span data-ttu-id="f8358-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f8358-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f8358-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8358-102">SYNOPSIS</span></span>
<span data-ttu-id="f8358-103">Obtém informações sobre o nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="f8358-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8358-104">SYNTAX</span></span>

### <span data-ttu-id="f8358-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8358-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8358-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8358-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8358-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8358-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8358-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8358-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8358-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8358-109">DESCRIPTION</span></span>
<span data-ttu-id="f8358-110">O cmdlet **Get-AzSynapseIntegrationRuntimeNode** Obtém as informações detalhadas de um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="f8358-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8358-111">EXAMPLES</span></span>

### <span data-ttu-id="f8358-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8358-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="f8358-113">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f8358-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f8358-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f8358-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="f8358-115">O cmdlet obtém informações do nó chamado ' Node_1 ' no tempo de execução de integração de hospedagem interna ' test-selfhost-IV ' no espaço de trabalho ' test-DF-EU2 ', incluindo o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f8358-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="f8358-116">OS</span><span class="sxs-lookup"><span data-stu-id="f8358-116">PARAMETERS</span></span>

### <span data-ttu-id="f8358-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8358-117">-DefaultProfile</span></span>
<span data-ttu-id="f8358-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8358-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8358-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8358-119">-InputObject</span></span>
<span data-ttu-id="f8358-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="f8358-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f8358-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f8358-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f8358-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f8358-123">-IpAddress</span></span>
<span data-ttu-id="f8358-124">O endereço IP do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="f8358-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8358-125">-Name</span></span>
<span data-ttu-id="f8358-126">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f8358-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="f8358-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8358-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8358-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f8358-128">Resource group name.</span></span>

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

### <span data-ttu-id="f8358-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8358-129">-ResourceId</span></span>
<span data-ttu-id="f8358-130">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="f8358-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f8358-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8358-131">-WorkspaceName</span></span>
<span data-ttu-id="f8358-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="f8358-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f8358-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f8358-133">-WorkspaceObject</span></span>
<span data-ttu-id="f8358-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8358-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f8358-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8358-135">CommonParameters</span></span>
<span data-ttu-id="f8358-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8358-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8358-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8358-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8358-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8358-138">INPUTS</span></span>

### <span data-ttu-id="f8358-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f8358-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f8358-140">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f8358-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f8358-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8358-141">OUTPUTS</span></span>

### <span data-ttu-id="f8358-142">Microsoft. Azure. Commands. Synapse. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f8358-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="f8358-143">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f8358-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f8358-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8358-144">NOTES</span></span>

## <span data-ttu-id="f8358-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8358-145">RELATED LINKS</span></span>
