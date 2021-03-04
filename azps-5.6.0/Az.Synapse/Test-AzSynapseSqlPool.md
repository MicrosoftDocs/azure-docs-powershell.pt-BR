---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d932a875957f1649976966a9f2e115e93dfea351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893056"
---
# <span data-ttu-id="2c4f9-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2c4f9-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="2c4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4f9-103">Verifica a existência de um pool do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2c4f9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c4f9-104">SYNTAX</span></span>

### <span data-ttu-id="2c4f9-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c4f9-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c4f9-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c4f9-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c4f9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c4f9-107">DESCRIPTION</span></span>
<span data-ttu-id="2c4f9-108">O cmdlet **Test-AzSynapseSqlPool** verifica a existência de um pool de SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2c4f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-109">EXAMPLES</span></span>

### <span data-ttu-id="2c4f9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c4f9-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2c4f9-111">Este comando verifica a existência do pool de SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="2c4f9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-112">PARAMETERS</span></span>

### <span data-ttu-id="2c4f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4f9-113">-DefaultProfile</span></span>
<span data-ttu-id="2c4f9-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c4f9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2c4f9-115">-Name</span></span>
<span data-ttu-id="2c4f9-116">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c4f9-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-118">Resource group name.</span></span>

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

### <span data-ttu-id="2c4f9-119">-Version</span><span class="sxs-lookup"><span data-stu-id="2c4f9-119">-Version</span></span>
<span data-ttu-id="2c4f9-120">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="2c4f9-121">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4f9-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c4f9-122">-WorkspaceName</span></span>
<span data-ttu-id="2c4f9-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2c4f9-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2c4f9-124">-WorkspaceObject</span></span>
<span data-ttu-id="2c4f9-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2c4f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4f9-126">CommonParameters</span></span>
<span data-ttu-id="2c4f9-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4f9-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c4f9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4f9-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-129">INPUTS</span></span>

### <span data-ttu-id="2c4f9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c4f9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2c4f9-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-131">OUTPUTS</span></span>

### <span data-ttu-id="2c4f9-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="2c4f9-132">System.Object</span></span>
## <span data-ttu-id="2c4f9-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c4f9-133">NOTES</span></span>

## <span data-ttu-id="2c4f9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-134">RELATED LINKS</span></span>
