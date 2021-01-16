---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260176"
---
# <span data-ttu-id="fdabb-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fdabb-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="fdabb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdabb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdabb-103">Verifica a existência de um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fdabb-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fdabb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdabb-104">SYNTAX</span></span>

### <span data-ttu-id="fdabb-105">TestByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdabb-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdabb-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdabb-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdabb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdabb-107">DESCRIPTION</span></span>
<span data-ttu-id="fdabb-108">O cmdlet **Test-AzSynapseSqlPool** verifica a existência de um pool do SQL Analytics do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fdabb-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fdabb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdabb-109">EXAMPLES</span></span>

### <span data-ttu-id="fdabb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdabb-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fdabb-111">Esse comando verifica a existência do pool SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="fdabb-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="fdabb-112">OS</span><span class="sxs-lookup"><span data-stu-id="fdabb-112">PARAMETERS</span></span>

### <span data-ttu-id="fdabb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdabb-113">-DefaultProfile</span></span>
<span data-ttu-id="fdabb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdabb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdabb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdabb-115">-Name</span></span>
<span data-ttu-id="fdabb-116">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fdabb-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fdabb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdabb-117">-ResourceGroupName</span></span>
<span data-ttu-id="fdabb-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdabb-118">Resource group name.</span></span>

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

### <span data-ttu-id="fdabb-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="fdabb-119">-Version</span></span>
<span data-ttu-id="fdabb-120">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fdabb-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="fdabb-121">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="fdabb-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="fdabb-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fdabb-122">-WorkspaceName</span></span>
<span data-ttu-id="fdabb-123">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fdabb-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fdabb-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fdabb-124">-WorkspaceObject</span></span>
<span data-ttu-id="fdabb-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdabb-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fdabb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdabb-126">CommonParameters</span></span>
<span data-ttu-id="fdabb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdabb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdabb-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdabb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdabb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdabb-129">INPUTS</span></span>

### <span data-ttu-id="fdabb-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fdabb-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fdabb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdabb-131">OUTPUTS</span></span>

### <span data-ttu-id="fdabb-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="fdabb-132">System.Object</span></span>
## <span data-ttu-id="fdabb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdabb-133">NOTES</span></span>

## <span data-ttu-id="fdabb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdabb-134">RELATED LINKS</span></span>
