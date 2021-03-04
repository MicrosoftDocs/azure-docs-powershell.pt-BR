---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893059"
---
# <span data-ttu-id="f73cb-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f73cb-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="f73cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f73cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f73cb-103">Verifica a existência de um banco de dados do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="f73cb-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f73cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f73cb-104">SYNTAX</span></span>

### <span data-ttu-id="f73cb-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f73cb-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73cb-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f73cb-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f73cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f73cb-107">DESCRIPTION</span></span>
<span data-ttu-id="f73cb-108">O cmdlet **Test-AzSynapseSqlDatabase** verifica a existência de um banco de dados do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="f73cb-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f73cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f73cb-109">EXAMPLES</span></span>

### <span data-ttu-id="f73cb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f73cb-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="f73cb-111">Este comando verifica a existência do banco de dados SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="f73cb-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="f73cb-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f73cb-112">PARAMETERS</span></span>

### <span data-ttu-id="f73cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73cb-113">-DefaultProfile</span></span>
<span data-ttu-id="f73cb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f73cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f73cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f73cb-115">-Name</span></span>
<span data-ttu-id="f73cb-116">Nome do banco de dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f73cb-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="f73cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="f73cb-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f73cb-118">Resource group name.</span></span>

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

### <span data-ttu-id="f73cb-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f73cb-119">-WorkspaceName</span></span>
<span data-ttu-id="f73cb-120">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f73cb-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f73cb-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f73cb-121">-WorkspaceObject</span></span>
<span data-ttu-id="f73cb-122">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f73cb-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f73cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73cb-123">CommonParameters</span></span>
<span data-ttu-id="f73cb-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73cb-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f73cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73cb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f73cb-126">INPUTS</span></span>

### <span data-ttu-id="f73cb-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f73cb-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f73cb-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f73cb-128">OUTPUTS</span></span>

### <span data-ttu-id="f73cb-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f73cb-129">System.Boolean</span></span>

## <span data-ttu-id="f73cb-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="f73cb-130">NOTES</span></span>

## <span data-ttu-id="f73cb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f73cb-131">RELATED LINKS</span></span>
