---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429595"
---
# <span data-ttu-id="d48a8-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d48a8-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="d48a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d48a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d48a8-103">Verifica a existência de um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d48a8-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d48a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d48a8-104">SYNTAX</span></span>

### <span data-ttu-id="d48a8-105">TestByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d48a8-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d48a8-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d48a8-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d48a8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d48a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d48a8-108">O cmdlet **Test-AzSynapseSqlDatabase** verifica a existência de um banco de dados SQL analítico do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d48a8-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="d48a8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d48a8-109">EXAMPLES</span></span>

### <span data-ttu-id="d48a8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d48a8-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="d48a8-111">Esse comando verifica a existência do banco de dados SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="d48a8-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="d48a8-112">OS</span><span class="sxs-lookup"><span data-stu-id="d48a8-112">PARAMETERS</span></span>

### <span data-ttu-id="d48a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48a8-113">-DefaultProfile</span></span>
<span data-ttu-id="d48a8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d48a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d48a8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d48a8-115">-Name</span></span>
<span data-ttu-id="d48a8-116">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d48a8-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="d48a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d48a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="d48a8-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d48a8-118">Resource group name.</span></span>

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

### <span data-ttu-id="d48a8-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d48a8-119">-WorkspaceName</span></span>
<span data-ttu-id="d48a8-120">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d48a8-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d48a8-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="d48a8-121">-WorkspaceObject</span></span>
<span data-ttu-id="d48a8-122">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d48a8-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d48a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48a8-123">CommonParameters</span></span>
<span data-ttu-id="d48a8-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48a8-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d48a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48a8-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d48a8-126">INPUTS</span></span>

### <span data-ttu-id="d48a8-127">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d48a8-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d48a8-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d48a8-128">OUTPUTS</span></span>

### <span data-ttu-id="d48a8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d48a8-129">System.Boolean</span></span>

## <span data-ttu-id="d48a8-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d48a8-130">NOTES</span></span>

## <span data-ttu-id="d48a8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d48a8-131">RELATED LINKS</span></span>
