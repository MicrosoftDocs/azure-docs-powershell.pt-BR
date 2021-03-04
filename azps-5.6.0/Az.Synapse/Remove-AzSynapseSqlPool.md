---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891546"
---
# <span data-ttu-id="c0fa7-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c0fa7-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="c0fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fa7-103">Exclui um pool do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c0fa7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0fa7-104">SYNTAX</span></span>

### <span data-ttu-id="c0fa7-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0fa7-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0fa7-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fa7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0fa7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fa7-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0fa7-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0fa7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0fa7-109">DESCRIPTION</span></span>
<span data-ttu-id="c0fa7-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c0fa7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-111">EXAMPLES</span></span>

### <span data-ttu-id="c0fa7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0fa7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c0fa7-113">Este comando exclui um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="c0fa7-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0fa7-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="c0fa7-115">Este comando exclui um pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="c0fa7-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c0fa7-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="c0fa7-117">Este comando exclui um pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="c0fa7-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c0fa7-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="c0fa7-119">Este comando exclui um pool do Azure Synapse Analytics SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="c0fa7-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-120">PARAMETERS</span></span>

### <span data-ttu-id="c0fa7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0fa7-121">-AsJob</span></span>
<span data-ttu-id="c0fa7-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c0fa7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0fa7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fa7-123">-DefaultProfile</span></span>
<span data-ttu-id="c0fa7-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0fa7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c0fa7-125">-Force</span></span>
<span data-ttu-id="c0fa7-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c0fa7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0fa7-127">-InputObject</span></span>
<span data-ttu-id="c0fa7-128">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c0fa7-129">-Name</span></span>
<span data-ttu-id="c0fa7-130">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0fa7-131">-PassThru</span></span>
<span data-ttu-id="c0fa7-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c0fa7-133">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c0fa7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0fa7-134">-ResourceGroupName</span></span>
<span data-ttu-id="c0fa7-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0fa7-136">-ResourceId</span></span>
<span data-ttu-id="c0fa7-137">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-138">-Version</span><span class="sxs-lookup"><span data-stu-id="c0fa7-138">-Version</span></span>
<span data-ttu-id="c0fa7-139">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="c0fa7-140">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="c0fa7-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0fa7-141">-WorkspaceName</span></span>
<span data-ttu-id="c0fa7-142">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0fa7-143">-WorkspaceObject</span></span>
<span data-ttu-id="c0fa7-144">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0fa7-145">-Confirm</span></span>
<span data-ttu-id="c0fa7-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0fa7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-147">-WhatIf</span></span>
<span data-ttu-id="c0fa7-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0fa7-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0fa7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fa7-150">CommonParameters</span></span>
<span data-ttu-id="c0fa7-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fa7-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0fa7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fa7-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-153">INPUTS</span></span>

### <span data-ttu-id="c0fa7-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0fa7-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c0fa7-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c0fa7-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="c0fa7-156">System.String</span><span class="sxs-lookup"><span data-stu-id="c0fa7-156">System.String</span></span>

## <span data-ttu-id="c0fa7-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-157">OUTPUTS</span></span>

### <span data-ttu-id="c0fa7-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0fa7-158">System.Boolean</span></span>

## <span data-ttu-id="c0fa7-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0fa7-159">NOTES</span></span>

## <span data-ttu-id="c0fa7-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-160">RELATED LINKS</span></span>
