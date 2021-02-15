---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114553"
---
# <span data-ttu-id="80a3d-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80a3d-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="80a3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80a3d-102">SYNOPSIS</span></span>

<span data-ttu-id="80a3d-103">Restaura os dados e a configuração de um item de Backup para o ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="80a3d-104">Os parâmetros necessários variam com o tipo de item de backup.</span><span class="sxs-lookup"><span data-stu-id="80a3d-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="80a3d-105">O mesmo comando é usado para restaurar máquinas virtuais do Azure, bancos de dados em execução em máquinas virtuais do Azure e compartilhamentos de arquivos do Azure também.</span><span class="sxs-lookup"><span data-stu-id="80a3d-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="80a3d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80a3d-106">SYNTAX</span></span>

### <span data-ttu-id="80a3d-107">AzureVMParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80a3d-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3d-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a3d-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3d-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="80a3d-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3d-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a3d-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3d-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a3d-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3d-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a3d-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a3d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="80a3d-113">DESCRIPTION</span></span>

<span data-ttu-id="80a3d-114">O cmdlet **Restore-AzRecoveryServicesBackupItem** restaura os dados e a configuração de um item de Backup do Azure para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="80a3d-115">**Para backup do VM do Azure**</span><span class="sxs-lookup"><span data-stu-id="80a3d-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="80a3d-116">Você pode fazer backup de máquinas virtuais do Azure e restaurar discos (gerenciados e não gerenciados) usando esse comando.</span><span class="sxs-lookup"><span data-stu-id="80a3d-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="80a3d-117">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="80a3d-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="80a3d-118">Se esse for um VM de disco gerenciado, um grupo de recursos de destino deverá ser especificado onde os discos restaurados serão mantidos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="80a3d-119">Quando o grupo de recursos de destino é especificado, se os instantâneos estão presentes no grupo de recursos especificado na política de backup, a operação de restauração será instantânea e os discos serão criados a partir de instantâneos locais e mantidos no grupo de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="80a3d-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="80a3d-120">Também há uma opção para restaurá-los como discos não gerenciados, mas isso aproveitará os dados presentes no cofre de serviços de recuperação do Azure e, portanto, ficará muito mais lento.</span><span class="sxs-lookup"><span data-stu-id="80a3d-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="80a3d-121">A configuração do VM e do modelo de implantação que pode ser usado para criar VM dos discos restaurados será baixada para a conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="80a3d-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="80a3d-122">Se esse for um VM de disco não gerenciado, os instantâneos estão presentes na conta de armazenamento original do disco e/ou no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="80a3d-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="80a3d-123">Se o usuário der uma opção para usar a conta de armazenamento original para restaurar, a restauração instantânea poderá ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="80a3d-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="80a3d-124">Caso contrário, os dados são buscados no cofre de serviços de Recuperação do Azure e os discos são criados em uma conta de armazenamento especificada, juntamente com a configuração do VM e do modelo de implantação.</span><span class="sxs-lookup"><span data-stu-id="80a3d-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80a3d-125">Por padrão, o backup do Azure VM fazer backup de todos os discos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="80a3d-126">Você pode fazer backup de discos relevantes seletivamente usando os parâmetros da Lista de exclusão ou da Lista de Inclusão durante o Enable-Backup.</span><span class="sxs-lookup"><span data-stu-id="80a3d-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="80a3d-127">A opção de restaurar seletivamente os discos só estará disponível se um deles tiver feito backup seletivo deles.</span><span class="sxs-lookup"><span data-stu-id="80a3d-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="80a3d-128">Consulte diferentes conjuntos de parâmetros possíveis e texto de parâmetro para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="80a3d-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="80a3d-129">Se o parâmetro -VaultId for usado, o parâmetro -VaultLocation também deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="80a3d-130">**Para backup de compartilhamento de arquivo do Azure**</span><span class="sxs-lookup"><span data-stu-id="80a3d-130">**For Azure File share backup**</span></span>

<span data-ttu-id="80a3d-131">Você pode restaurar um compartilhamento de arquivo inteiro ou arquivos/pastas específicos/múltiplos no compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="80a3d-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="80a3d-132">Você pode restaurar para o local original ou para um local alternativo.</span><span class="sxs-lookup"><span data-stu-id="80a3d-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="80a3d-133">**Para cargas de trabalho do Azure**</span><span class="sxs-lookup"><span data-stu-id="80a3d-133">**For Azure Workloads**</span></span>

<span data-ttu-id="80a3d-134">Você pode restaurar DBs SQL em VMs do Azure</span><span class="sxs-lookup"><span data-stu-id="80a3d-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="80a3d-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80a3d-135">EXAMPLES</span></span>

### <span data-ttu-id="80a3d-136">Exemplo 1: Restaurar os discos de um VM do Azure de disco gerenciado com backup de um determinado ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="80a3d-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="80a3d-137">O primeiro comando obtém o cofre dos Serviços de Recuperação e o armazena $vault variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="80a3d-138">O segundo comando obtém o item de Backup do tipo AzureVM, do nome "V2VM" e o armazena na variável $BackupItem dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="80a3d-139">O terceiro comando obtém a data de sete dias antes e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="80a3d-140">O quarto comando obtém a data atual e a armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="80a3d-141">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="80a3d-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="80a3d-142">O último comando restaura todos os discos para o grupo de recursos de destino Target_RG e fornece as informações de configuração do VM e o modelo de implantação na conta de armazenamento DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="80a3d-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="80a3d-143">Exemplo 2: Restaurar discos especificados de um VM de disco gerenciado com backup do Azure de um determinado ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="80a3d-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="80a3d-144">O primeiro comando obtém o cofre dos Serviços de Recuperação e o armazena $vault variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="80a3d-145">O segundo comando obtém o item de Backup do tipo AzureVM, do nome "V2VM" e o armazena na variável $BackupItem dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="80a3d-146">O terceiro comando obtém a data de sete dias antes e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="80a3d-147">O quarto comando obtém a data atual e a armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="80a3d-148">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="80a3d-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="80a3d-149">O sexto comando armazena a lista de discos a serem restaurados na variável RestoreDiskLUN.</span><span class="sxs-lookup"><span data-stu-id="80a3d-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="80a3d-150">O último comando restaura os discos determinados, dos LUNs especificados, para o grupo de recursos de destino Target_RG e, em seguida, fornece as informações de configuração do VM e o modelo de implantação na conta de armazenamento DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="80a3d-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="80a3d-151">Exemplo 3: Restaurar discos de um VM gerenciado como discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="80a3d-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="80a3d-152">O primeiro comando obtém o cofre RecoveryServices e o armazena $vault variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="80a3d-153">O segundo comando obtém o item backup e o armazena na variável $BackupItem dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="80a3d-154">O terceiro comando obtém a data de sete dias antes e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="80a3d-155">O quarto comando obtém a data atual e a armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="80a3d-156">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="80a3d-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="80a3d-157">O sexto comando restaura os discos como discos nãomanados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="80a3d-158">Exemplo 4: Restaurar um VM não gerenciamento como discos não gerenciamento usando a conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="80a3d-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="80a3d-159">O primeiro comando obtém o cofre RecoveryServices e o armazena $vault variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="80a3d-160">O segundo comando obtém o item backup e o armazena na variável $BackupItem dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="80a3d-161">O terceiro comando obtém a data de sete dias antes e a armazena na variável $StartDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="80a3d-162">O quarto comando obtém a data atual e a armazena na variável $EndDate dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="80a3d-163">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="80a3d-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="80a3d-164">O sexto comando restaura os discos como discos não gerenciamento para suas contas de armazenamento originais</span><span class="sxs-lookup"><span data-stu-id="80a3d-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="80a3d-165">Exemplo 5: Restaurar vários arquivos de um item do AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="80a3d-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="80a3d-166">O primeiro comando obtém o cofre dos Serviços de Recuperação e o armazena $vault variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="80a3d-167">O segundo comando obtém o item de Backup chamado fileshareitem e o armazena na variável $BackupItem dados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="80a3d-168">O terceiro comando obtém uma lista de pontos de recuperação para o item de backup específico.</span><span class="sxs-lookup"><span data-stu-id="80a3d-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="80a3d-169">O quarto comando especifica quais arquivos restaurar e armazená-los $files variável.</span><span class="sxs-lookup"><span data-stu-id="80a3d-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="80a3d-170">O último comando restaura os arquivos especificados em seu local original.</span><span class="sxs-lookup"><span data-stu-id="80a3d-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="80a3d-171">Exemplo 6: Restaurar um SQL DB em um VM do Azure para outro VM de destino para um ponto de recuperação completo distinto</span><span class="sxs-lookup"><span data-stu-id="80a3d-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="80a3d-172">Exemplo 7: Restaurar um SQL DB em um VM do Azure para outro VM de destino para um ponto de recuperação de log</span><span class="sxs-lookup"><span data-stu-id="80a3d-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="80a3d-173">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80a3d-173">PARAMETERS</span></span>

### <span data-ttu-id="80a3d-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a3d-174">-DefaultProfile</span></span>

<span data-ttu-id="80a3d-175">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="80a3d-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a3d-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="80a3d-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="80a3d-177">Usado para restaurar vários arquivos a partir de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="80a3d-178">Os caminhos dos itens a serem restaurados dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-178">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="80a3d-179">-RecoveryPoint</span></span>

<span data-ttu-id="80a3d-180">Especifica o ponto de recuperação para o qual restaurar o item de backup.</span><span class="sxs-lookup"><span data-stu-id="80a3d-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="80a3d-181">Para obter um **objeto AzureRmRecoveryServicesBackupRecoveryPoint,** use o cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint.**</span><span class="sxs-lookup"><span data-stu-id="80a3d-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="80a3d-182">-ResolveConflict</span></span>

<span data-ttu-id="80a3d-183">Caso o item restaurado também exista no destino, use-o para indicar se deve substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="80a3d-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="80a3d-184">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="80a3d-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80a3d-185">Substituir</span><span class="sxs-lookup"><span data-stu-id="80a3d-185">Overwrite</span></span>
- <span data-ttu-id="80a3d-186">Ignorar</span><span class="sxs-lookup"><span data-stu-id="80a3d-186">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="80a3d-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="80a3d-188">Use esta opção para especificar a restauração como discos nãomanados</span><span class="sxs-lookup"><span data-stu-id="80a3d-188">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="80a3d-189">-RestoreDiskList</span></span>
<span data-ttu-id="80a3d-190">Especificar quais discos recuperar do VM com backup</span><span class="sxs-lookup"><span data-stu-id="80a3d-190">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="80a3d-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="80a3d-192">Use esta opção para restaurar apenas os discos do sistema operacional de um VM com backup</span><span class="sxs-lookup"><span data-stu-id="80a3d-192">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="80a3d-193">-SourceFilePath</span></span>

<span data-ttu-id="80a3d-194">Usado para restaurar um item específico a partir de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="80a3d-195">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-195">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="80a3d-196">-SourceFileType</span></span>

<span data-ttu-id="80a3d-197">Usado para restaurar um item específico a partir de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="80a3d-198">O tipo do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="80a3d-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="80a3d-199">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="80a3d-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80a3d-200">Arquivo</span><span class="sxs-lookup"><span data-stu-id="80a3d-200">File</span></span>
- <span data-ttu-id="80a3d-201">Diretório</span><span class="sxs-lookup"><span data-stu-id="80a3d-201">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="80a3d-202">-StorageAccountName</span></span>

<span data-ttu-id="80a3d-203">Especifica o nome da conta de armazenamento de destino em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="80a3d-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="80a3d-204">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="80a3d-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a3d-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="80a3d-206">Especifica o nome do grupo de recursos que contém a conta de Armazenamento de destino em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="80a3d-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="80a3d-207">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="80a3d-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="80a3d-208">-TargetFileShareName</span></span>

<span data-ttu-id="80a3d-209">O Compartilhamento de Arquivo para o qual o compartilhamento de arquivos deve ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-209">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="80a3d-210">-TargetFolder</span></span>

<span data-ttu-id="80a3d-211">A pasta na qual o compartilhamento de arquivos deve ser restaurada no TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="80a3d-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="80a3d-212">Se o conteúdo em backup for restaurado para uma pasta raiz, dê os valores da pasta de destino como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="80a3d-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a3d-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="80a3d-214">O grupo de recursos ao qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="80a3d-215">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="80a3d-215">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="80a3d-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="80a3d-217">A conta de armazenamento para a qual o compartilhamento de arquivos deve ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-217">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="80a3d-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="80a3d-219">Use essa opção se os discos do ponto de recuperação devem ser restaurados para suas contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="80a3d-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="80a3d-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="80a3d-221">A ID de DES para criptografar os discos restaurados.</span><span class="sxs-lookup"><span data-stu-id="80a3d-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="80a3d-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="80a3d-223">Use essa opção para acionar a restauração entre regiões para a região secundária.</span><span class="sxs-lookup"><span data-stu-id="80a3d-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="80a3d-224">-VaultId</span></span>

<span data-ttu-id="80a3d-225">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="80a3d-225">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="80a3d-226">-VaultLocation</span></span>

<span data-ttu-id="80a3d-227">Local do Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="80a3d-227">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="80a3d-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="80a3d-229">Configuração de recuperação</span><span class="sxs-lookup"><span data-stu-id="80a3d-229">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a3d-230">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="80a3d-230">-Confirm</span></span>

<span data-ttu-id="80a3d-231">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a3d-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a3d-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a3d-232">-WhatIf</span></span>

<span data-ttu-id="80a3d-233">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="80a3d-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="80a3d-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a3d-234">CommonParameters</span></span>
<span data-ttu-id="80a3d-235">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a3d-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a3d-236">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a3d-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a3d-237">Entradas</span><span class="sxs-lookup"><span data-stu-id="80a3d-237">INPUTS</span></span>

### <span data-ttu-id="80a3d-238">System.String</span><span class="sxs-lookup"><span data-stu-id="80a3d-238">System.String</span></span>

### <span data-ttu-id="80a3d-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="80a3d-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="80a3d-240">Saídas</span><span class="sxs-lookup"><span data-stu-id="80a3d-240">OUTPUTS</span></span>

### <span data-ttu-id="80a3d-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="80a3d-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="80a3d-242">Notas</span><span class="sxs-lookup"><span data-stu-id="80a3d-242">NOTES</span></span>

## <span data-ttu-id="80a3d-243">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80a3d-243">RELATED LINKS</span></span>

[<span data-ttu-id="80a3d-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80a3d-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="80a3d-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80a3d-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="80a3d-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="80a3d-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
