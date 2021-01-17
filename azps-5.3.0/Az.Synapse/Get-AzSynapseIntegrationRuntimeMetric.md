---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427611"
---
# <span data-ttu-id="69251-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="69251-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="69251-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69251-102">SYNOPSIS</span></span>
<span data-ttu-id="69251-103">Obtém dados métricos para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="69251-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="69251-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69251-104">SYNTAX</span></span>

### <span data-ttu-id="69251-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="69251-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69251-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69251-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69251-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69251-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69251-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69251-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69251-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69251-109">DESCRIPTION</span></span>
<span data-ttu-id="69251-110">O cmdlet **Get-AzSynapseIntegrationRuntimeMetric** obtém dados métricos sobre o tempo de execução de integração em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="69251-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="69251-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69251-111">EXAMPLES</span></span>

### <span data-ttu-id="69251-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69251-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="69251-113">Esse comando exibe dados métricos sobre o tempo de execução de integração chamado "Test-selfhost-IV" no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="69251-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="69251-114">OS</span><span class="sxs-lookup"><span data-stu-id="69251-114">PARAMETERS</span></span>

### <span data-ttu-id="69251-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69251-115">-DefaultProfile</span></span>
<span data-ttu-id="69251-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69251-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69251-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69251-117">-InputObject</span></span>
<span data-ttu-id="69251-118">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="69251-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="69251-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="69251-119">-Name</span></span>
<span data-ttu-id="69251-120">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="69251-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="69251-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69251-121">-ResourceGroupName</span></span>
<span data-ttu-id="69251-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69251-122">Resource group name.</span></span>

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

### <span data-ttu-id="69251-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69251-123">-ResourceId</span></span>
<span data-ttu-id="69251-124">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="69251-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="69251-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69251-125">-WorkspaceName</span></span>
<span data-ttu-id="69251-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="69251-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="69251-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="69251-127">-WorkspaceObject</span></span>
<span data-ttu-id="69251-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="69251-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="69251-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69251-129">CommonParameters</span></span>
<span data-ttu-id="69251-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69251-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69251-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69251-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69251-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69251-132">INPUTS</span></span>

### <span data-ttu-id="69251-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="69251-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="69251-134">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69251-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="69251-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69251-135">OUTPUTS</span></span>

### <span data-ttu-id="69251-136">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="69251-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="69251-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69251-137">NOTES</span></span>

## <span data-ttu-id="69251-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69251-138">RELATED LINKS</span></span>
