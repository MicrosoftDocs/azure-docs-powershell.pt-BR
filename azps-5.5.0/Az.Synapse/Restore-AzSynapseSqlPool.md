---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112389"
---
# <span data-ttu-id="bab4c-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bab4c-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="bab4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bab4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bab4c-103">Restaura um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bab4c-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bab4c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bab4c-104">SYNTAX</span></span>

### <span data-ttu-id="bab4c-105">RestaurarFromBackupIdByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bab4c-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bab4c-106">RestaurarFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bab4c-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bab4c-107">RestaurarFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bab4c-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bab4c-108">RestaurarFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bab4c-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab4c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bab4c-109">DESCRIPTION</span></span>
<span data-ttu-id="bab4c-110">O cmdlet **Restore-AzSynapseSqlPool** restaura um pool SQL do Azure Synapse Analytics a partir de um backup ou um ponto de restauração de qualquer pool SQL.</span><span class="sxs-lookup"><span data-stu-id="bab4c-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="bab4c-111">O pool SQL restaurado é criado como um novo pool SQL.</span><span class="sxs-lookup"><span data-stu-id="bab4c-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="bab4c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bab4c-112">EXAMPLES</span></span>

### <span data-ttu-id="bab4c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bab4c-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="bab4c-114">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="bab4c-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="bab4c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bab4c-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="bab4c-116">Esse comando cria um pool SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="bab4c-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="bab4c-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bab4c-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="bab4c-118">Esse comando cria um pool SQL do Azure Synapse Analytics restaurando a partir do backup mais recente de qualquer pool SQL nesta assinatura com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bab4c-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="bab4c-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bab4c-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="bab4c-120">Esse comando cria um pool SQL do Azure Synapse Analytics aproveitando um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bab4c-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="bab4c-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bab4c-121">PARAMETERS</span></span>

### <span data-ttu-id="bab4c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bab4c-122">-AsJob</span></span>
<span data-ttu-id="bab4c-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bab4c-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bab4c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab4c-124">-DefaultProfile</span></span>
<span data-ttu-id="bab4c-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bab4c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bab4c-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="bab4c-126">-FromBackup</span></span>
<span data-ttu-id="bab4c-127">Indica a restauração do backup mais recente de qualquer pool SQL nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="bab4c-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="bab4c-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="bab4c-128">-FromRestorePoint</span></span>
<span data-ttu-id="bab4c-129">Indica aproveitar um ponto de restauração de qualquer pool SQL nesta assinatura para recuperar ou copiar de um estado anterior.</span><span class="sxs-lookup"><span data-stu-id="bab4c-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="bab4c-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="bab4c-130">-Name</span></span>
<span data-ttu-id="bab4c-131">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="bab4c-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="bab4c-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="bab4c-132">-PerformanceLevel</span></span>
<span data-ttu-id="bab4c-133">O nível de desempenho e o nível de desempenho do SQL Service a ser atribuído ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="bab4c-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="bab4c-134">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="bab4c-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="bab4c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab4c-135">-ResourceGroupName</span></span>
<span data-ttu-id="bab4c-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bab4c-136">Resource group name.</span></span>

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

### <span data-ttu-id="bab4c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bab4c-137">-ResourceId</span></span>
<span data-ttu-id="bab4c-138">A ID de recurso do banco de dados a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="bab4c-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="bab4c-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="bab4c-139">-RestorePoint</span></span>
<span data-ttu-id="bab4c-140">Tempo do instantâneo para restaurar.</span><span class="sxs-lookup"><span data-stu-id="bab4c-140">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="bab4c-141">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="bab4c-141">-WorkspaceName</span></span>
<span data-ttu-id="bab4c-142">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="bab4c-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bab4c-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bab4c-143">-WorkspaceObject</span></span>
<span data-ttu-id="bab4c-144">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bab4c-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bab4c-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bab4c-145">-Confirm</span></span>
<span data-ttu-id="bab4c-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab4c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bab4c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab4c-147">-WhatIf</span></span>
<span data-ttu-id="bab4c-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bab4c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bab4c-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bab4c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bab4c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab4c-150">CommonParameters</span></span>
<span data-ttu-id="bab4c-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab4c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab4c-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bab4c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab4c-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="bab4c-153">INPUTS</span></span>

### <span data-ttu-id="bab4c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bab4c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bab4c-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="bab4c-155">OUTPUTS</span></span>

### <span data-ttu-id="bab4c-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bab4c-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bab4c-157">Notas</span><span class="sxs-lookup"><span data-stu-id="bab4c-157">NOTES</span></span>

## <span data-ttu-id="bab4c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bab4c-158">RELATED LINKS</span></span>
