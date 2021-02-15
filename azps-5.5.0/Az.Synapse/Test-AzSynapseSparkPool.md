---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113903"
---
# <span data-ttu-id="60071-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="60071-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="60071-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60071-102">SYNOPSIS</span></span>
<span data-ttu-id="60071-103">Verifica a existência de um pool de Miniapsis de Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="60071-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="60071-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60071-104">SYNTAX</span></span>

### <span data-ttu-id="60071-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="60071-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60071-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60071-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60071-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="60071-107">DESCRIPTION</span></span>
<span data-ttu-id="60071-108">O cmdlet **Test-AzSynapseSparkPool** verifica a existência de um pool de miniaptas de análise synapse.</span><span class="sxs-lookup"><span data-stu-id="60071-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="60071-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60071-109">EXAMPLES</span></span>

### <span data-ttu-id="60071-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60071-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="60071-111">Esse comando verifica a existência do pool de Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="60071-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="60071-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60071-112">PARAMETERS</span></span>

### <span data-ttu-id="60071-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60071-113">-DefaultProfile</span></span>
<span data-ttu-id="60071-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60071-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60071-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="60071-115">-Name</span></span>
<span data-ttu-id="60071-116">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="60071-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="60071-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60071-117">-ResourceGroupName</span></span>
<span data-ttu-id="60071-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60071-118">Resource group name.</span></span>

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

### <span data-ttu-id="60071-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="60071-119">-WorkspaceName</span></span>
<span data-ttu-id="60071-120">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="60071-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="60071-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60071-121">-WorkspaceObject</span></span>
<span data-ttu-id="60071-122">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="60071-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="60071-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60071-123">CommonParameters</span></span>
<span data-ttu-id="60071-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60071-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60071-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60071-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60071-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="60071-126">INPUTS</span></span>

### <span data-ttu-id="60071-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="60071-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="60071-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="60071-128">OUTPUTS</span></span>

### <span data-ttu-id="60071-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="60071-129">System.Object</span></span>
## <span data-ttu-id="60071-130">Notas</span><span class="sxs-lookup"><span data-stu-id="60071-130">NOTES</span></span>

## <span data-ttu-id="60071-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60071-131">RELATED LINKS</span></span>
