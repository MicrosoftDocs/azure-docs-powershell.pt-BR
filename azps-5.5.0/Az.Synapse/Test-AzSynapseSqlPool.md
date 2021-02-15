---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113901"
---
# <span data-ttu-id="cc920-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cc920-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="cc920-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc920-102">SYNOPSIS</span></span>
<span data-ttu-id="cc920-103">Verifica a existência de um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc920-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cc920-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc920-104">SYNTAX</span></span>

### <span data-ttu-id="cc920-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc920-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc920-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc920-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc920-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc920-107">DESCRIPTION</span></span>
<span data-ttu-id="cc920-108">O cmdlet **Test-AzSynapseSqlPool** verifica a existência de um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc920-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cc920-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cc920-109">EXAMPLES</span></span>

### <span data-ttu-id="cc920-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc920-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="cc920-111">Esse comando verifica a existência do pool SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="cc920-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="cc920-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc920-112">PARAMETERS</span></span>

### <span data-ttu-id="cc920-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc920-113">-DefaultProfile</span></span>
<span data-ttu-id="cc920-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc920-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc920-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc920-115">-Name</span></span>
<span data-ttu-id="cc920-116">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc920-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="cc920-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc920-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc920-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc920-118">Resource group name.</span></span>

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

### <span data-ttu-id="cc920-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="cc920-119">-Version</span></span>
<span data-ttu-id="cc920-120">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc920-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="cc920-121">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="cc920-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="cc920-122">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="cc920-122">-WorkspaceName</span></span>
<span data-ttu-id="cc920-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc920-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc920-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc920-124">-WorkspaceObject</span></span>
<span data-ttu-id="cc920-125">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc920-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc920-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc920-126">CommonParameters</span></span>
<span data-ttu-id="cc920-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc920-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc920-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc920-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc920-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="cc920-129">INPUTS</span></span>

### <span data-ttu-id="cc920-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc920-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cc920-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="cc920-131">OUTPUTS</span></span>

### <span data-ttu-id="cc920-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="cc920-132">System.Object</span></span>
## <span data-ttu-id="cc920-133">Notas</span><span class="sxs-lookup"><span data-stu-id="cc920-133">NOTES</span></span>

## <span data-ttu-id="cc920-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc920-134">RELATED LINKS</span></span>
