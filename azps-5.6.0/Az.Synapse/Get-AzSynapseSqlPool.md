---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901536"
---
# <span data-ttu-id="949a4-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="949a4-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="949a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="949a4-102">SYNOPSIS</span></span>
<span data-ttu-id="949a4-103">Obtém um pool de análise SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="949a4-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="949a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="949a4-104">SYNTAX</span></span>

### <span data-ttu-id="949a4-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="949a4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949a4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="949a4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949a4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="949a4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="949a4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="949a4-108">DESCRIPTION</span></span>
<span data-ttu-id="949a4-109">O cmdlet **Get-AzSynapseSqlPool** obtém informações sobre um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="949a4-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="949a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="949a4-110">EXAMPLES</span></span>

### <span data-ttu-id="949a4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="949a4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="949a4-112">Esse comando obtém todos os SQL pools em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="949a4-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="949a4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="949a4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="949a4-114">Este comando obtém o pool SQL no espaço de trabalho ContosoWorkspace com o nome ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="949a4-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="949a4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="949a4-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="949a4-116">Esse comando obtém todos os pools SQL em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="949a4-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="949a4-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="949a4-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="949a4-118">Esse comando obtém o pool SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="949a4-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="949a4-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="949a4-119">PARAMETERS</span></span>

### <span data-ttu-id="949a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949a4-120">-DefaultProfile</span></span>
<span data-ttu-id="949a4-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="949a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="949a4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="949a4-122">-Name</span></span>
<span data-ttu-id="949a4-123">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="949a4-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="949a4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="949a4-125">Resource group name.</span></span>

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

### <span data-ttu-id="949a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="949a4-126">-ResourceId</span></span>
<span data-ttu-id="949a4-127">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="949a4-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="949a4-128">-Version</span><span class="sxs-lookup"><span data-stu-id="949a4-128">-Version</span></span>
<span data-ttu-id="949a4-129">[Esse recurso está em uma visualização limitada, inicialmente acessível apenas a determinadas assinaturas.] Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="949a4-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="949a4-130">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="949a4-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="949a4-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="949a4-131">-WorkspaceName</span></span>
<span data-ttu-id="949a4-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="949a4-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="949a4-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="949a4-133">-WorkspaceObject</span></span>
<span data-ttu-id="949a4-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="949a4-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="949a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949a4-135">CommonParameters</span></span>
<span data-ttu-id="949a4-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949a4-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="949a4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949a4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="949a4-138">INPUTS</span></span>

### <span data-ttu-id="949a4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="949a4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="949a4-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="949a4-140">OUTPUTS</span></span>

### <span data-ttu-id="949a4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="949a4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="949a4-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="949a4-142">NOTES</span></span>

## <span data-ttu-id="949a4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="949a4-143">RELATED LINKS</span></span>
