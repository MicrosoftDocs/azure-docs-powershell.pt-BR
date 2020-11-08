---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114674"
---
# <span data-ttu-id="05169-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="05169-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="05169-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05169-102">SYNOPSIS</span></span>
<span data-ttu-id="05169-103">Cria um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="05169-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="05169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05169-104">SYNTAX</span></span>

### <span data-ttu-id="05169-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="05169-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05169-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05169-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05169-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05169-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05169-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05169-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05169-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05169-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05169-117">DESCRIPTION</span></span>
<span data-ttu-id="05169-118">O cmdlet **New-AzSynapseSqlPool** cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="05169-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="05169-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05169-119">EXAMPLES</span></span>

### <span data-ttu-id="05169-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05169-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="05169-121">Esse comando cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="05169-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="05169-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="05169-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="05169-123">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="05169-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="05169-124">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="05169-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="05169-125">Esse comando cria um pool SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="05169-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="05169-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="05169-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="05169-127">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool do SQL nesta assinatura com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="05169-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="05169-128">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="05169-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="05169-129">Esse comando cria um pool do SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="05169-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="05169-130">OS</span><span class="sxs-lookup"><span data-stu-id="05169-130">PARAMETERS</span></span>

### <span data-ttu-id="05169-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05169-131">-AsJob</span></span>
<span data-ttu-id="05169-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="05169-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05169-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05169-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="05169-134">O nome do grupo de recursos do objeto de pool do SQL bakcup para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="05169-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="05169-135">-BackupResourceId</span></span>
<span data-ttu-id="05169-136">O identificador de recurso do objeto de pool do SQL de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="05169-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="05169-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="05169-138">O nome do objeto de pool do SQL bakcup a ser criado.</span><span class="sxs-lookup"><span data-stu-id="05169-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="05169-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="05169-140">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="05169-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05169-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="05169-142">O nome do espaço de trabalho Synapse do objeto de pool SQL do bakcup a ser criado.</span><span class="sxs-lookup"><span data-stu-id="05169-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-143">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="05169-143">-Collation</span></span>
<span data-ttu-id="05169-144">O agrupamento define as regras que classificam e comparam dados, e não podem ser alterados após a criação do pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="05169-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="05169-145">O agrupamento padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="05169-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05169-146">-DefaultProfile</span></span>
<span data-ttu-id="05169-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05169-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05169-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="05169-148">-FromBackup</span></span>
<span data-ttu-id="05169-149">Indica a restauração do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="05169-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="05169-150">-FromRestorePoint</span></span>
<span data-ttu-id="05169-151">Indica a utilização de um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="05169-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="05169-152">-Name</span></span>
<span data-ttu-id="05169-153">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="05169-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="05169-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="05169-154">-PerformanceLevel</span></span>
<span data-ttu-id="05169-155">A camada de serviço SQL e o nível de desempenho a serem atribuídos ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="05169-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="05169-156">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="05169-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05169-157">-ResourceGroupName</span></span>
<span data-ttu-id="05169-158">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05169-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="05169-159">-RestorePoint</span></span>
<span data-ttu-id="05169-160">Tempo para restauração do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="05169-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05169-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="05169-162">O nome do grupo de recursos do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="05169-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="05169-163">-SourceResourceId</span></span>
<span data-ttu-id="05169-164">O identificador de recurso do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="05169-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="05169-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="05169-166">O nome do objeto de pool do SQL de origem para o qual criar.</span><span class="sxs-lookup"><span data-stu-id="05169-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="05169-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="05169-168">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="05169-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05169-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="05169-170">O nome do espaço de trabalho Synapse do objeto de pool SQL de origem para criar.</span><span class="sxs-lookup"><span data-stu-id="05169-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-171">-Marca</span><span class="sxs-lookup"><span data-stu-id="05169-171">-Tag</span></span>
<span data-ttu-id="05169-172">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="05169-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="05169-173">-Versão</span><span class="sxs-lookup"><span data-stu-id="05169-173">-Version</span></span>
<span data-ttu-id="05169-174">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="05169-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="05169-175">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="05169-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="05169-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05169-176">-WorkspaceName</span></span>
<span data-ttu-id="05169-177">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="05169-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05169-178">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="05169-178">-WorkspaceObject</span></span>
<span data-ttu-id="05169-179">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="05169-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05169-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05169-180">-Confirm</span></span>
<span data-ttu-id="05169-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05169-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05169-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05169-182">-WhatIf</span></span>
<span data-ttu-id="05169-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05169-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05169-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05169-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05169-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05169-185">CommonParameters</span></span>
<span data-ttu-id="05169-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05169-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05169-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05169-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05169-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05169-188">INPUTS</span></span>

### <span data-ttu-id="05169-189">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="05169-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="05169-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05169-190">OUTPUTS</span></span>

### <span data-ttu-id="05169-191">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="05169-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="05169-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05169-192">NOTES</span></span>

## <span data-ttu-id="05169-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05169-193">RELATED LINKS</span></span>
