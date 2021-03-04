---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: d00e4c137e3b46e7721534264c9273cde5a9ad3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887840"
---
# <span data-ttu-id="3afd3-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3afd3-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="3afd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3afd3-102">SYNOPSIS</span></span>
<span data-ttu-id="3afd3-103">Obtém chaves para um tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="3afd3-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="3afd3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3afd3-104">SYNTAX</span></span>

### <span data-ttu-id="3afd3-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3afd3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3afd3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3afd3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3afd3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3afd3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3afd3-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3afd3-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3afd3-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3afd3-109">DESCRIPTION</span></span>
<span data-ttu-id="3afd3-110">O cmdlet **Get-AzSynapseIntegrationRuntimeKey** obtém chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3afd3-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="3afd3-111">As chaves são usadas para registrar um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3afd3-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="3afd3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3afd3-112">EXAMPLES</span></span>

### <span data-ttu-id="3afd3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3afd3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="3afd3-114">O cmdlet recupera chaves para um tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="3afd3-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3afd3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3afd3-115">PARAMETERS</span></span>

### <span data-ttu-id="3afd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afd3-116">-DefaultProfile</span></span>
<span data-ttu-id="3afd3-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3afd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3afd3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3afd3-118">-InputObject</span></span>
<span data-ttu-id="3afd3-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3afd3-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="3afd3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3afd3-120">-Name</span></span>
<span data-ttu-id="3afd3-121">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3afd3-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3afd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="3afd3-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3afd3-123">Resource group name.</span></span>

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

### <span data-ttu-id="3afd3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3afd3-124">-ResourceId</span></span>
<span data-ttu-id="3afd3-125">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="3afd3-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3afd3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3afd3-126">-WorkspaceName</span></span>
<span data-ttu-id="3afd3-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3afd3-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3afd3-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3afd3-128">-WorkspaceObject</span></span>
<span data-ttu-id="3afd3-129">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3afd3-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3afd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afd3-130">CommonParameters</span></span>
<span data-ttu-id="3afd3-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afd3-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3afd3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afd3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3afd3-133">INPUTS</span></span>

### <span data-ttu-id="3afd3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3afd3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3afd3-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3afd3-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3afd3-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3afd3-136">OUTPUTS</span></span>

### <span data-ttu-id="3afd3-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="3afd3-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="3afd3-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3afd3-138">NOTES</span></span>

## <span data-ttu-id="3afd3-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3afd3-139">RELATED LINKS</span></span>
