---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947464"
---
# <span data-ttu-id="ae828-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ae828-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="ae828-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae828-102">SYNOPSIS</span></span>
<span data-ttu-id="ae828-103">Verifica a existência de um pool Spark do Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae828-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ae828-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae828-104">SYNTAX</span></span>

### <span data-ttu-id="ae828-105">TestByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae828-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae828-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae828-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae828-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae828-107">DESCRIPTION</span></span>
<span data-ttu-id="ae828-108">O cmdlet **Test-AzSynapseSparkPool** verifica a existência de um pool Spark do Analytics do Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae828-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ae828-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae828-109">EXAMPLES</span></span>

### <span data-ttu-id="ae828-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae828-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="ae828-111">Esse comando verifica a existência do pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="ae828-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="ae828-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae828-112">PARAMETERS</span></span>

### <span data-ttu-id="ae828-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae828-113">-DefaultProfile</span></span>
<span data-ttu-id="ae828-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae828-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae828-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae828-115">-Name</span></span>
<span data-ttu-id="ae828-116">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae828-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ae828-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae828-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae828-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae828-118">Resource group name.</span></span>

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

### <span data-ttu-id="ae828-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ae828-119">-WorkspaceName</span></span>
<span data-ttu-id="ae828-120">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae828-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ae828-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="ae828-121">-WorkspaceObject</span></span>
<span data-ttu-id="ae828-122">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae828-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ae828-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae828-123">CommonParameters</span></span>
<span data-ttu-id="ae828-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae828-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae828-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae828-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae828-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae828-126">INPUTS</span></span>

### <span data-ttu-id="ae828-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae828-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ae828-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae828-128">OUTPUTS</span></span>

### <span data-ttu-id="ae828-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="ae828-129">System.Object</span></span>
## <span data-ttu-id="ae828-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae828-130">NOTES</span></span>

## <span data-ttu-id="ae828-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae828-131">RELATED LINKS</span></span>
