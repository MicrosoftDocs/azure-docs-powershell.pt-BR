---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772964"
---
# <span data-ttu-id="8e7d4-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e7d4-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8e7d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e7d4-102">SYNOPSIS</span></span>

<span data-ttu-id="8e7d4-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="8e7d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e7d4-104">SYNTAX</span></span>

### <span data-ttu-id="8e7d4-105">AzureVMParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e7d4-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7d4-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e7d4-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e7d4-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e7d4-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7d4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e7d4-108">DESCRIPTION</span></span>

<span data-ttu-id="8e7d4-109">O cmdlet **Restore-AzRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="8e7d4-110">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="8e7d4-111">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="8e7d4-112">Ele restaura os dados de disco e as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="8e7d4-113">Após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="8e7d4-114">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="8e7d4-115">Observação: para executar este cmdlet com êxito, o parâmetro de VaultLocation também deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="8e7d4-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e7d4-116">EXAMPLES</span></span>

### <span data-ttu-id="8e7d4-117">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="8e7d4-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8e7d4-118">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8e7d4-119">O segundo comando obtém o item de backup chamado V2VM de $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8e7d4-120">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8e7d4-121">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8e7d4-122">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8e7d4-123">O intervalo de datas especificado é os últimos 7 dias.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="8e7d4-124">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="8e7d4-125">OS</span><span class="sxs-lookup"><span data-stu-id="8e7d4-125">PARAMETERS</span></span>

### <span data-ttu-id="8e7d4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7d4-126">-DefaultProfile</span></span>

<span data-ttu-id="8e7d4-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7d4-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8e7d4-128">-RecoveryPoint</span></span>

<span data-ttu-id="8e7d4-129">Especifica o ponto de recuperação no qual restaurar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="8e7d4-130">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** .</span><span class="sxs-lookup"><span data-stu-id="8e7d4-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="8e7d4-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="8e7d4-131">-ResolveConflict</span></span>

<span data-ttu-id="8e7d4-132">Caso o item restaurado também exista no destino, use-o para indicar se deseja substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="8e7d4-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8e7d4-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7d4-134">Pelas</span><span class="sxs-lookup"><span data-stu-id="8e7d4-134">Overwrite</span></span>
- <span data-ttu-id="8e7d4-135">Siga</span><span class="sxs-lookup"><span data-stu-id="8e7d4-135">Skip</span></span>

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

### <span data-ttu-id="8e7d4-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8e7d4-136">-SourceFilePath</span></span>

<span data-ttu-id="8e7d4-137">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8e7d4-138">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="8e7d4-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="8e7d4-139">-SourceFileType</span></span>

<span data-ttu-id="8e7d4-140">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8e7d4-141">O tipo do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="8e7d4-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8e7d4-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7d4-143">Arquivos</span><span class="sxs-lookup"><span data-stu-id="8e7d4-143">File</span></span>
- <span data-ttu-id="8e7d4-144">Diretório</span><span class="sxs-lookup"><span data-stu-id="8e7d4-144">Directory</span></span>

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

### <span data-ttu-id="8e7d4-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e7d4-145">-StorageAccountName</span></span>

<span data-ttu-id="8e7d4-146">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="8e7d4-147">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8e7d4-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7d4-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="8e7d4-149">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="8e7d4-150">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="8e7d4-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="8e7d4-151">-TargetFileShareName</span></span>

<span data-ttu-id="8e7d4-152">O compartilhamento de arquivos ao qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8e7d4-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="8e7d4-153">-TargetFolder</span></span>

<span data-ttu-id="8e7d4-154">A pasta na qual o compartilhamento de arquivos precisa ser restaurado no TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="8e7d4-155">Se o conteúdo de backup for restaurado para uma pasta raiz, forneça os valores da pasta de destino como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="8e7d4-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7d4-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="8e7d4-157">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8e7d4-158">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="8e7d4-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="8e7d4-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e7d4-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="8e7d4-160">A conta de armazenamento à qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8e7d4-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e7d4-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="8e7d4-162">Use esta opção se os discos do ponto de recuperação forem restaurados às contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="8e7d4-163">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="8e7d4-163">-VaultId</span></span>

<span data-ttu-id="8e7d4-164">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8e7d4-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="8e7d4-165">-VaultLocation</span></span>

<span data-ttu-id="8e7d4-166">Localização do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8e7d4-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="8e7d4-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="8e7d4-168">Configuração de recuperação</span><span class="sxs-lookup"><span data-stu-id="8e7d4-168">Recovery config</span></span>

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

### <span data-ttu-id="8e7d4-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e7d4-169">-Confirm</span></span>

<span data-ttu-id="8e7d4-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7d4-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7d4-171">-WhatIf</span></span>

<span data-ttu-id="8e7d4-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e7d4-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7d4-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7d4-174">-CommonParameters</span></span>

<span data-ttu-id="8e7d4-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7d4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7d4-176">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e7d4-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7d4-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e7d4-177">INPUTS</span></span>

### <span data-ttu-id="8e7d4-178">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7d4-178">System.String</span></span>

### <span data-ttu-id="8e7d4-179">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8e7d4-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="8e7d4-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e7d4-180">OUTPUTS</span></span>

### <span data-ttu-id="8e7d4-181">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8e7d4-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8e7d4-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e7d4-182">NOTES</span></span>

## <span data-ttu-id="8e7d4-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e7d4-183">RELATED LINKS</span></span>

[<span data-ttu-id="8e7d4-184">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e7d4-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8e7d4-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8e7d4-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="8e7d4-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8e7d4-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)