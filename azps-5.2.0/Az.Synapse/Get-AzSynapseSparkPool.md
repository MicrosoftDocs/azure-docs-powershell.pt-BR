---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262550"
---
# <span data-ttu-id="fd5e3-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fd5e3-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="fd5e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5e3-103">Obtém um pool do Spark da análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="fd5e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd5e3-104">SYNTAX</span></span>

### <span data-ttu-id="fd5e3-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd5e3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd5e3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd5e3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd5e3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd5e3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd5e3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd5e3-108">DESCRIPTION</span></span>
<span data-ttu-id="fd5e3-109">O cmdlet **Get-AzSynapseSparkPool** Obtém informações sobre um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="fd5e3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd5e3-110">EXAMPLES</span></span>

### <span data-ttu-id="fd5e3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd5e3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fd5e3-112">Esse comando obtém todos os pools do Spark em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="fd5e3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd5e3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="fd5e3-114">Esse comando obtém o pool do Spark em ContosoWorkspace do espaço de trabalho com o nome ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="fd5e3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fd5e3-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="fd5e3-116">Esse comando obtém todos os pools do Spark em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="fd5e3-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fd5e3-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="fd5e3-118">Esse comando obtém o pool do Spark com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="fd5e3-119">OS</span><span class="sxs-lookup"><span data-stu-id="fd5e3-119">PARAMETERS</span></span>

### <span data-ttu-id="fd5e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5e3-120">-DefaultProfile</span></span>
<span data-ttu-id="fd5e3-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd5e3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd5e3-122">-Name</span></span>
<span data-ttu-id="fd5e3-123">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd5e3-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-125">Resource group name.</span></span>

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

### <span data-ttu-id="fd5e3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd5e3-126">-ResourceId</span></span>
<span data-ttu-id="fd5e3-127">Identificador de recurso do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="fd5e3-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd5e3-128">-WorkspaceName</span></span>
<span data-ttu-id="fd5e3-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd5e3-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fd5e3-130">-WorkspaceObject</span></span>
<span data-ttu-id="fd5e3-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd5e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5e3-132">CommonParameters</span></span>
<span data-ttu-id="fd5e3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd5e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5e3-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd5e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5e3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd5e3-135">INPUTS</span></span>

### <span data-ttu-id="fd5e3-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd5e3-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fd5e3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd5e3-137">OUTPUTS</span></span>

### <span data-ttu-id="fd5e3-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fd5e3-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="fd5e3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd5e3-139">NOTES</span></span>

## <span data-ttu-id="fd5e3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd5e3-140">RELATED LINKS</span></span>
