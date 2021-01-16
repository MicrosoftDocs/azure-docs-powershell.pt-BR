---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258342"
---
# <span data-ttu-id="d8dda-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8dda-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d8dda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8dda-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dda-103">Restaura um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8dda-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d8dda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8dda-104">SYNTAX</span></span>

### <span data-ttu-id="d8dda-105">RestoreFromBackupIdByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8dda-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dda-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dda-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dda-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dda-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dda-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dda-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dda-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dda-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dda-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dda-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8dda-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8dda-115">DESCRIPTION</span></span>
<span data-ttu-id="d8dda-116">O cmdlet **Restore-AzSynapseSqlPool** restaura um pool do SQL Synapse Analytics do Azure de um ponto de backup ou um ponto de restauração de qualquer pool SQL.</span><span class="sxs-lookup"><span data-stu-id="d8dda-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="d8dda-117">O pool SQL restaurado é criado como um novo pool SQL.</span><span class="sxs-lookup"><span data-stu-id="d8dda-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="d8dda-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8dda-118">EXAMPLES</span></span>

### <span data-ttu-id="d8dda-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8dda-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="d8dda-120">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8dda-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="d8dda-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d8dda-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="d8dda-122">Esse comando cria um pool SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="d8dda-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="d8dda-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d8dda-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="d8dda-124">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool do SQL nesta assinatura com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8dda-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="d8dda-125">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d8dda-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="d8dda-126">Esse comando cria um pool do SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8dda-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="d8dda-127">OS</span><span class="sxs-lookup"><span data-stu-id="d8dda-127">PARAMETERS</span></span>

### <span data-ttu-id="d8dda-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8dda-128">-AsJob</span></span>
<span data-ttu-id="d8dda-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d8dda-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8dda-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dda-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="d8dda-131">O nome do grupo de recursos do objeto de pool do SQL bakcup para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="d8dda-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dda-132">-BackupResourceId</span></span>
<span data-ttu-id="d8dda-133">O identificador de recurso do objeto de pool do SQL de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="d8dda-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="d8dda-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="d8dda-135">O nome do objeto de pool do SQL bakcup a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d8dda-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="d8dda-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="d8dda-137">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dda-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8dda-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="d8dda-139">O nome do espaço de trabalho Synapse do objeto de pool SQL do bakcup a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d8dda-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dda-140">-DefaultProfile</span></span>
<span data-ttu-id="d8dda-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8dda-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dda-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="d8dda-142">-FromBackup</span></span>
<span data-ttu-id="d8dda-143">Indica a restauração do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8dda-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d8dda-144">-FromRestorePoint</span></span>
<span data-ttu-id="d8dda-145">Indica a utilização de um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="d8dda-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8dda-146">-Name</span></span>
<span data-ttu-id="d8dda-147">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8dda-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d8dda-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="d8dda-148">-PerformanceLevel</span></span>
<span data-ttu-id="d8dda-149">A camada de serviço SQL e o nível de desempenho a serem atribuídos ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="d8dda-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="d8dda-150">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="d8dda-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dda-151">-ResourceGroupName</span></span>
<span data-ttu-id="d8dda-152">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="d8dda-153">-RestorePoint</span></span>
<span data-ttu-id="d8dda-154">Tempo para restauração do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="d8dda-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dda-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="d8dda-156">O nome do grupo de recursos do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="d8dda-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d8dda-157">-SourceResourceId</span></span>
<span data-ttu-id="d8dda-158">O identificador de recurso do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="d8dda-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="d8dda-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="d8dda-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="d8dda-160">O nome do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="d8dda-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="d8dda-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="d8dda-162">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dda-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8dda-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="d8dda-164">O nome do espaço de trabalho Synapse do objeto de pool SQL de origem para criar.</span><span class="sxs-lookup"><span data-stu-id="d8dda-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-165">-Marca</span><span class="sxs-lookup"><span data-stu-id="d8dda-165">-Tag</span></span>
<span data-ttu-id="d8dda-166">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="d8dda-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="d8dda-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8dda-167">-WorkspaceName</span></span>
<span data-ttu-id="d8dda-168">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8dda-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-169">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="d8dda-169">-WorkspaceObject</span></span>
<span data-ttu-id="d8dda-170">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8dda-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dda-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8dda-171">-Confirm</span></span>
<span data-ttu-id="d8dda-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8dda-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dda-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8dda-173">-WhatIf</span></span>
<span data-ttu-id="d8dda-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8dda-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8dda-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8dda-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dda-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dda-176">CommonParameters</span></span>
<span data-ttu-id="d8dda-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dda-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dda-178">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8dda-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dda-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8dda-179">INPUTS</span></span>

### <span data-ttu-id="d8dda-180">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8dda-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d8dda-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8dda-181">OUTPUTS</span></span>

### <span data-ttu-id="d8dda-182">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8dda-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d8dda-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8dda-183">NOTES</span></span>

## <span data-ttu-id="d8dda-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8dda-184">RELATED LINKS</span></span>
