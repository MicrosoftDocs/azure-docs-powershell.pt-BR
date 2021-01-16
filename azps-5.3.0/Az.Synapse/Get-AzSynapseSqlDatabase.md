---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272419"
---
# <span data-ttu-id="7703f-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7703f-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="7703f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7703f-102">SYNOPSIS</span></span>
<span data-ttu-id="7703f-103">Obtém um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7703f-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="7703f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7703f-104">SYNTAX</span></span>

### <span data-ttu-id="7703f-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7703f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7703f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7703f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7703f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7703f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7703f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7703f-108">DESCRIPTION</span></span>
<span data-ttu-id="7703f-109">[Este recurso está em uma visualização limitada, inicialmente acessível somente para determinadas assinaturas.] O cmdlet **Get-AzSynapseSqlDatabase** Obtém informações sobre um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7703f-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="7703f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7703f-110">EXAMPLES</span></span>

### <span data-ttu-id="7703f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7703f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7703f-112">Esse comando obtém todos os bancos de dados SQL em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7703f-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="7703f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7703f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="7703f-114">Esse comando obtém o banco de dados SQL em espaço de trabalho ContosoWorkspace com o nome ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="7703f-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="7703f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7703f-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="7703f-116">Esse comando obtém todos os bancos de dados SQL em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7703f-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="7703f-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7703f-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="7703f-118">Esse comando obtém o banco de dados SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="7703f-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="7703f-119">OS</span><span class="sxs-lookup"><span data-stu-id="7703f-119">PARAMETERS</span></span>

### <span data-ttu-id="7703f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7703f-120">-DefaultProfile</span></span>
<span data-ttu-id="7703f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7703f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7703f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7703f-122">-Name</span></span>
<span data-ttu-id="7703f-123">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="7703f-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7703f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7703f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7703f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7703f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7703f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7703f-126">-ResourceId</span></span>
<span data-ttu-id="7703f-127">Identificador de recurso do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="7703f-127">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7703f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7703f-128">-WorkspaceName</span></span>
<span data-ttu-id="7703f-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="7703f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7703f-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7703f-130">-WorkspaceObject</span></span>
<span data-ttu-id="7703f-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7703f-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7703f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7703f-132">CommonParameters</span></span>
<span data-ttu-id="7703f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7703f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7703f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7703f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7703f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7703f-135">INPUTS</span></span>

### <span data-ttu-id="7703f-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7703f-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7703f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7703f-137">OUTPUTS</span></span>

### <span data-ttu-id="7703f-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7703f-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="7703f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7703f-139">NOTES</span></span>

## <span data-ttu-id="7703f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7703f-140">RELATED LINKS</span></span>
