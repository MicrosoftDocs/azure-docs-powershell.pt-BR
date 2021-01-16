---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259896"
---
# <span data-ttu-id="70531-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="70531-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="70531-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70531-102">SYNOPSIS</span></span>
<span data-ttu-id="70531-103">Exclui um ponto de restauração de pool do SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="70531-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="70531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70531-104">SYNTAX</span></span>

### <span data-ttu-id="70531-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="70531-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70531-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70531-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70531-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70531-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70531-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70531-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70531-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70531-109">DESCRIPTION</span></span>
<span data-ttu-id="70531-110">O cmdlet **Remove-AzSynapseSqlPoolRestorePoint** exclui permanentemente um ponto de restauração de pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="70531-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="70531-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70531-111">EXAMPLES</span></span>

### <span data-ttu-id="70531-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70531-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="70531-113">Esse comando exclui um ponto de restauração de pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="70531-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="70531-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="70531-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="70531-115">Esse comando exclui um pipeline de restauração do pool do SQL Synapse Analytics do Azure.</span><span class="sxs-lookup"><span data-stu-id="70531-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="70531-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="70531-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="70531-117">Esse comando exclui um pipeline de restauração do pool do SQL Synapse Analytics do Azure.</span><span class="sxs-lookup"><span data-stu-id="70531-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="70531-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="70531-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="70531-119">Esse comando exclui um ponto de restauração de pool do SQL do Azure Synapse Analytics com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="70531-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="70531-120">OS</span><span class="sxs-lookup"><span data-stu-id="70531-120">PARAMETERS</span></span>

### <span data-ttu-id="70531-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70531-121">-AsJob</span></span>
<span data-ttu-id="70531-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="70531-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70531-123">-Force</span><span class="sxs-lookup"><span data-stu-id="70531-123">-Force</span></span>
<span data-ttu-id="70531-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="70531-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="70531-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70531-125">-InputObject</span></span>
<span data-ttu-id="70531-126">Objeto de entrada do tempo de criação do pool de SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="70531-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70531-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="70531-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="70531-128">Nome da data de criação do ponto de restauração do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="70531-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70531-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70531-129">-PassThru</span></span>
<span data-ttu-id="70531-130">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="70531-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="70531-131">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="70531-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="70531-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70531-132">-ResourceGroupName</span></span>
<span data-ttu-id="70531-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70531-133">Resource group name.</span></span>

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

### <span data-ttu-id="70531-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70531-134">-ResourceId</span></span>
<span data-ttu-id="70531-135">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="70531-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="70531-136">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="70531-136">-SqlPoolName</span></span>
<span data-ttu-id="70531-137">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="70531-137">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="70531-138">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="70531-138">-SqlPoolObject</span></span>
<span data-ttu-id="70531-139">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="70531-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70531-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="70531-140">-WorkspaceName</span></span>
<span data-ttu-id="70531-141">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="70531-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="70531-142">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="70531-142">-WorkspaceObject</span></span>
<span data-ttu-id="70531-143">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="70531-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="70531-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70531-144">-Confirm</span></span>
<span data-ttu-id="70531-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70531-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70531-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70531-146">-WhatIf</span></span>
<span data-ttu-id="70531-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70531-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70531-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70531-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70531-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70531-149">CommonParameters</span></span>
<span data-ttu-id="70531-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70531-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70531-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70531-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70531-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70531-152">INPUTS</span></span>

### <span data-ttu-id="70531-153">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="70531-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="70531-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70531-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="70531-155">Microsoft. Azure. Commands. Synapse. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="70531-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="70531-156">System. String</span><span class="sxs-lookup"><span data-stu-id="70531-156">System.String</span></span>

## <span data-ttu-id="70531-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70531-157">OUTPUTS</span></span>

### <span data-ttu-id="70531-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70531-158">System.Boolean</span></span>

## <span data-ttu-id="70531-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70531-159">NOTES</span></span>

## <span data-ttu-id="70531-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70531-160">RELATED LINKS</span></span>
