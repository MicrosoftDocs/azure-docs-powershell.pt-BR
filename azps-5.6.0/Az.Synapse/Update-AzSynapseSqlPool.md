---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886380"
---
# <span data-ttu-id="5a94e-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5a94e-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5a94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a94e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a94e-103">Atualiza um pool do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="5a94e-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5a94e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a94e-104">SYNTAX</span></span>

### <span data-ttu-id="5a94e-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a94e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a94e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a94e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a94e-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a94e-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a94e-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a94e-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a94e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a94e-109">DESCRIPTION</span></span>
<span data-ttu-id="5a94e-110">O cmdlet **Update-AzSynapseSqlPool** atualiza um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="5a94e-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5a94e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a94e-111">EXAMPLES</span></span>

### <span data-ttu-id="5a94e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a94e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="5a94e-113">Este comando atualiza um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="5a94e-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="5a94e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a94e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="5a94e-115">Este comando atualiza um pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a94e-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="5a94e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5a94e-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="5a94e-117">Este comando atualiza um pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a94e-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="5a94e-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5a94e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="5a94e-119">Este comando atualiza um pool do Azure Synapse Analytics SQL com a ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="5a94e-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="5a94e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a94e-120">PARAMETERS</span></span>

### <span data-ttu-id="5a94e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a94e-121">-AsJob</span></span>
<span data-ttu-id="5a94e-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5a94e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a94e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a94e-123">-DefaultProfile</span></span>
<span data-ttu-id="5a94e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a94e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a94e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a94e-125">-InputObject</span></span>
<span data-ttu-id="5a94e-126">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a94e-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5a94e-127">-Name</span></span>
<span data-ttu-id="5a94e-128">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a94e-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a94e-129">-PassThru</span></span>
<span data-ttu-id="5a94e-130">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5a94e-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5a94e-131">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5a94e-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5a94e-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="5a94e-132">-PerformanceLevel</span></span>
<span data-ttu-id="5a94e-133">A SQL nível de serviço e o nível de desempenho a ser atribuído ao pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="5a94e-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="5a94e-134">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="5a94e-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="5a94e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a94e-135">-ResourceGroupName</span></span>
<span data-ttu-id="5a94e-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a94e-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a94e-137">-ResourceId</span></span>
<span data-ttu-id="5a94e-138">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a94e-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a94e-139">-Tag</span></span>
<span data-ttu-id="5a94e-140">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="5a94e-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5a94e-141">-Version</span><span class="sxs-lookup"><span data-stu-id="5a94e-141">-Version</span></span>
<span data-ttu-id="5a94e-142">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a94e-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5a94e-143">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="5a94e-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5a94e-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a94e-144">-WorkspaceName</span></span>
<span data-ttu-id="5a94e-145">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a94e-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a94e-146">-WorkspaceObject</span></span>
<span data-ttu-id="5a94e-147">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a94e-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a94e-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a94e-148">-Confirm</span></span>
<span data-ttu-id="5a94e-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a94e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a94e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a94e-150">-WhatIf</span></span>
<span data-ttu-id="5a94e-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a94e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a94e-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a94e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a94e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a94e-153">CommonParameters</span></span>
<span data-ttu-id="5a94e-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a94e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a94e-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a94e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a94e-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a94e-156">INPUTS</span></span>

### <span data-ttu-id="5a94e-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a94e-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5a94e-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5a94e-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5a94e-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a94e-159">OUTPUTS</span></span>

### <span data-ttu-id="5a94e-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5a94e-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5a94e-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a94e-161">NOTES</span></span>

## <span data-ttu-id="5a94e-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a94e-162">RELATED LINKS</span></span>
