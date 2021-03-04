---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 829227e47c0c68ac8ebe44f1a365898baa6e123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890340"
---
# <span data-ttu-id="a20bd-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a20bd-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a20bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a20bd-102">SYNOPSIS</span></span>
<span data-ttu-id="a20bd-103">Cria um pool de análise SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a20bd-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a20bd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a20bd-104">SYNTAX</span></span>

### <span data-ttu-id="a20bd-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a20bd-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20bd-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a20bd-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20bd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a20bd-107">DESCRIPTION</span></span>
<span data-ttu-id="a20bd-108">O cmdlet **New-AzSynapseSqlPool** cria um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="a20bd-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a20bd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a20bd-109">EXAMPLES</span></span>

### <span data-ttu-id="a20bd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a20bd-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="a20bd-111">Este comando cria um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="a20bd-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a20bd-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a20bd-112">PARAMETERS</span></span>

### <span data-ttu-id="a20bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a20bd-113">-AsJob</span></span>
<span data-ttu-id="a20bd-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a20bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a20bd-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="a20bd-115">-Collation</span></span>
<span data-ttu-id="a20bd-116">O collation define as regras que classificar e comparar dados e não pode ser alterado após a criação SQL pool.</span><span class="sxs-lookup"><span data-stu-id="a20bd-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="a20bd-117">O collation padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="a20bd-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20bd-118">-DefaultProfile</span></span>
<span data-ttu-id="a20bd-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a20bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a20bd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a20bd-120">-Name</span></span>
<span data-ttu-id="a20bd-121">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a20bd-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="a20bd-122">-PerformanceLevel</span></span>
<span data-ttu-id="a20bd-123">A SQL nível de serviço e o nível de desempenho a ser atribuído ao pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="a20bd-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="a20bd-124">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="a20bd-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="a20bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="a20bd-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a20bd-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a20bd-127">-Tag</span></span>
<span data-ttu-id="a20bd-128">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="a20bd-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-129">-Version</span><span class="sxs-lookup"><span data-stu-id="a20bd-129">-Version</span></span>
<span data-ttu-id="a20bd-130">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a20bd-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="a20bd-131">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="a20bd-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="a20bd-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a20bd-132">-WorkspaceName</span></span>
<span data-ttu-id="a20bd-133">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a20bd-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a20bd-134">-WorkspaceObject</span></span>
<span data-ttu-id="a20bd-135">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a20bd-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a20bd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a20bd-136">-Confirm</span></span>
<span data-ttu-id="a20bd-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a20bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20bd-138">-WhatIf</span></span>
<span data-ttu-id="a20bd-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a20bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20bd-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a20bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20bd-141">CommonParameters</span></span>
<span data-ttu-id="a20bd-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20bd-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a20bd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20bd-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a20bd-144">INPUTS</span></span>

### <span data-ttu-id="a20bd-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a20bd-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a20bd-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a20bd-146">OUTPUTS</span></span>

### <span data-ttu-id="a20bd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a20bd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a20bd-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="a20bd-148">NOTES</span></span>

## <span data-ttu-id="a20bd-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a20bd-149">RELATED LINKS</span></span>
