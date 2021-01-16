---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272344"
---
# <span data-ttu-id="68979-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="68979-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="68979-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68979-102">SYNOPSIS</span></span>
<span data-ttu-id="68979-103">Exclui um ponto de restauração de pool do SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="68979-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="68979-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68979-104">SYNTAX</span></span>

### <span data-ttu-id="68979-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="68979-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68979-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68979-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68979-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68979-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68979-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68979-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68979-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68979-109">DESCRIPTION</span></span>
<span data-ttu-id="68979-110">O cmdlet **Remove-AzSynapseSqlPoolRestorePoint** exclui permanentemente um ponto de restauração de pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="68979-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="68979-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68979-111">EXAMPLES</span></span>

### <span data-ttu-id="68979-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68979-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="68979-113">Esse comando exclui um ponto de restauração de pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="68979-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="68979-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="68979-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="68979-115">Esse comando exclui um pipeline de restauração do pool do SQL Synapse Analytics do Azure.</span><span class="sxs-lookup"><span data-stu-id="68979-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="68979-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="68979-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="68979-117">Esse comando exclui um pipeline de restauração do pool do SQL Synapse Analytics do Azure.</span><span class="sxs-lookup"><span data-stu-id="68979-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="68979-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="68979-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="68979-119">Esse comando exclui um ponto de restauração de pool do SQL do Azure Synapse Analytics com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="68979-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="68979-120">OS</span><span class="sxs-lookup"><span data-stu-id="68979-120">PARAMETERS</span></span>

### <span data-ttu-id="68979-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68979-121">-AsJob</span></span>
<span data-ttu-id="68979-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="68979-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68979-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68979-123">-DefaultProfile</span></span>
<span data-ttu-id="68979-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68979-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68979-125">-Force</span><span class="sxs-lookup"><span data-stu-id="68979-125">-Force</span></span>
<span data-ttu-id="68979-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="68979-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68979-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68979-127">-InputObject</span></span>
<span data-ttu-id="68979-128">Objeto de entrada do tempo de criação do pool de SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="68979-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68979-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68979-129">-PassThru</span></span>
<span data-ttu-id="68979-130">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="68979-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="68979-131">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="68979-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="68979-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68979-132">-ResourceGroupName</span></span>
<span data-ttu-id="68979-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68979-133">Resource group name.</span></span>

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

### <span data-ttu-id="68979-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68979-134">-ResourceId</span></span>
<span data-ttu-id="68979-135">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="68979-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="68979-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="68979-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="68979-137">Nome da data de criação do ponto de restauração do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="68979-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

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

### <span data-ttu-id="68979-138">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="68979-138">-SqlPoolName</span></span>
<span data-ttu-id="68979-139">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="68979-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="68979-140">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="68979-140">-SqlPoolObject</span></span>
<span data-ttu-id="68979-141">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="68979-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68979-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68979-142">-WorkspaceName</span></span>
<span data-ttu-id="68979-143">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="68979-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68979-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68979-144">-Confirm</span></span>
<span data-ttu-id="68979-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68979-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68979-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68979-146">-WhatIf</span></span>
<span data-ttu-id="68979-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68979-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68979-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68979-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68979-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68979-149">CommonParameters</span></span>
<span data-ttu-id="68979-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68979-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68979-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68979-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68979-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68979-152">INPUTS</span></span>

### <span data-ttu-id="68979-153">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68979-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="68979-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="68979-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="68979-155">Microsoft. Azure. Commands. Synapse. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="68979-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="68979-156">System. String</span><span class="sxs-lookup"><span data-stu-id="68979-156">System.String</span></span>

## <span data-ttu-id="68979-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68979-157">OUTPUTS</span></span>

### <span data-ttu-id="68979-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68979-158">System.Boolean</span></span>

## <span data-ttu-id="68979-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68979-159">NOTES</span></span>

## <span data-ttu-id="68979-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68979-160">RELATED LINKS</span></span>
