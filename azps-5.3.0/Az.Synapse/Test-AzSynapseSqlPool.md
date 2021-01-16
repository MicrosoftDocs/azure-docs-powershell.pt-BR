---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272302"
---
# <span data-ttu-id="a6a3c-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a6a3c-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a6a3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a3c-103">Verifica a existência de um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a6a3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6a3c-104">SYNTAX</span></span>

### <span data-ttu-id="a6a3c-105">TestByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6a3c-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a3c-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a3c-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a3c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6a3c-107">DESCRIPTION</span></span>
<span data-ttu-id="a6a3c-108">O cmdlet **Test-AzSynapseSqlPool** verifica a existência de um pool do SQL Analytics do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a6a3c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6a3c-109">EXAMPLES</span></span>

### <span data-ttu-id="a6a3c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6a3c-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a6a3c-111">Esse comando verifica a existência do pool SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="a6a3c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a6a3c-112">PARAMETERS</span></span>

### <span data-ttu-id="a6a3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a3c-113">-DefaultProfile</span></span>
<span data-ttu-id="a6a3c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a3c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6a3c-115">-Name</span></span>
<span data-ttu-id="a6a3c-116">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a6a3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6a3c-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-118">Resource group name.</span></span>

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

### <span data-ttu-id="a6a3c-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="a6a3c-119">-Version</span></span>
<span data-ttu-id="a6a3c-120">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="a6a3c-121">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="a6a3c-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a6a3c-122">-WorkspaceName</span></span>
<span data-ttu-id="a6a3c-123">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a6a3c-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a6a3c-124">-WorkspaceObject</span></span>
<span data-ttu-id="a6a3c-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a6a3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a3c-126">CommonParameters</span></span>
<span data-ttu-id="a6a3c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a3c-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6a3c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a3c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6a3c-129">INPUTS</span></span>

### <span data-ttu-id="a6a3c-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6a3c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a6a3c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6a3c-131">OUTPUTS</span></span>

### <span data-ttu-id="a6a3c-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="a6a3c-132">System.Object</span></span>
## <span data-ttu-id="a6a3c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6a3c-133">NOTES</span></span>

## <span data-ttu-id="a6a3c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6a3c-134">RELATED LINKS</span></span>
