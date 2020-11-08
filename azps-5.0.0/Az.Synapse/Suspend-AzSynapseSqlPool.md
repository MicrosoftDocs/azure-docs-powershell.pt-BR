---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115163"
---
# <span data-ttu-id="21964-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="21964-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="21964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21964-102">SYNOPSIS</span></span>
<span data-ttu-id="21964-103">Suspende um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="21964-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="21964-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21964-104">SYNTAX</span></span>

### <span data-ttu-id="21964-105">SuspendByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="21964-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21964-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21964-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21964-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21964-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21964-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21964-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21964-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21964-109">DESCRIPTION</span></span>
<span data-ttu-id="21964-110">O cmdlet **Suspend-AzSynapseSqlPool** suspende um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="21964-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="21964-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21964-111">EXAMPLES</span></span>

### <span data-ttu-id="21964-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21964-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="21964-113">Esse comando suspende um pool SQL do Azure Synapse Analytics ativo.</span><span class="sxs-lookup"><span data-stu-id="21964-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="21964-114">OS</span><span class="sxs-lookup"><span data-stu-id="21964-114">PARAMETERS</span></span>

### <span data-ttu-id="21964-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21964-115">-AsJob</span></span>
<span data-ttu-id="21964-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21964-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21964-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21964-117">-DefaultProfile</span></span>
<span data-ttu-id="21964-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21964-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21964-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21964-119">-InputObject</span></span>
<span data-ttu-id="21964-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="21964-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21964-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="21964-121">-Name</span></span>
<span data-ttu-id="21964-122">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="21964-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21964-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21964-123">-PassThru</span></span>
<span data-ttu-id="21964-124">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="21964-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="21964-125">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21964-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="21964-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21964-126">-ResourceGroupName</span></span>
<span data-ttu-id="21964-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21964-127">Resource group name.</span></span>

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

### <span data-ttu-id="21964-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21964-128">-ResourceId</span></span>
<span data-ttu-id="21964-129">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="21964-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="21964-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21964-130">-WorkspaceName</span></span>
<span data-ttu-id="21964-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="21964-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="21964-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="21964-132">-WorkspaceObject</span></span>
<span data-ttu-id="21964-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="21964-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21964-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21964-134">-Confirm</span></span>
<span data-ttu-id="21964-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21964-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21964-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21964-136">-WhatIf</span></span>
<span data-ttu-id="21964-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21964-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21964-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21964-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21964-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21964-139">CommonParameters</span></span>
<span data-ttu-id="21964-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21964-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21964-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21964-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21964-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21964-142">INPUTS</span></span>

### <span data-ttu-id="21964-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="21964-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="21964-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="21964-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="21964-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21964-145">OUTPUTS</span></span>

### <span data-ttu-id="21964-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="21964-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="21964-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21964-147">NOTES</span></span>

## <span data-ttu-id="21964-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21964-148">RELATED LINKS</span></span>
