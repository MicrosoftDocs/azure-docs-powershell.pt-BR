---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262835"
---
# <span data-ttu-id="9f50d-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9f50d-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="9f50d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f50d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f50d-103">Verifica a existência de um pool Spark do Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="9f50d-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9f50d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f50d-104">SYNTAX</span></span>

### <span data-ttu-id="9f50d-105">TestByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f50d-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f50d-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f50d-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f50d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f50d-107">DESCRIPTION</span></span>
<span data-ttu-id="9f50d-108">O cmdlet **Test-AzSynapseSparkPool** verifica a existência de um pool Spark do Analytics do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9f50d-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9f50d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f50d-109">EXAMPLES</span></span>

### <span data-ttu-id="9f50d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f50d-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="9f50d-111">Esse comando verifica a existência do pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9f50d-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="9f50d-112">OS</span><span class="sxs-lookup"><span data-stu-id="9f50d-112">PARAMETERS</span></span>

### <span data-ttu-id="9f50d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f50d-113">-DefaultProfile</span></span>
<span data-ttu-id="9f50d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f50d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f50d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f50d-115">-Name</span></span>
<span data-ttu-id="9f50d-116">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9f50d-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9f50d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f50d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f50d-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f50d-118">Resource group name.</span></span>

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

### <span data-ttu-id="9f50d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f50d-119">-WorkspaceName</span></span>
<span data-ttu-id="9f50d-120">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9f50d-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9f50d-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9f50d-121">-WorkspaceObject</span></span>
<span data-ttu-id="9f50d-122">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f50d-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9f50d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f50d-123">CommonParameters</span></span>
<span data-ttu-id="9f50d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f50d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f50d-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f50d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f50d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f50d-126">INPUTS</span></span>

### <span data-ttu-id="9f50d-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f50d-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9f50d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f50d-128">OUTPUTS</span></span>

### <span data-ttu-id="9f50d-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f50d-129">System.Object</span></span>
## <span data-ttu-id="9f50d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f50d-130">NOTES</span></span>

## <span data-ttu-id="9f50d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f50d-131">RELATED LINKS</span></span>
