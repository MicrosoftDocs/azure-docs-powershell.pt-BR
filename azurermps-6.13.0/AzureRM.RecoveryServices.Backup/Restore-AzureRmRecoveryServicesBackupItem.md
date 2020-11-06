---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426306"
---
# <span data-ttu-id="8476e-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8476e-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8476e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8476e-102">SYNOPSIS</span></span>
<span data-ttu-id="8476e-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8476e-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8476e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8476e-104">SYNTAX</span></span>

### <span data-ttu-id="8476e-105">AzureVMParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8476e-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8476e-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8476e-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8476e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8476e-107">DESCRIPTION</span></span>
<span data-ttu-id="8476e-108">O cmdlet **Restore-AzureRmRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="8476e-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="8476e-109">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="8476e-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="8476e-110">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="8476e-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="8476e-111">Ele restaura os dados de disco e as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="8476e-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="8476e-112">Após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="8476e-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="8476e-113">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="8476e-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8476e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8476e-114">EXAMPLES</span></span>

### <span data-ttu-id="8476e-115">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="8476e-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8476e-116">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="8476e-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8476e-117">O segundo comando obtém o item de backup chamado V2VM de $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8476e-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8476e-118">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="8476e-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8476e-119">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8476e-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8476e-120">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="8476e-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="8476e-121">O intervalo de datas especificado é os últimos 7 dias.</span><span class="sxs-lookup"><span data-stu-id="8476e-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="8476e-122">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="8476e-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="8476e-123">OS</span><span class="sxs-lookup"><span data-stu-id="8476e-123">PARAMETERS</span></span>

### <span data-ttu-id="8476e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8476e-124">-DefaultProfile</span></span>
<span data-ttu-id="8476e-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8476e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8476e-126">-RecoveryPoint</span></span>
<span data-ttu-id="8476e-127">Especifica o ponto de recuperação no qual restaurar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8476e-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="8476e-128">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="8476e-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="8476e-129">-ResolveConflict</span></span>
<span data-ttu-id="8476e-130">Caso o item restaurado também exista no destino, use-o para indicar se deseja substituir ou não.</span><span class="sxs-lookup"><span data-stu-id="8476e-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="8476e-131">-SourceFilePath</span></span>
<span data-ttu-id="8476e-132">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8476e-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8476e-133">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8476e-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="8476e-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="8476e-134">-SourceFileType</span></span>
<span data-ttu-id="8476e-135">Usado para uma restauração de item específica de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8476e-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="8476e-136">O caminho do item a ser restaurado dentro do compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8476e-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8476e-137">-StorageAccountName</span></span>
<span data-ttu-id="8476e-138">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8476e-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="8476e-139">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8476e-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8476e-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="8476e-141">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="8476e-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="8476e-142">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8476e-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8476e-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="8476e-143">-TargetFileShareName</span></span>
<span data-ttu-id="8476e-144">O compartilhamento de arquivos ao qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8476e-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8476e-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="8476e-145">-TargetFolder</span></span>
<span data-ttu-id="8476e-146">A pasta na qual o compartilhamento de arquivos precisa ser restaurado dentro do targetFileShareName. deixe a variável vazia para restaurar na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="8476e-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="8476e-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8476e-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="8476e-148">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="8476e-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8476e-149">Aplicável ao backup de VM com discos gerenciados</span><span class="sxs-lookup"><span data-stu-id="8476e-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="8476e-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8476e-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="8476e-151">A conta de armazenamento à qual o compartilhamento de arquivos precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8476e-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="8476e-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8476e-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="8476e-153">Use esta opção se os discos do ponto de recuperação forem restaurados às contas de armazenamento originais.</span><span class="sxs-lookup"><span data-stu-id="8476e-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="8476e-154">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="8476e-154">-VaultId</span></span>
<span data-ttu-id="8476e-155">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8476e-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8476e-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="8476e-156">-VaultLocation</span></span>
<span data-ttu-id="8476e-157">Localização do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8476e-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8476e-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8476e-158">-Confirm</span></span>
<span data-ttu-id="8476e-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8476e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8476e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8476e-160">-WhatIf</span></span>
<span data-ttu-id="8476e-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8476e-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8476e-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8476e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8476e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8476e-163">CommonParameters</span></span>
<span data-ttu-id="8476e-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8476e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8476e-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8476e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8476e-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8476e-166">INPUTS</span></span>

### <span data-ttu-id="8476e-167">System. String</span><span class="sxs-lookup"><span data-stu-id="8476e-167">System.String</span></span>
<span data-ttu-id="8476e-168">Parâmetros: Vaultid (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8476e-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="8476e-169">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8476e-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="8476e-170">Parâmetros: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8476e-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="8476e-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8476e-171">OUTPUTS</span></span>

### <span data-ttu-id="8476e-172">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8476e-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8476e-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8476e-173">NOTES</span></span>

## <span data-ttu-id="8476e-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8476e-174">RELATED LINKS</span></span>

[<span data-ttu-id="8476e-175">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8476e-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="8476e-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8476e-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="8476e-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8476e-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


