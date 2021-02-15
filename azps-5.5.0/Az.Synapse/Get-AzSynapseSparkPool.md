---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113918"
---
# <span data-ttu-id="5adb6-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5adb6-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="5adb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5adb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5adb6-103">Obtém um pool de miniapse analytics.</span><span class="sxs-lookup"><span data-stu-id="5adb6-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5adb6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5adb6-104">SYNTAX</span></span>

### <span data-ttu-id="5adb6-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5adb6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5adb6-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5adb6-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5adb6-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5adb6-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5adb6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5adb6-108">DESCRIPTION</span></span>
<span data-ttu-id="5adb6-109">O cmdlet **Get-AzSynapseSparkPool** obtém informações sobre um pool de sparks de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="5adb6-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5adb6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5adb6-110">EXAMPLES</span></span>

### <span data-ttu-id="5adb6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5adb6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5adb6-112">Esse comando obtém todos os pools de Spark sob um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5adb6-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="5adb6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5adb6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="5adb6-114">Esse comando obtém o pool de Spark no espaço de trabalho ContosoWorkspace com o nome ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="5adb6-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="5adb6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5adb6-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="5adb6-116">Esse comando obtém todos os pools de Spark sob um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="5adb6-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="5adb6-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5adb6-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="5adb6-118">Esse comando obtém o pool de Spark com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="5adb6-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="5adb6-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5adb6-119">PARAMETERS</span></span>

### <span data-ttu-id="5adb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5adb6-120">-DefaultProfile</span></span>
<span data-ttu-id="5adb6-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5adb6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5adb6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5adb6-122">-Name</span></span>
<span data-ttu-id="5adb6-123">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="5adb6-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5adb6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5adb6-124">-ResourceGroupName</span></span>
<span data-ttu-id="5adb6-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5adb6-125">Resource group name.</span></span>

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

### <span data-ttu-id="5adb6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5adb6-126">-ResourceId</span></span>
<span data-ttu-id="5adb6-127">Identificador de recurso do pool de Miniapse Spark.</span><span class="sxs-lookup"><span data-stu-id="5adb6-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5adb6-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5adb6-128">-WorkspaceName</span></span>
<span data-ttu-id="5adb6-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5adb6-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5adb6-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5adb6-130">-WorkspaceObject</span></span>
<span data-ttu-id="5adb6-131">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5adb6-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5adb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adb6-132">CommonParameters</span></span>
<span data-ttu-id="5adb6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5adb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adb6-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5adb6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adb6-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="5adb6-135">INPUTS</span></span>

### <span data-ttu-id="5adb6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5adb6-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5adb6-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="5adb6-137">OUTPUTS</span></span>

### <span data-ttu-id="5adb6-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5adb6-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="5adb6-139">Notas</span><span class="sxs-lookup"><span data-stu-id="5adb6-139">NOTES</span></span>

## <span data-ttu-id="5adb6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5adb6-140">RELATED LINKS</span></span>
