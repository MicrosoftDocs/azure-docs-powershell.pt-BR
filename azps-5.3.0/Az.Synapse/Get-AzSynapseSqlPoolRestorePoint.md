---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272411"
---
# <span data-ttu-id="a5658-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a5658-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="a5658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5658-102">SYNOPSIS</span></span>
<span data-ttu-id="a5658-103">Recupera os pontos de restauração distintos a partir dos quais um pool do SQL Synapse Analytics pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a5658-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="a5658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5658-104">SYNTAX</span></span>

### <span data-ttu-id="a5658-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5658-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5658-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5658-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5658-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5658-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5658-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5658-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5658-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5658-109">DESCRIPTION</span></span>
<span data-ttu-id="a5658-110">O cmdlet **Get-AzSynapseSqlPoolRestorePoint** recupera os pontos de restauração distintos nos quais um pool SQL do Azure Synapse Analytics pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a5658-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="a5658-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5658-111">EXAMPLES</span></span>

### <span data-ttu-id="a5658-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5658-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a5658-113">Esse comando retorna todos os pontos de restauração disponíveis para o pool SQL do Azure Synapse Analytics chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a5658-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="a5658-114">OS</span><span class="sxs-lookup"><span data-stu-id="a5658-114">PARAMETERS</span></span>

### <span data-ttu-id="a5658-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5658-115">-DefaultProfile</span></span>
<span data-ttu-id="a5658-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5658-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5658-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5658-117">-InputObject</span></span>
<span data-ttu-id="a5658-118">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5658-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5658-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5658-119">-Name</span></span>
<span data-ttu-id="a5658-120">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a5658-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5658-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5658-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5658-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5658-122">Resource group name.</span></span>

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

### <span data-ttu-id="a5658-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5658-123">-ResourceId</span></span>
<span data-ttu-id="a5658-124">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a5658-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a5658-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5658-125">-WorkspaceName</span></span>
<span data-ttu-id="a5658-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="a5658-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5658-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a5658-127">-WorkspaceObject</span></span>
<span data-ttu-id="a5658-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5658-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5658-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5658-129">CommonParameters</span></span>
<span data-ttu-id="a5658-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5658-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5658-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5658-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5658-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5658-132">INPUTS</span></span>

### <span data-ttu-id="a5658-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5658-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a5658-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a5658-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a5658-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5658-135">OUTPUTS</span></span>

### <span data-ttu-id="a5658-136">Microsoft. Azure. Management. Synapse. Models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="a5658-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="a5658-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5658-137">NOTES</span></span>

## <span data-ttu-id="a5658-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5658-138">RELATED LINKS</span></span>
