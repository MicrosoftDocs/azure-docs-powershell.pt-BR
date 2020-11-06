---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432946"
---
# <span data-ttu-id="abf1d-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="abf1d-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="abf1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="abf1d-103">Restaura os dados e a configuração de um item de backup para um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="abf1d-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abf1d-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="abf1d-106">O cmdlet **Restore-AzureRmBackupItem** restaura os dados e a configuração de um item do Azure backup para um ponto de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="abf1d-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="abf1d-107">Esse cmdlet inicia a restauração do cofre de backup para a sua conta.</span><span class="sxs-lookup"><span data-stu-id="abf1d-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="abf1d-108">A operação de restauração não restaura a máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="abf1d-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="abf1d-109">Ele restaura os dados de disco e as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="abf1d-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="abf1d-110">Após a conclusão da operação de restauração, você deve criar a máquina virtual e iniciá-la.</span><span class="sxs-lookup"><span data-stu-id="abf1d-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="abf1d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abf1d-111">EXAMPLES</span></span>

### <span data-ttu-id="abf1d-112">Exemplo 1: restaurar uma máquina virtual para um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="abf1d-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="abf1d-113">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="abf1d-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="abf1d-114">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="abf1d-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="abf1d-115">O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="abf1d-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="abf1d-116">O comando armazena esse objeto na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="abf1d-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="abf1d-117">O terceiro comando obtém o item de backup no contêiner no $Container usando o cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="abf1d-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="abf1d-118">O comando armazena esse objeto na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="abf1d-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="abf1d-119">O quarto comando obtém o ponto de recuperação do item em $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="abf1d-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="abf1d-120">O comando armazena esse objeto na variável $RecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="abf1d-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="abf1d-121">O comando final restaura o ponto de recuperação no $RecoveryPoint para a conta chamada DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="abf1d-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="abf1d-122">OS</span><span class="sxs-lookup"><span data-stu-id="abf1d-122">PARAMETERS</span></span>

### <span data-ttu-id="abf1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-123">-DefaultProfile</span></span>
<span data-ttu-id="abf1d-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abf1d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf1d-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-125">-RecoveryPoint</span></span>
<span data-ttu-id="abf1d-126">Especifica o ponto de recuperação no qual restaurar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abf1d-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="abf1d-127">Para obter um **AzureRmBackupRecoveryPoint** , use o cmdlet Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="abf1d-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf1d-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="abf1d-128">-StorageAccountName</span></span>
<span data-ttu-id="abf1d-129">Especifica o nome da conta de armazenamento de destino na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="abf1d-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="abf1d-130">Como parte do processo de restauração, esse cmdlet armazena os discos e as informações de configuração nesta conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="abf1d-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf1d-131">CommonParameters</span></span>
<span data-ttu-id="abf1d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf1d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf1d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abf1d-134">INPUTS</span></span>

### <span data-ttu-id="abf1d-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="abf1d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abf1d-136">OUTPUTS</span></span>

### <span data-ttu-id="abf1d-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="abf1d-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="abf1d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abf1d-138">NOTES</span></span>

## <span data-ttu-id="abf1d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abf1d-139">RELATED LINKS</span></span>

[<span data-ttu-id="abf1d-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="abf1d-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="abf1d-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="abf1d-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="abf1d-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


