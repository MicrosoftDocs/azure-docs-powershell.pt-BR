---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ef4684cd6f4c852a9833dfdbe8c26ae1df6d326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885768"
---
# <span data-ttu-id="4361e-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="4361e-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="4361e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4361e-102">SYNOPSIS</span></span>
<span data-ttu-id="4361e-103">Recupera os pontos de restauração distintos dos quais um pool do Synapse Analytics SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="4361e-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="4361e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4361e-104">SYNTAX</span></span>

### <span data-ttu-id="4361e-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4361e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4361e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4361e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4361e-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4361e-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4361e-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4361e-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4361e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4361e-109">DESCRIPTION</span></span>
<span data-ttu-id="4361e-110">O cmdlet **Get-AzSynapseSqlPoolRestorePoint** recupera os pontos de restauração distintos dos SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4361e-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="4361e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4361e-111">EXAMPLES</span></span>

### <span data-ttu-id="4361e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4361e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="4361e-113">Este comando retorna todos os pontos de restauração disponíveis para o pool do Azure Synapse Analytics SQL chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="4361e-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="4361e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4361e-114">PARAMETERS</span></span>

### <span data-ttu-id="4361e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4361e-115">-DefaultProfile</span></span>
<span data-ttu-id="4361e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4361e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4361e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4361e-117">-InputObject</span></span>
<span data-ttu-id="4361e-118">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4361e-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4361e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4361e-119">-Name</span></span>
<span data-ttu-id="4361e-120">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4361e-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4361e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4361e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4361e-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4361e-122">Resource group name.</span></span>

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

### <span data-ttu-id="4361e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4361e-123">-ResourceId</span></span>
<span data-ttu-id="4361e-124">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4361e-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4361e-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4361e-125">-WorkspaceName</span></span>
<span data-ttu-id="4361e-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4361e-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4361e-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4361e-127">-WorkspaceObject</span></span>
<span data-ttu-id="4361e-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4361e-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4361e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4361e-129">CommonParameters</span></span>
<span data-ttu-id="4361e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4361e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4361e-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4361e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4361e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4361e-132">INPUTS</span></span>

### <span data-ttu-id="4361e-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4361e-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4361e-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4361e-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4361e-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4361e-135">OUTPUTS</span></span>

### <span data-ttu-id="4361e-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="4361e-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="4361e-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="4361e-137">NOTES</span></span>

## <span data-ttu-id="4361e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4361e-138">RELATED LINKS</span></span>
