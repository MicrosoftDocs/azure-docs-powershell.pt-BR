---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 3a9620a6b5fa68fc2d4e5baf647d8dc720d787a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891073"
---
# <span data-ttu-id="9c63f-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9c63f-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9c63f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c63f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c63f-103">Restaura um pool do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="9c63f-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9c63f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c63f-104">SYNTAX</span></span>

### <span data-ttu-id="9c63f-105">RestoreFromBackupIdByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9c63f-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c63f-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c63f-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c63f-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c63f-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c63f-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c63f-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c63f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c63f-109">DESCRIPTION</span></span>
<span data-ttu-id="9c63f-110">O cmdlet **Restore-AzSynapseSqlPool** restaura um pool do Azure Synapse Analytics SQL de um backup ou de um ponto de restauração de qualquer pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="9c63f-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="9c63f-111">O pool SQL é criado como um novo pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="9c63f-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="9c63f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c63f-112">EXAMPLES</span></span>

### <span data-ttu-id="9c63f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c63f-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9c63f-114">Este comando cria um pool do Azure Synapse Analytics SQL restaurando o backup mais recente de qualquer pool de SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="9c63f-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="9c63f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c63f-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9c63f-116">Este comando cria um pool do Azure Synapse Analytics SQL aproveitando um ponto de restauração de qualquer pool de SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="9c63f-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="9c63f-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9c63f-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="9c63f-118">Este comando cria um pool do Azure Synapse Analytics SQL restaurando do backup mais recente de qualquer pool de SQL nessa assinatura com a ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c63f-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="9c63f-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9c63f-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="9c63f-120">Este comando cria um pool do Azure Synapse Analytics SQL aproveitando um ponto de restauração de qualquer pool de SQL nesta assinatura para recuperar ou copiar de um estado anterior com a ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c63f-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="9c63f-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c63f-121">PARAMETERS</span></span>

### <span data-ttu-id="9c63f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c63f-122">-AsJob</span></span>
<span data-ttu-id="9c63f-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9c63f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c63f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c63f-124">-DefaultProfile</span></span>
<span data-ttu-id="9c63f-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c63f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c63f-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="9c63f-126">-FromBackup</span></span>
<span data-ttu-id="9c63f-127">Indica a restauração do backup mais recente de qualquer SQL pool nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="9c63f-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9c63f-128">-FromRestorePoint</span></span>
<span data-ttu-id="9c63f-129">Indica aproveitar um ponto de restauração de qualquer SQL pool nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="9c63f-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9c63f-130">-Name</span></span>
<span data-ttu-id="9c63f-131">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c63f-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9c63f-132">-PerformanceLevel</span></span>
<span data-ttu-id="9c63f-133">A SQL nível de serviço e o nível de desempenho a ser atribuído ao pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="9c63f-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9c63f-134">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9c63f-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c63f-135">-ResourceGroupName</span></span>
<span data-ttu-id="9c63f-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c63f-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c63f-137">-ResourceId</span></span>
<span data-ttu-id="9c63f-138">A ID de recurso do banco de dados a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="9c63f-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="9c63f-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="9c63f-139">-RestorePoint</span></span>
<span data-ttu-id="9c63f-140">Tempo do instantâneo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="9c63f-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9c63f-141">-WorkspaceName</span></span>
<span data-ttu-id="9c63f-142">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c63f-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9c63f-143">-WorkspaceObject</span></span>
<span data-ttu-id="9c63f-144">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c63f-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c63f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c63f-145">-Confirm</span></span>
<span data-ttu-id="9c63f-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c63f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c63f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c63f-147">-WhatIf</span></span>
<span data-ttu-id="9c63f-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c63f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c63f-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c63f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c63f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c63f-150">CommonParameters</span></span>
<span data-ttu-id="9c63f-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c63f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c63f-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c63f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c63f-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c63f-153">INPUTS</span></span>

### <span data-ttu-id="9c63f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c63f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9c63f-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c63f-155">OUTPUTS</span></span>

### <span data-ttu-id="9c63f-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9c63f-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9c63f-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c63f-157">NOTES</span></span>

## <span data-ttu-id="9c63f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c63f-158">RELATED LINKS</span></span>
