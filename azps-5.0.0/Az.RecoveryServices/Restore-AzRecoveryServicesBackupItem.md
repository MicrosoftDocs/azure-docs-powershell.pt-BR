---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117212"
---
# <span data-ttu-id="8341c-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8341c-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8341c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8341c-102">SYNOPSIS</span></span>

<span data-ttu-id="8341c-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8341c-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="8341c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8341c-104">SYNTAX</span></span>

### <span data-ttu-id="8341c-105">AzureVMParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8341c-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8341c-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8341c-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8341c-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="8341c-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8341c-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="8341c-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8341c-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="8341c-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8341c-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="8341c-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8341c-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8341c-111">DESCRIPTION</span></span>

<span data-ttu-id="8341c-112">O cmdlet **Restore-AzRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="8341c-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="8341c-113">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="8341c-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="8341c-114">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="8341c-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="8341c-115">Ele restaura os discos gerenciados para um grupo de recursos de destino e informações de configuração para a conta de armazenamento do cliente após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="8341c-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="8341c-116">Para obter mais informações, Refter para diferentes conjuntos de parâmetros e texto de parâmetro possíveis.</span><span class="sxs-lookup"><span data-stu-id="8341c-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="8341c-117">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="8341c-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="8341c-118">Observação: para executar este cmdlet com êxito, o parâmetro de VaultLocation também deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="8341c-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="8341c-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8341c-119">EXAMPLES</span></span>

### <span data-ttu-id="8341c-120">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="8341c-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8341c-121">O primeiro comando obtém o cofre Recoveryservices e o armazena em $vault variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8341c-122">O segundo comando obtém os itens de backup e, em seguida, armazena-os na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8341c-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8341c-123">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8341c-124">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8341c-125">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8341c-126">O sexto comando especifica quais discos a serem restaurados do ponto de recuperação e os armazena em $restoreDiskLUNs variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="8341c-127">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="8341c-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="8341c-128">Exemplo 2: restaurar vários arquivos de um item do AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="8341c-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8341c-129">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="8341c-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8341c-130">O segundo comando obtém o item de backup chamado fileshareitem e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8341c-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8341c-131">O terceiro comando obtém uma lista de pontos de recuperação para o item de backup específico.</span><span class="sxs-lookup"><span data-stu-id="8341c-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="8341c-132">O quarto comando spceifies quais arquivos restaurar e armazená-los em $files variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="8341c-133">O último comando restaura os arquivos especificados para o local original.</span><span class="sxs-lookup"><span data-stu-id="8341c-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="8341c-134">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8341c-134">Example 3</span></span>

<span data-ttu-id="8341c-135">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8341c-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="8341c-136">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="8341c-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="8341c-137">Exemplo 4: restaurar uma VM gerenciada como discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="8341c-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8341c-138">O primeiro comando obtém o cofre Recoveryservices e o armazena em $vault variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8341c-139">O segundo comando obtém o item de backup e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8341c-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8341c-140">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8341c-141">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8341c-142">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8341c-143">O sexto comando restaura os discos como discos gerenciados com o grupo de recursos de destino fornecido.</span><span class="sxs-lookup"><span data-stu-id="8341c-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="8341c-144">Exemplo 5: restaurar uma VM gerenciada como discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="8341c-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8341c-145">O primeiro comando obtém o cofre Recoveryservices e o armazena em $vault variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8341c-146">O segundo comando obtém o item de backup e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8341c-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8341c-147">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8341c-148">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8341c-149">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8341c-150">O sexto comando restaura os discos como discos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="8341c-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="8341c-151">Exemplo 6: restaurar uma VM não gerenciada como discos não gerenciados usando a conta de armazenamento original.</span><span class="sxs-lookup"><span data-stu-id="8341c-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8341c-152">O primeiro comando obtém o cofre Recoveryservices e o armazena em $vault variável.</span><span class="sxs-lookup"><span data-stu-id="8341c-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="8341c-153">O segundo comando obtém o item de backup e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8341c-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8341c-154">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8341c-155">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8341c-156">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8341c-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8341c-157">O sexto comando restaura os discos como discos não gerenciados usando a conta de armazenamento original da VM.</span><span class="sxs-lookup"><span data-stu-id="8341c-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="8341c-158">OS</span><span class="sxs-lookup"><span data-stu-id="8341c-158">PARAMETERS</span></span>

### <span data-ttu-id="8341c-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8341c-159">-DefaultProfile</span></span>

<span data-ttu-id="8341c-160">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8341c-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8341c-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8341c-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="8341c-162">Usado para vários arquivos restaurados de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="8341c-163">Os caminhos dos itens a serem restaurados dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="8341c-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8341c-164">-RecoveryPoint</span></span>

<span data-ttu-id="8341c-165">Especifica o ponto de recuperação para o qual restaurar o item de backup.</span><span class="sxs-lookup"><span data-stu-id="8341c-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="8341c-166">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="8341c-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="8341c-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="8341c-167">-ResolveConflict</span></span>

<span data-ttu-id="8341c-168">Caso o item restaurado também exista no destino, use-o para indicar se deseja substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="8341c-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="8341c-169">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8341c-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8341c-170">Pelas</span><span class="sxs-lookup"><span data-stu-id="8341c-170">Overwrite</span></span>
- <span data-ttu-id="8341c-171">Siga</span><span class="sxs-lookup"><span data-stu-id="8341c-171">Skip</span></span>

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

### <span data-ttu-id="8341c-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="8341c-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="8341c-173">Use essa opção para especificar a restauração como discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="8341c-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="8341c-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="8341c-174">-RestoreDiskList</span></span>
<span data-ttu-id="8341c-175">Especificar quais discos recuperar da VM com backup</span><span class="sxs-lookup"><span data-stu-id="8341c-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="8341c-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="8341c-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="8341c-177">Use essa opção para restaurar somente OS discos de so de uma VM com backup</span><span class="sxs-lookup"><span data-stu-id="8341c-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="8341c-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8341c-178">-SourceFilePath</span></span>

<span data-ttu-id="8341c-179">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8341c-180">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="8341c-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="8341c-181">-SourceFileType</span></span>

<span data-ttu-id="8341c-182">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8341c-183">O tipo do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8341c-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="8341c-184">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8341c-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8341c-185">Arquivos</span><span class="sxs-lookup"><span data-stu-id="8341c-185">File</span></span>
- <span data-ttu-id="8341c-186">Diretório</span><span class="sxs-lookup"><span data-stu-id="8341c-186">Directory</span></span>

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

### <span data-ttu-id="8341c-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8341c-187">-StorageAccountName</span></span>

<span data-ttu-id="8341c-188">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8341c-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="8341c-189">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8341c-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8341c-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8341c-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="8341c-191">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8341c-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="8341c-192">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8341c-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8341c-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="8341c-193">-TargetFileShareName</span></span>

<span data-ttu-id="8341c-194">O compartilhamento de arquivos ao qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8341c-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8341c-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="8341c-195">-TargetFolder</span></span>

<span data-ttu-id="8341c-196">A pasta na qual o compartilhamento de arquivos precisa ser restaurado no TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="8341c-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="8341c-197">Se o conteúdo de backup for restaurado para uma pasta raiz, forneça os valores da pasta de destino como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="8341c-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="8341c-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8341c-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="8341c-199">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="8341c-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8341c-200">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="8341c-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="8341c-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8341c-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="8341c-202">A conta de armazenamento à qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8341c-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8341c-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8341c-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="8341c-204">Use esta opção se os discos do ponto de recuperação forem restaurados às contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="8341c-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="8341c-205">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="8341c-205">-VaultId</span></span>

<span data-ttu-id="8341c-206">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8341c-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8341c-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="8341c-207">-VaultLocation</span></span>

<span data-ttu-id="8341c-208">Localização do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8341c-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8341c-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="8341c-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="8341c-210">Configuração de recuperação</span><span class="sxs-lookup"><span data-stu-id="8341c-210">Recovery config</span></span>

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

### <span data-ttu-id="8341c-211">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8341c-211">-Confirm</span></span>

<span data-ttu-id="8341c-212">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8341c-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8341c-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8341c-213">-WhatIf</span></span>

<span data-ttu-id="8341c-214">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8341c-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="8341c-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8341c-215">CommonParameters</span></span>
<span data-ttu-id="8341c-216">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8341c-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8341c-217">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8341c-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8341c-218">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8341c-218">INPUTS</span></span>

### <span data-ttu-id="8341c-219">System. String</span><span class="sxs-lookup"><span data-stu-id="8341c-219">System.String</span></span>

### <span data-ttu-id="8341c-220">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8341c-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="8341c-221">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8341c-221">OUTPUTS</span></span>

### <span data-ttu-id="8341c-222">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8341c-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8341c-223">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8341c-223">NOTES</span></span>

## <span data-ttu-id="8341c-224">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8341c-224">RELATED LINKS</span></span>

[<span data-ttu-id="8341c-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8341c-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8341c-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8341c-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8341c-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8341c-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
