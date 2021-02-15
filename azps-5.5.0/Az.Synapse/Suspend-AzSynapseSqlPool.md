---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: f0d06956c15b83511989b0ec5917918773f92293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118871"
---
# <span data-ttu-id="c8622-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c8622-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="c8622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8622-102">SYNOPSIS</span></span>
<span data-ttu-id="c8622-103">Suspende um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8622-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c8622-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8622-104">SYNTAX</span></span>

### <span data-ttu-id="c8622-105">SuspendByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8622-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8622-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8622-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8622-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8622-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8622-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8622-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8622-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8622-109">DESCRIPTION</span></span>
<span data-ttu-id="c8622-110">O cmdlet **Suspend-AzSynapseSqlPool** suspende um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8622-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c8622-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8622-111">EXAMPLES</span></span>

### <span data-ttu-id="c8622-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8622-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c8622-113">Esse comando suspende um pool SQL ativo do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8622-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c8622-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8622-114">PARAMETERS</span></span>

### <span data-ttu-id="c8622-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8622-115">-AsJob</span></span>
<span data-ttu-id="c8622-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8622-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8622-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8622-117">-DefaultProfile</span></span>
<span data-ttu-id="c8622-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8622-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8622-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8622-119">-InputObject</span></span>
<span data-ttu-id="c8622-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8622-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8622-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8622-121">-Name</span></span>
<span data-ttu-id="c8622-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8622-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="c8622-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8622-123">-PassThru</span></span>
<span data-ttu-id="c8622-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="c8622-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c8622-125">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c8622-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c8622-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8622-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8622-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8622-127">Resource group name.</span></span>

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

### <span data-ttu-id="c8622-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8622-128">-ResourceId</span></span>
<span data-ttu-id="c8622-129">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8622-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="c8622-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c8622-130">-WorkspaceName</span></span>
<span data-ttu-id="c8622-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8622-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c8622-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8622-132">-WorkspaceObject</span></span>
<span data-ttu-id="c8622-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8622-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8622-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8622-134">-Confirm</span></span>
<span data-ttu-id="c8622-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8622-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8622-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8622-136">-WhatIf</span></span>
<span data-ttu-id="c8622-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8622-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8622-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8622-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8622-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8622-139">CommonParameters</span></span>
<span data-ttu-id="c8622-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8622-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8622-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8622-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8622-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8622-142">INPUTS</span></span>

### <span data-ttu-id="c8622-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8622-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c8622-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c8622-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c8622-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8622-145">OUTPUTS</span></span>

### <span data-ttu-id="c8622-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c8622-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c8622-147">Notas</span><span class="sxs-lookup"><span data-stu-id="c8622-147">NOTES</span></span>

## <span data-ttu-id="c8622-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8622-148">RELATED LINKS</span></span>
