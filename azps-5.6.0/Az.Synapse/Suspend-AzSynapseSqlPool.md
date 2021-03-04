---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893061"
---
# <span data-ttu-id="76097-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="76097-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="76097-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76097-102">SYNOPSIS</span></span>
<span data-ttu-id="76097-103">Suspende um pool do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="76097-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="76097-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76097-104">SYNTAX</span></span>

### <span data-ttu-id="76097-105">SuspendByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76097-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76097-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76097-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76097-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76097-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76097-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76097-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76097-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76097-109">DESCRIPTION</span></span>
<span data-ttu-id="76097-110">O cmdlet **Suspend-AzSynapseSqlPool** suspende um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="76097-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="76097-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76097-111">EXAMPLES</span></span>

### <span data-ttu-id="76097-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76097-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="76097-113">Este comando suspende um pool ativo do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="76097-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="76097-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76097-114">PARAMETERS</span></span>

### <span data-ttu-id="76097-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76097-115">-AsJob</span></span>
<span data-ttu-id="76097-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76097-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76097-117">-DefaultProfile</span></span>
<span data-ttu-id="76097-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76097-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76097-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76097-119">-InputObject</span></span>
<span data-ttu-id="76097-120">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="76097-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76097-121">-Name</span><span class="sxs-lookup"><span data-stu-id="76097-121">-Name</span></span>
<span data-ttu-id="76097-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="76097-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76097-123">-PassThru</span></span>
<span data-ttu-id="76097-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="76097-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="76097-125">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="76097-125">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76097-126">-ResourceGroupName</span></span>
<span data-ttu-id="76097-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76097-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76097-128">-ResourceId</span></span>
<span data-ttu-id="76097-129">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="76097-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76097-130">-WorkspaceName</span></span>
<span data-ttu-id="76097-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="76097-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="76097-132">-WorkspaceObject</span></span>
<span data-ttu-id="76097-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="76097-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76097-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76097-134">-Confirm</span></span>
<span data-ttu-id="76097-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76097-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76097-136">-WhatIf</span></span>
<span data-ttu-id="76097-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76097-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76097-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76097-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76097-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76097-139">CommonParameters</span></span>
<span data-ttu-id="76097-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76097-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76097-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76097-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76097-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76097-142">INPUTS</span></span>

### <span data-ttu-id="76097-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76097-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="76097-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="76097-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="76097-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76097-145">OUTPUTS</span></span>

### <span data-ttu-id="76097-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="76097-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="76097-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="76097-147">NOTES</span></span>

## <span data-ttu-id="76097-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76097-148">RELATED LINKS</span></span>
