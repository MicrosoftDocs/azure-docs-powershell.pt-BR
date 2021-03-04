---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887837"
---
# <span data-ttu-id="5585e-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5585e-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="5585e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5585e-102">SYNOPSIS</span></span>
<span data-ttu-id="5585e-103">Exclui um ponto de restauração do pool do Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="5585e-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5585e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5585e-104">SYNTAX</span></span>

### <span data-ttu-id="5585e-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5585e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5585e-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5585e-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5585e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5585e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5585e-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5585e-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5585e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5585e-109">DESCRIPTION</span></span>
<span data-ttu-id="5585e-110">O cmdlet **Remove-AzSynapseSqlPoolRestorePoint** exclui permanentemente um ponto de restauração do pool do Azure Synapse SQL Analytics.</span><span class="sxs-lookup"><span data-stu-id="5585e-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5585e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5585e-111">EXAMPLES</span></span>

### <span data-ttu-id="5585e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5585e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5585e-113">Este comando exclui um ponto de restauração do pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="5585e-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="5585e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5585e-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5585e-115">Este comando exclui um ponto de restauração do pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="5585e-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5585e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5585e-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="5585e-117">Este comando exclui um ponto de restauração do pool do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="5585e-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5585e-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5585e-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="5585e-119">Este comando exclui um ponto de restauração do pool do Azure Synapse Analytics SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="5585e-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="5585e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5585e-120">PARAMETERS</span></span>

### <span data-ttu-id="5585e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5585e-121">-AsJob</span></span>
<span data-ttu-id="5585e-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5585e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5585e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5585e-123">-DefaultProfile</span></span>
<span data-ttu-id="5585e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5585e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5585e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5585e-125">-Force</span></span>
<span data-ttu-id="5585e-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5585e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5585e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5585e-127">-InputObject</span></span>
<span data-ttu-id="5585e-128">SQL objeto de entrada de tempo de criação de ponto de restauração do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5585e-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5585e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5585e-129">-Name</span></span>
<span data-ttu-id="5585e-130">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5585e-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5585e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5585e-131">-PassThru</span></span>
<span data-ttu-id="5585e-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5585e-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5585e-133">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5585e-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5585e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5585e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5585e-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5585e-135">Resource group name.</span></span>

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

### <span data-ttu-id="5585e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5585e-136">-ResourceId</span></span>
<span data-ttu-id="5585e-137">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5585e-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5585e-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="5585e-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="5585e-139">Nome da Synapse SQL Data de Criação de Ponto de Restauração.</span><span class="sxs-lookup"><span data-stu-id="5585e-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5585e-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5585e-140">-SqlPoolObject</span></span>
<span data-ttu-id="5585e-141">Objeto de entrada do Sql Pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5585e-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5585e-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5585e-142">-WorkspaceName</span></span>
<span data-ttu-id="5585e-143">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5585e-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5585e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5585e-144">-Confirm</span></span>
<span data-ttu-id="5585e-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5585e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5585e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5585e-146">-WhatIf</span></span>
<span data-ttu-id="5585e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5585e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5585e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5585e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5585e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5585e-149">CommonParameters</span></span>
<span data-ttu-id="5585e-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5585e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5585e-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5585e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5585e-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5585e-152">INPUTS</span></span>

### <span data-ttu-id="5585e-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5585e-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5585e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5585e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="5585e-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5585e-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="5585e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5585e-156">System.String</span></span>

## <span data-ttu-id="5585e-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5585e-157">OUTPUTS</span></span>

### <span data-ttu-id="5585e-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5585e-158">System.Boolean</span></span>

## <span data-ttu-id="5585e-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="5585e-159">NOTES</span></span>

## <span data-ttu-id="5585e-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5585e-160">RELATED LINKS</span></span>
