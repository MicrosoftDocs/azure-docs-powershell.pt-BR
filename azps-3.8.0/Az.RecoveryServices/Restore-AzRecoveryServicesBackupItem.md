---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943533"
---
# <span data-ttu-id="a2ff4-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a2ff4-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a2ff4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2ff4-102">SYNOPSIS</span></span>

<span data-ttu-id="a2ff4-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="a2ff4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2ff4-104">SYNTAX</span></span>

### <span data-ttu-id="a2ff4-105">AzureVMParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2ff4-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ff4-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ff4-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ff4-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ff4-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ff4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2ff4-108">DESCRIPTION</span></span>

<span data-ttu-id="a2ff4-109">O cmdlet **Restore-AzRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="a2ff4-110">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="a2ff4-111">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="a2ff4-112">Ele restaura os discos gerenciados para um grupo de recursos de destino e informações de configuração para a conta de armazenamento do cliente após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="a2ff4-113">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="a2ff4-114">Observação: para executar este cmdlet com êxito, o parâmetro de VaultLocation também deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="a2ff4-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2ff4-115">EXAMPLES</span></span>

### <span data-ttu-id="a2ff4-116">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="a2ff4-116">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="a2ff4-117">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a2ff4-118">O segundo comando obtém o item de backup chamado V2VM de $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a2ff4-119">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="a2ff4-120">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="a2ff4-121">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="a2ff4-122">O intervalo de datas especificado é os últimos 7 dias.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="a2ff4-123">O sétimo comando especifica quais discos são restaurados a partir do ponto de recuperação e os armazena em $restoreDiskLUNs variável.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="a2ff4-124">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="a2ff4-125">Exemplo 2: restaurar vários arquivos de um item do AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a2ff4-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="a2ff4-126">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a2ff4-127">O segundo comando obtém o item de backup chamado fileshareitem e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="a2ff4-128">O terceiro comando obtém uma lista de pontos de recuperação para o item de backup específico.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="a2ff4-129">O quarto comando spceifies quais arquivos restaurar e armazená-los em $files variável.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="a2ff4-130">O último comando restaura os arquivos especificados para o local original.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="a2ff4-131">OS</span><span class="sxs-lookup"><span data-stu-id="a2ff4-131">PARAMETERS</span></span>

### <span data-ttu-id="a2ff4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ff4-132">-DefaultProfile</span></span>

<span data-ttu-id="a2ff4-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2ff4-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a2ff4-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="a2ff4-135">Usado para vários arquivos restaurados de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="a2ff4-136">Os caminhos dos itens a serem restaurados dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="a2ff4-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a2ff4-137">-RecoveryPoint</span></span>

<span data-ttu-id="a2ff4-138">Especifica o ponto de recuperação no qual restaurar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="a2ff4-139">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="a2ff4-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="a2ff4-140">-ResolveConflict</span></span>

<span data-ttu-id="a2ff4-141">Caso o item restaurado também exista no destino, use-o para indicar se deseja substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="a2ff4-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a2ff4-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2ff4-143">Pelas</span><span class="sxs-lookup"><span data-stu-id="a2ff4-143">Overwrite</span></span>
- <span data-ttu-id="a2ff4-144">Siga</span><span class="sxs-lookup"><span data-stu-id="a2ff4-144">Skip</span></span>

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

### <span data-ttu-id="a2ff4-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="a2ff4-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="a2ff4-146">Use essa opção para especificar a restauração como discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="a2ff4-146">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="a2ff4-147">-RestoreDiskList</span></span>
<span data-ttu-id="a2ff4-148">Especificar quais discos recuperar da VM com backup</span><span class="sxs-lookup"><span data-stu-id="a2ff4-148">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="a2ff4-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="a2ff4-150">Use essa opção para restaurar somente OS discos de so de uma VM com backup</span><span class="sxs-lookup"><span data-stu-id="a2ff4-150">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="a2ff4-151">-SourceFilePath</span></span>

<span data-ttu-id="a2ff4-152">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a2ff4-153">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="a2ff4-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="a2ff4-154">-SourceFileType</span></span>

<span data-ttu-id="a2ff4-155">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="a2ff4-156">O tipo do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="a2ff4-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a2ff4-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2ff4-158">Arquivos</span><span class="sxs-lookup"><span data-stu-id="a2ff4-158">File</span></span>
- <span data-ttu-id="a2ff4-159">Diretório</span><span class="sxs-lookup"><span data-stu-id="a2ff4-159">Directory</span></span>

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

### <span data-ttu-id="a2ff4-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2ff4-160">-StorageAccountName</span></span>

<span data-ttu-id="a2ff4-161">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="a2ff4-162">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ff4-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="a2ff4-164">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="a2ff4-165">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="a2ff4-166">-TargetFileShareName</span></span>

<span data-ttu-id="a2ff4-167">O compartilhamento de arquivos ao qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a2ff4-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="a2ff4-168">-TargetFolder</span></span>

<span data-ttu-id="a2ff4-169">A pasta na qual o compartilhamento de arquivos precisa ser restaurado no TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="a2ff4-170">Se o conteúdo de backup for restaurado para uma pasta raiz, forneça os valores da pasta de destino como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="a2ff4-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ff4-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="a2ff4-172">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a2ff4-173">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="a2ff4-173">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2ff4-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="a2ff4-175">A conta de armazenamento à qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="a2ff4-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2ff4-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="a2ff4-177">Use esta opção se os discos do ponto de recuperação forem restaurados às contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff4-178">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="a2ff4-178">-VaultId</span></span>

<span data-ttu-id="a2ff4-179">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a2ff4-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="a2ff4-180">-VaultLocation</span></span>

<span data-ttu-id="a2ff4-181">Localização do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a2ff4-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="a2ff4-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="a2ff4-183">Configuração de recuperação</span><span class="sxs-lookup"><span data-stu-id="a2ff4-183">Recovery config</span></span>

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

### <span data-ttu-id="a2ff4-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2ff4-184">-Confirm</span></span>

<span data-ttu-id="a2ff4-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ff4-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ff4-186">-WhatIf</span></span>

<span data-ttu-id="a2ff4-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2ff4-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ff4-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ff4-189">CommonParameters</span></span>
<span data-ttu-id="a2ff4-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ff4-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ff4-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2ff4-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ff4-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2ff4-192">INPUTS</span></span>

### <span data-ttu-id="a2ff4-193">System. String</span><span class="sxs-lookup"><span data-stu-id="a2ff4-193">System.String</span></span>

### <span data-ttu-id="a2ff4-194">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a2ff4-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a2ff4-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2ff4-195">OUTPUTS</span></span>

### <span data-ttu-id="a2ff4-196">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a2ff4-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a2ff4-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2ff4-197">NOTES</span></span>

## <span data-ttu-id="a2ff4-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2ff4-198">RELATED LINKS</span></span>

[<span data-ttu-id="a2ff4-199">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a2ff4-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a2ff4-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a2ff4-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a2ff4-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a2ff4-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
