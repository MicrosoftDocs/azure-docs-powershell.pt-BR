---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955314"
---
# <span data-ttu-id="4757a-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4757a-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4757a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4757a-102">SYNOPSIS</span></span>

<span data-ttu-id="4757a-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4757a-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="4757a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4757a-104">SYNTAX</span></span>

### <span data-ttu-id="4757a-105">AzureVMParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4757a-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4757a-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4757a-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4757a-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="4757a-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4757a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4757a-108">DESCRIPTION</span></span>

<span data-ttu-id="4757a-109">O cmdlet **Restore-AzRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="4757a-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="4757a-110">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="4757a-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="4757a-111">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="4757a-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="4757a-112">Ele restaura os discos gerenciados para um grupo de recursos de destino e informações de configuração para a conta de armazenamento do cliente após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="4757a-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="4757a-113">Para obter mais informações, Refter para diferentes conjuntos de parâmetros e texto de parâmetro possíveis.</span><span class="sxs-lookup"><span data-stu-id="4757a-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="4757a-114">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="4757a-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="4757a-115">Observação: para executar este cmdlet com êxito, o parâmetro de VaultLocation também deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="4757a-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="4757a-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4757a-116">EXAMPLES</span></span>

### <span data-ttu-id="4757a-117">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="4757a-117">Example 1: Restore an item to a recovery point</span></span>

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

<span data-ttu-id="4757a-118">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="4757a-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4757a-119">O segundo comando obtém o item de backup chamado V2VM de $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="4757a-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4757a-120">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="4757a-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="4757a-121">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4757a-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="4757a-122">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4757a-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="4757a-123">O intervalo de datas especificado é os últimos 7 dias.</span><span class="sxs-lookup"><span data-stu-id="4757a-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="4757a-124">O sétimo comando especifica quais discos são restaurados a partir do ponto de recuperação e os armazena em $restoreDiskLUNs variável.</span><span class="sxs-lookup"><span data-stu-id="4757a-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="4757a-125">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="4757a-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="4757a-126">Exemplo 2: restaurar vários arquivos de um item do AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4757a-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="4757a-127">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="4757a-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4757a-128">O segundo comando obtém o item de backup chamado fileshareitem e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="4757a-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="4757a-129">O terceiro comando obtém uma lista de pontos de recuperação para o item de backup específico.</span><span class="sxs-lookup"><span data-stu-id="4757a-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="4757a-130">O quarto comando spceifies quais arquivos restaurar e armazená-los em $files variável.</span><span class="sxs-lookup"><span data-stu-id="4757a-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="4757a-131">O último comando restaura os arquivos especificados para o local original.</span><span class="sxs-lookup"><span data-stu-id="4757a-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="4757a-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4757a-132">Example 3</span></span>

<span data-ttu-id="4757a-133">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4757a-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="4757a-134">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="4757a-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="4757a-135">OS</span><span class="sxs-lookup"><span data-stu-id="4757a-135">PARAMETERS</span></span>

### <span data-ttu-id="4757a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4757a-136">-DefaultProfile</span></span>

<span data-ttu-id="4757a-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4757a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4757a-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="4757a-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="4757a-139">Usado para vários arquivos restaurados de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="4757a-140">Os caminhos dos itens a serem restaurados dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="4757a-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4757a-141">-RecoveryPoint</span></span>

<span data-ttu-id="4757a-142">Especifica o ponto de recuperação para o qual restaurar o item de backup.</span><span class="sxs-lookup"><span data-stu-id="4757a-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="4757a-143">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="4757a-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="4757a-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="4757a-144">-ResolveConflict</span></span>

<span data-ttu-id="4757a-145">Caso o item restaurado também exista no destino, use-o para indicar se deseja substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="4757a-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="4757a-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4757a-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4757a-147">Pelas</span><span class="sxs-lookup"><span data-stu-id="4757a-147">Overwrite</span></span>
- <span data-ttu-id="4757a-148">Siga</span><span class="sxs-lookup"><span data-stu-id="4757a-148">Skip</span></span>

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

### <span data-ttu-id="4757a-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="4757a-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="4757a-150">Use essa opção para especificar a restauração como discos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="4757a-150">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="4757a-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="4757a-151">-RestoreDiskList</span></span>
<span data-ttu-id="4757a-152">Especificar quais discos recuperar da VM com backup</span><span class="sxs-lookup"><span data-stu-id="4757a-152">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="4757a-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="4757a-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="4757a-154">Use essa opção para restaurar somente OS discos de so de uma VM com backup</span><span class="sxs-lookup"><span data-stu-id="4757a-154">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="4757a-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="4757a-155">-SourceFilePath</span></span>

<span data-ttu-id="4757a-156">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="4757a-157">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="4757a-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="4757a-158">-SourceFileType</span></span>

<span data-ttu-id="4757a-159">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="4757a-160">O tipo do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4757a-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="4757a-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4757a-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4757a-162">Arquivos</span><span class="sxs-lookup"><span data-stu-id="4757a-162">File</span></span>
- <span data-ttu-id="4757a-163">Diretório</span><span class="sxs-lookup"><span data-stu-id="4757a-163">Directory</span></span>

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

### <span data-ttu-id="4757a-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4757a-164">-StorageAccountName</span></span>

<span data-ttu-id="4757a-165">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4757a-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="4757a-166">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4757a-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="4757a-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4757a-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="4757a-168">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4757a-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="4757a-169">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4757a-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="4757a-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="4757a-170">-TargetFileShareName</span></span>

<span data-ttu-id="4757a-171">O compartilhamento de arquivos ao qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="4757a-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="4757a-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="4757a-172">-TargetFolder</span></span>

<span data-ttu-id="4757a-173">A pasta na qual o compartilhamento de arquivos precisa ser restaurado no TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="4757a-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="4757a-174">Se o conteúdo de backup for restaurado para uma pasta raiz, forneça os valores da pasta de destino como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4757a-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="4757a-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4757a-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="4757a-176">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="4757a-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="4757a-177">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="4757a-177">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="4757a-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4757a-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="4757a-179">A conta de armazenamento à qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="4757a-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="4757a-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4757a-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="4757a-181">Use esta opção se os discos do ponto de recuperação forem restaurados às contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="4757a-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="4757a-182">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="4757a-182">-VaultId</span></span>

<span data-ttu-id="4757a-183">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4757a-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4757a-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="4757a-184">-VaultLocation</span></span>

<span data-ttu-id="4757a-185">Localização do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4757a-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4757a-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="4757a-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="4757a-187">Configuração de recuperação</span><span class="sxs-lookup"><span data-stu-id="4757a-187">Recovery config</span></span>

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

### <span data-ttu-id="4757a-188">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4757a-188">-Confirm</span></span>

<span data-ttu-id="4757a-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4757a-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4757a-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4757a-190">-WhatIf</span></span>

<span data-ttu-id="4757a-191">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4757a-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="4757a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4757a-192">CommonParameters</span></span>
<span data-ttu-id="4757a-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4757a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4757a-194">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4757a-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4757a-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4757a-195">INPUTS</span></span>

### <span data-ttu-id="4757a-196">System. String</span><span class="sxs-lookup"><span data-stu-id="4757a-196">System.String</span></span>

### <span data-ttu-id="4757a-197">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4757a-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="4757a-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4757a-198">OUTPUTS</span></span>

### <span data-ttu-id="4757a-199">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4757a-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4757a-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4757a-200">NOTES</span></span>

## <span data-ttu-id="4757a-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4757a-201">RELATED LINKS</span></span>

[<span data-ttu-id="4757a-202">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4757a-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4757a-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4757a-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4757a-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4757a-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
