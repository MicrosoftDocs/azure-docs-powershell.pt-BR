---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954725"
---
# <span data-ttu-id="789b4-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="789b4-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="789b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="789b4-102">SYNOPSIS</span></span>
<span data-ttu-id="789b4-103">Cria um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados.</span><span class="sxs-lookup"><span data-stu-id="789b4-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="789b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="789b4-104">SYNTAX</span></span>

### <span data-ttu-id="789b4-105">AzureToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="789b4-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="789b4-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="789b4-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="789b4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="789b4-107">DESCRIPTION</span></span>
<span data-ttu-id="789b4-108">Cria um objeto de mapeamento de disco que mapeia um disco da máquina virtual do Azure para a conta de armazenamento do cache e a conta de armazenamento de destino (região de recuperação) a ser usada para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="789b4-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="789b4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="789b4-109">EXAMPLES</span></span>

### <span data-ttu-id="789b4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="789b4-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="789b4-111">Crie um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados. Usado durante o Azure to Azure EnableDer e para proteger novamente a operação.</span><span class="sxs-lookup"><span data-stu-id="789b4-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="789b4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="789b4-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="789b4-113">Crie um objeto de mapeamento de disco gerenciado para discos de máquina virtual do Azure serem replicados. Usado durante o Azure to Azure EnableDer e para proteger novamente a operação.</span><span class="sxs-lookup"><span data-stu-id="789b4-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="789b4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="789b4-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="789b4-115">Crie um objeto de mapeamento de disco gerenciado com uma passagem de configurações de criptografia para discos de máquina virtual do Azure a serem replicados. Usado durante o Azure to Azure EnableDer e para proteger novamente a operação.</span><span class="sxs-lookup"><span data-stu-id="789b4-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="789b4-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="789b4-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="789b4-117">Crie um objeto de mapeamento de disco gerenciado com o ID do conjunto de criptografia do disco de destino para replicar os discos da máquina virtual do Azure. Usado durante o Azure to Azure EnableDer e para proteger novamente a operação.</span><span class="sxs-lookup"><span data-stu-id="789b4-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="789b4-118">OS</span><span class="sxs-lookup"><span data-stu-id="789b4-118">PARAMETERS</span></span>

### <span data-ttu-id="789b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789b4-119">-DefaultProfile</span></span>
<span data-ttu-id="789b4-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="789b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789b4-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="789b4-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="789b4-122">Especifica a URL do segredo de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="789b4-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="789b4-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="789b4-124">Especifica a ID do braço do cofre de chaves de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="789b4-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="789b4-125">-DiskId</span></span>
<span data-ttu-id="789b4-126">Especifica a identificação do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="789b4-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="789b4-127">-FailoverDiskName</span></span>
<span data-ttu-id="789b4-128">Especifica o nome do disco criado durante o failover.</span><span class="sxs-lookup"><span data-stu-id="789b4-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="789b4-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="789b4-130">Especifica a URL da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="789b4-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="789b4-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="789b4-132">Especifica a ID do braço do cofre da chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="789b4-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="789b4-133">-LogStorageAccountId</span></span>
<span data-ttu-id="789b4-134">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="789b4-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="789b4-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="789b4-135">-ManagedDisk</span></span>
<span data-ttu-id="789b4-136">Especifica a entrada para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="789b4-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="789b4-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="789b4-138">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="789b4-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="789b4-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="789b4-140">Especifica a ID do conjunto de criptografia do disco do Azure a ser usado para discos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="789b4-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="789b4-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="789b4-142">Especifica o tipo de conta de disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="789b4-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="789b4-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="789b4-144">Especifica a ID do grupo de recursos de recuperação para o disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="789b4-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="789b4-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="789b4-146">Especifica o disco de destino de recuperação para disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="789b4-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="789b4-147">-TfoDiskName</span></span>
<span data-ttu-id="789b4-148">Especifica o nome do disco criado durante o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="789b4-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="789b4-149">-VhdUri</span></span>
<span data-ttu-id="789b4-150">Especifique o URI do VHD do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="789b4-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b4-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="789b4-151">-Confirm</span></span>
<span data-ttu-id="789b4-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789b4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789b4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789b4-153">-WhatIf</span></span>
<span data-ttu-id="789b4-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="789b4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789b4-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="789b4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789b4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789b4-156">CommonParameters</span></span>
<span data-ttu-id="789b4-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789b4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789b4-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="789b4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789b4-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="789b4-159">INPUTS</span></span>

### <span data-ttu-id="789b4-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="789b4-160">None</span></span>

## <span data-ttu-id="789b4-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="789b4-161">OUTPUTS</span></span>

### <span data-ttu-id="789b4-162">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="789b4-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="789b4-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="789b4-163">NOTES</span></span>

## <span data-ttu-id="789b4-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="789b4-164">RELATED LINKS</span></span>
