---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: cb7abd3c54d263ae9516344237588ecf9a1297ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893058"
---
# <span data-ttu-id="4b83f-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4b83f-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="4b83f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b83f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b83f-103">Verifica a existência de um pool de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="4b83f-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="4b83f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4b83f-104">SYNTAX</span></span>

### <span data-ttu-id="4b83f-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b83f-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b83f-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b83f-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b83f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4b83f-107">DESCRIPTION</span></span>
<span data-ttu-id="4b83f-108">O cmdlet **Test-AzSynapseSparkPool** verifica a existência de um pool de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="4b83f-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="4b83f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b83f-109">EXAMPLES</span></span>

### <span data-ttu-id="4b83f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b83f-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="4b83f-111">Este comando verifica a existência do pool de Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="4b83f-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="4b83f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4b83f-112">PARAMETERS</span></span>

### <span data-ttu-id="4b83f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b83f-113">-DefaultProfile</span></span>
<span data-ttu-id="4b83f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b83f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b83f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4b83f-115">-Name</span></span>
<span data-ttu-id="4b83f-116">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="4b83f-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4b83f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b83f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b83f-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b83f-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b83f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4b83f-119">-WorkspaceName</span></span>
<span data-ttu-id="4b83f-120">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4b83f-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b83f-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4b83f-121">-WorkspaceObject</span></span>
<span data-ttu-id="4b83f-122">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4b83f-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b83f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b83f-123">CommonParameters</span></span>
<span data-ttu-id="4b83f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b83f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b83f-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b83f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b83f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b83f-126">INPUTS</span></span>

### <span data-ttu-id="4b83f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b83f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4b83f-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4b83f-128">OUTPUTS</span></span>

### <span data-ttu-id="4b83f-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="4b83f-129">System.Object</span></span>
## <span data-ttu-id="4b83f-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="4b83f-130">NOTES</span></span>

## <span data-ttu-id="4b83f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b83f-131">RELATED LINKS</span></span>
