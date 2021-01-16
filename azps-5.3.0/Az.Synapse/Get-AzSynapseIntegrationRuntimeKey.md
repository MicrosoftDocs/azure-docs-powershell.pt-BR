---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272446"
---
# <span data-ttu-id="a576a-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a576a-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="a576a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a576a-102">SYNOPSIS</span></span>
<span data-ttu-id="a576a-103">Obtém chaves para um tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="a576a-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="a576a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a576a-104">SYNTAX</span></span>

### <span data-ttu-id="a576a-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a576a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a576a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a576a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a576a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a576a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a576a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a576a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a576a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a576a-109">DESCRIPTION</span></span>
<span data-ttu-id="a576a-110">O cmdlet **Get-AzSynapseIntegrationRuntimeKey** Obtém chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a576a-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="a576a-111">As chaves são usadas para registrar um nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a576a-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="a576a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a576a-112">EXAMPLES</span></span>

### <span data-ttu-id="a576a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a576a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="a576a-114">O cmdlet recupera chaves para um tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="a576a-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a576a-115">OS</span><span class="sxs-lookup"><span data-stu-id="a576a-115">PARAMETERS</span></span>

### <span data-ttu-id="a576a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a576a-116">-DefaultProfile</span></span>
<span data-ttu-id="a576a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a576a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a576a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a576a-118">-InputObject</span></span>
<span data-ttu-id="a576a-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a576a-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="a576a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a576a-120">-Name</span></span>
<span data-ttu-id="a576a-121">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="a576a-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="a576a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a576a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a576a-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a576a-123">Resource group name.</span></span>

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

### <span data-ttu-id="a576a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a576a-124">-ResourceId</span></span>
<span data-ttu-id="a576a-125">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a576a-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a576a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a576a-126">-WorkspaceName</span></span>
<span data-ttu-id="a576a-127">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a576a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a576a-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a576a-128">-WorkspaceObject</span></span>
<span data-ttu-id="a576a-129">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a576a-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a576a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a576a-130">CommonParameters</span></span>
<span data-ttu-id="a576a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a576a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a576a-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a576a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a576a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a576a-133">INPUTS</span></span>

### <span data-ttu-id="a576a-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a576a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a576a-135">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a576a-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a576a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a576a-136">OUTPUTS</span></span>

### <span data-ttu-id="a576a-137">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="a576a-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="a576a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a576a-138">NOTES</span></span>

## <span data-ttu-id="a576a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a576a-139">RELATED LINKS</span></span>
