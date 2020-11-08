---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116610"
---
# <span data-ttu-id="088de-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="088de-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="088de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="088de-102">SYNOPSIS</span></span>
<span data-ttu-id="088de-103">Obtém um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="088de-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="088de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="088de-104">SYNTAX</span></span>

### <span data-ttu-id="088de-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="088de-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="088de-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="088de-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="088de-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="088de-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="088de-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="088de-108">DESCRIPTION</span></span>
<span data-ttu-id="088de-109">O cmdlet **Get-AzSynapseSqlPool** Obtém informações sobre um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="088de-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="088de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="088de-110">EXAMPLES</span></span>

### <span data-ttu-id="088de-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="088de-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="088de-112">Esse comando obtém todos os pools SQL em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088de-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="088de-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="088de-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="088de-114">Esse comando obtém o pool do SQL em ContosoWorkspace do espaço de trabalho com o nome ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="088de-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="088de-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="088de-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="088de-116">Esse comando obtém todos os pools SQL em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="088de-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="088de-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="088de-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="088de-118">Este comando obtém o pool de SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="088de-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="088de-119">OS</span><span class="sxs-lookup"><span data-stu-id="088de-119">PARAMETERS</span></span>

### <span data-ttu-id="088de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088de-120">-DefaultProfile</span></span>
<span data-ttu-id="088de-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="088de-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="088de-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="088de-122">-Name</span></span>
<span data-ttu-id="088de-123">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="088de-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="088de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="088de-124">-ResourceGroupName</span></span>
<span data-ttu-id="088de-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="088de-125">Resource group name.</span></span>

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

### <span data-ttu-id="088de-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="088de-126">-ResourceId</span></span>
<span data-ttu-id="088de-127">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="088de-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="088de-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="088de-128">-Version</span></span>
<span data-ttu-id="088de-129">[Este recurso está em uma visualização limitada, inicialmente acessível somente para determinadas assinaturas.] Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="088de-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="088de-130">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="088de-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="088de-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="088de-131">-WorkspaceName</span></span>
<span data-ttu-id="088de-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="088de-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="088de-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="088de-133">-WorkspaceObject</span></span>
<span data-ttu-id="088de-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="088de-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="088de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088de-135">CommonParameters</span></span>
<span data-ttu-id="088de-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="088de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088de-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="088de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088de-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="088de-138">INPUTS</span></span>

### <span data-ttu-id="088de-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="088de-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="088de-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="088de-140">OUTPUTS</span></span>

### <span data-ttu-id="088de-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="088de-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="088de-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="088de-142">NOTES</span></span>

## <span data-ttu-id="088de-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="088de-143">RELATED LINKS</span></span>
