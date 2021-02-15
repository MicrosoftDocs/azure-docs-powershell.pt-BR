---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114941"
---
# <span data-ttu-id="025fa-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="025fa-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="025fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="025fa-102">SYNOPSIS</span></span>
<span data-ttu-id="025fa-103">Cria um objeto de mapeamento de disco para que discos de máquina virtuais do Azure sejam replicados.</span><span class="sxs-lookup"><span data-stu-id="025fa-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="025fa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="025fa-104">SYNTAX</span></span>

### <span data-ttu-id="025fa-105">AzureToAzure (Padrão)</span><span class="sxs-lookup"><span data-stu-id="025fa-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025fa-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="025fa-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025fa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="025fa-107">DESCRIPTION</span></span>
<span data-ttu-id="025fa-108">Cria um objeto de mapeamento de disco que mapeia um disco de máquina virtual do Azure para a conta de armazenamento em cache e a conta de armazenamento de destino (região de recuperação) a ser usada para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="025fa-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="025fa-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="025fa-109">EXAMPLES</span></span>

### <span data-ttu-id="025fa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="025fa-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="025fa-111">Crie um objeto de mapeamento de disco para que discos de máquina virtual do Azure sejam replicados. Usado durante o Azure para HabilitarDr do Azure e proteger a operação.</span><span class="sxs-lookup"><span data-stu-id="025fa-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="025fa-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="025fa-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="025fa-113">Crie um objeto de mapeamento de disco gerenciado para que discos de máquina virtuais do Azure sejam replicados. Usado durante o Azure para HabilitarDr do Azure e proteger a operação.</span><span class="sxs-lookup"><span data-stu-id="025fa-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="025fa-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="025fa-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="025fa-115">Crie um objeto de mapeamento de disco gerenciado com configurações de criptografia de uma passagem para discos de máquina virtuais do Azure serem replicados. Usado durante o Azure para HabilitarDr do Azure e proteger a operação.</span><span class="sxs-lookup"><span data-stu-id="025fa-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="025fa-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="025fa-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="025fa-117">Crie um objeto de mapeamento de disco gerenciado com a ID de conjunto de criptografia de disco de destino para que os discos de máquina virtuais do Azure sejam replicados. Usado durante o Azure para HabilitarDr do Azure e proteger a operação.</span><span class="sxs-lookup"><span data-stu-id="025fa-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="025fa-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="025fa-118">PARAMETERS</span></span>

### <span data-ttu-id="025fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025fa-119">-DefaultProfile</span></span>
<span data-ttu-id="025fa-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="025fa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025fa-121">-DiskEncryptionSecurl</span><span class="sxs-lookup"><span data-stu-id="025fa-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="025fa-122">Especifica a URL secreta da criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="025fa-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="025fa-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="025fa-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="025fa-124">Especifica a ID arm do cofre de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="025fa-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="025fa-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="025fa-125">-DiskId</span></span>
<span data-ttu-id="025fa-126">Especifica a ID de disco do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="025fa-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="025fa-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="025fa-127">-FailoverDiskName</span></span>
<span data-ttu-id="025fa-128">Especifica o nome do disco criado durante o failover.</span><span class="sxs-lookup"><span data-stu-id="025fa-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="025fa-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="025fa-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="025fa-130">Especifica a URL de criptografia da chave.</span><span class="sxs-lookup"><span data-stu-id="025fa-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="025fa-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="025fa-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="025fa-132">Especifica a ID arm do cofre de criptografia de chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="025fa-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="025fa-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="025fa-133">-LogStorageAccountId</span></span>
<span data-ttu-id="025fa-134">Especifica a ID da conta de armazenamento em cache ou log a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="025fa-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="025fa-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="025fa-135">-ManagedDisk</span></span>
<span data-ttu-id="025fa-136">Especifica que a entrada é para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="025fa-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="025fa-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="025fa-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="025fa-138">Especifica a ID da conta de armazenamento do Azure para a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="025fa-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="025fa-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="025fa-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="025fa-140">Especifica a ID do conjunto de criptografia de disco do Azure a ser usado para discos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="025fa-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="025fa-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="025fa-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="025fa-142">Especifica o tipo de conta do disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="025fa-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="025fa-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="025fa-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="025fa-144">Especifica a ID do grupo de recursos de recuperação para disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="025fa-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="025fa-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="025fa-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="025fa-146">Especifica o disco de destino de recuperação para disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="025fa-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="025fa-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="025fa-147">-TfoDiskName</span></span>
<span data-ttu-id="025fa-148">Especifica o nome do disco criado durante o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="025fa-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="025fa-149">-HighdUri</span><span class="sxs-lookup"><span data-stu-id="025fa-149">-VhdUri</span></span>
<span data-ttu-id="025fa-150">Especifique o URI DE ACORDO do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="025fa-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="025fa-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="025fa-151">-Confirm</span></span>
<span data-ttu-id="025fa-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025fa-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025fa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025fa-153">-WhatIf</span></span>
<span data-ttu-id="025fa-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="025fa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025fa-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="025fa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025fa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025fa-156">CommonParameters</span></span>
<span data-ttu-id="025fa-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025fa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025fa-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="025fa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025fa-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="025fa-159">INPUTS</span></span>

### <span data-ttu-id="025fa-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="025fa-160">None</span></span>

## <span data-ttu-id="025fa-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="025fa-161">OUTPUTS</span></span>

### <span data-ttu-id="025fa-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="025fa-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="025fa-163">Notas</span><span class="sxs-lookup"><span data-stu-id="025fa-163">NOTES</span></span>

## <span data-ttu-id="025fa-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="025fa-164">RELATED LINKS</span></span>
