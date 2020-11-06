---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440579"
---
# <span data-ttu-id="10c22-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="10c22-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="10c22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10c22-102">SYNOPSIS</span></span>
<span data-ttu-id="10c22-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10c22-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10c22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10c22-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c22-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10c22-105">DESCRIPTION</span></span>
<span data-ttu-id="10c22-106">O cmdlet **Restore-AzureRmRecoveryServicesBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="10c22-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="10c22-107">Este cmdlet inicia a restauração do cofre de serviços de recuperação para a conta de armazenamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="10c22-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="10c22-108">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="10c22-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="10c22-109">Ele restaura os dados de disco e as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="10c22-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="10c22-110">Após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="10c22-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="10c22-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="10c22-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="10c22-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10c22-112">EXAMPLES</span></span>

### <span data-ttu-id="10c22-113">Exemplo 1: restaurar um item para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="10c22-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="10c22-114">O primeiro comando obtém o contêiner de backup do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="10c22-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="10c22-115">O segundo comando obtém o item de backup chamado V2VM de $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="10c22-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="10c22-116">O terceiro comando obtém a data de sete dias antes e, em seguida, armazena-o na variável $StartDate.</span><span class="sxs-lookup"><span data-stu-id="10c22-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="10c22-117">O quarto comando obtém a data atual e a armazena na variável $EndDate.</span><span class="sxs-lookup"><span data-stu-id="10c22-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="10c22-118">O quinto comando obtém uma lista de pontos de recuperação para o item de backup específico filtrado por $StartDate e $EndDate.</span><span class="sxs-lookup"><span data-stu-id="10c22-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="10c22-119">O intervalo de datas especificado é os últimos 7 dias.</span><span class="sxs-lookup"><span data-stu-id="10c22-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="10c22-120">O último comando restaura os discos para a conta de armazenamento de destino DestAccount no grupo de recursos DestRG.</span><span class="sxs-lookup"><span data-stu-id="10c22-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="10c22-121">OS</span><span class="sxs-lookup"><span data-stu-id="10c22-121">PARAMETERS</span></span>

### <span data-ttu-id="10c22-122">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10c22-122">-RecoveryPoint</span></span>
<span data-ttu-id="10c22-123">Especifica o ponto de recuperação no qual restaurar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="10c22-123">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="10c22-124">Para obter um objeto **AzureRmRecoveryServicesBackupRecoveryPoint** , use o cmdlet Get-AzureRmRecoveryServicesBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="10c22-124">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="10c22-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="10c22-125">-StorageAccountName</span></span>
<span data-ttu-id="10c22-126">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="10c22-126">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="10c22-127">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10c22-127">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="10c22-128">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c22-128">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="10c22-129">Especifica o nome do grupo de recursos que contém a conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="10c22-129">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="10c22-130">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10c22-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="10c22-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c22-131">-DefaultProfile</span></span>
<span data-ttu-id="10c22-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10c22-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c22-133">CommonParameters</span></span>
<span data-ttu-id="10c22-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c22-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c22-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c22-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10c22-136">INPUTS</span></span>

### <span data-ttu-id="10c22-137">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="10c22-137">RecoveryPointBase</span></span>
<span data-ttu-id="10c22-138">O parâmetro ' RecoveryPoint ' aceita o valor do tipo ' RecoveryPointBase ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="10c22-138">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="10c22-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10c22-139">OUTPUTS</span></span>

### <span data-ttu-id="10c22-140">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="10c22-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="10c22-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10c22-141">NOTES</span></span>

## <span data-ttu-id="10c22-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10c22-142">RELATED LINKS</span></span>

[<span data-ttu-id="10c22-143">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="10c22-143">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="10c22-144">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="10c22-144">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="10c22-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="10c22-145">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


