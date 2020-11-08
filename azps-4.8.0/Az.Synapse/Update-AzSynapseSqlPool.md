---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113457"
---
# <span data-ttu-id="d6b0f-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d6b0f-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d6b0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b0f-103">Atualiza um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d6b0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6b0f-104">SYNTAX</span></span>

### <span data-ttu-id="d6b0f-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6b0f-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b0f-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b0f-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b0f-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6b0f-117">DESCRIPTION</span></span>
<span data-ttu-id="d6b0f-118">O cmdlet **Update-AzSynapseSqlPool** atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d6b0f-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6b0f-119">EXAMPLES</span></span>

### <span data-ttu-id="d6b0f-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6b0f-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="d6b0f-121">Esse comando atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="d6b0f-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d6b0f-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="d6b0f-123">Esse comando atualiza um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d6b0f-124">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d6b0f-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="d6b0f-125">Esse comando atualiza um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d6b0f-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d6b0f-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="d6b0f-127">Esse comando atualiza um pool SQL do Azure Synapse Analytics com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="d6b0f-128">OS</span><span class="sxs-lookup"><span data-stu-id="d6b0f-128">PARAMETERS</span></span>

### <span data-ttu-id="d6b0f-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6b0f-129">-AsJob</span></span>
<span data-ttu-id="d6b0f-130">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d6b0f-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6b0f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b0f-131">-DefaultProfile</span></span>
<span data-ttu-id="d6b0f-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b0f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b0f-133">-InputObject</span></span>
<span data-ttu-id="d6b0f-134">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6b0f-135">-Name</span></span>
<span data-ttu-id="d6b0f-136">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6b0f-137">-PassThru</span></span>
<span data-ttu-id="d6b0f-138">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d6b0f-139">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d6b0f-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="d6b0f-140">-PerformanceLevel</span></span>
<span data-ttu-id="d6b0f-141">A camada de serviço SQL e o nível de desempenho a serem atribuídos ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="d6b0f-142">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b0f-143">-ResourceGroupName</span></span>
<span data-ttu-id="d6b0f-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6b0f-145">-ResourceId</span></span>
<span data-ttu-id="d6b0f-146">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-147">-Retomar</span><span class="sxs-lookup"><span data-stu-id="d6b0f-147">-Resume</span></span>
<span data-ttu-id="d6b0f-148">Indica a retomada do pool de SQL</span><span class="sxs-lookup"><span data-stu-id="d6b0f-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-149">-Suspender</span><span class="sxs-lookup"><span data-stu-id="d6b0f-149">-Suspend</span></span>
<span data-ttu-id="d6b0f-150">Indica a pausa do pool de SQL</span><span class="sxs-lookup"><span data-stu-id="d6b0f-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-151">-Marca</span><span class="sxs-lookup"><span data-stu-id="d6b0f-151">-Tag</span></span>
<span data-ttu-id="d6b0f-152">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-153">-Versão</span><span class="sxs-lookup"><span data-stu-id="d6b0f-153">-Version</span></span>
<span data-ttu-id="d6b0f-154">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="d6b0f-155">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-155">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="d6b0f-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6b0f-156">-WorkspaceName</span></span>
<span data-ttu-id="d6b0f-157">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-158">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="d6b0f-158">-WorkspaceObject</span></span>
<span data-ttu-id="d6b0f-159">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b0f-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6b0f-160">-Confirm</span></span>
<span data-ttu-id="d6b0f-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b0f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b0f-162">-WhatIf</span></span>
<span data-ttu-id="d6b0f-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b0f-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b0f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b0f-165">CommonParameters</span></span>
<span data-ttu-id="d6b0f-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b0f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b0f-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6b0f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b0f-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6b0f-168">INPUTS</span></span>

### <span data-ttu-id="d6b0f-169">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6b0f-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d6b0f-170">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d6b0f-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d6b0f-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6b0f-171">OUTPUTS</span></span>

### <span data-ttu-id="d6b0f-172">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d6b0f-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d6b0f-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6b0f-173">NOTES</span></span>

## <span data-ttu-id="d6b0f-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6b0f-174">RELATED LINKS</span></span>
