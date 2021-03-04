---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ad3f2c07d358819917706253df05bfd899c3b53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891302"
---
# <span data-ttu-id="12c9b-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12c9b-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="12c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="12c9b-103">Define propriedades de recuperação, como rede de destino e tamanho de máquina virtual para o item protegido de replicação especificado.</span><span class="sxs-lookup"><span data-stu-id="12c9b-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="12c9b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12c9b-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12c9b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="12c9b-106">O cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** define as propriedades de recuperação de um Item Protegido por Replicação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="12c9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12c9b-107">EXAMPLES</span></span>

### <span data-ttu-id="12c9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12c9b-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="12c9b-109">Inicia a operação de atualização das configurações de item protegido de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="12c9b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="12c9b-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="12c9b-111">Inicia a operação de atualização das configurações de cartão de interface de rede do item protegido de replicação(Redução de NIC) usando os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="12c9b-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="12c9b-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="12c9b-113">Inicia a operação de atualização do NIC principal do item protegido de replicação (a ser usado para configurações de vm )recuperadas usando os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="12c9b-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="12c9b-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="12c9b-115">Inicia a operação de atualização do item protegido de replicação NIC (a ser usado para configurações de vm recuperada )usando os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="12c9b-116">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="12c9b-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="12c9b-117">Inicia a operação de atualização do item protegido de replicação selecionado noc tp habilitar rede acelerada na VM de recuperação(para o Azure para recuperação de desastre do Azure).</span><span class="sxs-lookup"><span data-stu-id="12c9b-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="12c9b-118">Não passe -EnableAcceleratedNetworkingOnRecovery para desabilitar a Rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="12c9b-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="12c9b-119">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="12c9b-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="12c9b-120">Inicie a operação de atualização do item protegido de replicação criptografada especificado para usar detalhes de criptografia fornecidos para vM de failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="12c9b-121">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="12c9b-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="12c9b-122">Inicie a operação de atualização para o item protegido de replicação especificado para usar o grupo de posicionamento de proximidade fornecido para vm de failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>

## <span data-ttu-id="12c9b-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12c9b-123">PARAMETERS</span></span>

### <span data-ttu-id="12c9b-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="12c9b-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="12c9b-125">Especifica os detalhes de configuração de NIC de failover e failover de teste.</span><span class="sxs-lookup"><span data-stu-id="12c9b-125">Specifies the test failover and failover NIC configuration details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="12c9b-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="12c9b-127">Especifica a configuração de disco a ser udpated para Vm de disco gerenciado (Azure para Scenrio dr do Azure).</span><span class="sxs-lookup"><span data-stu-id="12c9b-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c9b-128">-DefaultProfile</span></span>
<span data-ttu-id="12c9b-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12c9b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="12c9b-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="12c9b-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="12c9b-131">Especifica a URL secreta de criptografia de disco com a versão(criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="12c9b-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="12c9b-133">Especifica a ID do cofre de chave secreta de criptografia de disco (criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="12c9b-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="12c9b-135">O dicionário da ID do recurso de disco para o conjunto de criptografia de disco ARM ID.</span><span class="sxs-lookup"><span data-stu-id="12c9b-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="12c9b-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="12c9b-137">Especifica o NIC especificado no vm de recuperação depois que o failover usa rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="12c9b-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12c9b-138">-InputObject</span></span>
<span data-ttu-id="12c9b-139">O objeto de entrada para o cmdlet: o objeto de item protegido de replicação ASR correspondente ao item protegido de replicação a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="12c9b-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="12c9b-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="12c9b-141">Especifica a versão da URL da chave de criptografia de disco (criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="12c9b-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="12c9b-143">Especifica a chave de chave de criptografia de discoVault ID(criptografia de disco do Azure) a ser usada para recuperação VM após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="12c9b-144">-LicenseType</span></span>
<span data-ttu-id="12c9b-145">Especifica a seleção do tipo de licença a ser usada para máquinas virtuais do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="12c9b-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="12c9b-146">Se você tiver o direito de usar o Benefício de Uso Híbrido do Azure (HUB) para migrações e quiser especificar que a configuração hub seja usada durante a falha nesse item protegido, deverão definir o tipo de licença como WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="12c9b-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-147">-Name</span><span class="sxs-lookup"><span data-stu-id="12c9b-147">-Name</span></span>
<span data-ttu-id="12c9b-148">Especifica o nome da máquina virtual de recuperação que será criada no failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="12c9b-149">-NicSelectionType</span></span>
<span data-ttu-id="12c9b-150">Especifica as propriedades do NIC (cartão de interface de rede) definidas pelo usuário ou definidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="12c9b-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="12c9b-151">Você pode especificar NotSelected para voltar aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="12c9b-151">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="12c9b-152">-PrimaryNic</span></span>
<span data-ttu-id="12c9b-153">Especifica o NIC que será usado como NIC principal para VM de revcovery após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="12c9b-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="12c9b-155">Conjunto de disponibilidade para item protegido por replicação após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-155">Availability set for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-156">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="12c9b-156">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="12c9b-157">Especifica a zona de disponibilidade para o item protegido de replicação após o failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-157">Specifies availability zone for replication protected item after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-158">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="12c9b-158">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="12c9b-159">Especifica a conta de armazenamento para diagnósticos de inicialização para a VM do azure de recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-159">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-160">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="12c9b-160">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="12c9b-161">A ID de recurso do serviço de nuvem de recuperação para o failover dessa máquina virtual para.</span><span class="sxs-lookup"><span data-stu-id="12c9b-161">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-162">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="12c9b-162">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="12c9b-163">Especifica os pools de endereços de back-end de destino a serem associados à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-163">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-164">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="12c9b-164">-RecoveryNetworkId</span></span>
<span data-ttu-id="12c9b-165">Especifica a ID da rede virtual do Azure para a qual o item protegido deve ser reprovado.</span><span class="sxs-lookup"><span data-stu-id="12c9b-165">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-166">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="12c9b-166">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="12c9b-167">Especifica a ID do grupo de segurança de rede a ser associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-167">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-168">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="12c9b-168">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="12c9b-169">Especifica o endereço IP estático que deve ser atribuído à NIC principal na recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-169">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-170">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="12c9b-170">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="12c9b-171">Especifica o nome da sub-rede na rede virtual de recuperação do Azure à qual essa NIC do item protegido deve ser conectada no failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-171">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-172">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="12c9b-172">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="12c9b-173">Especifica a ID de Recurso do grupo de posicionamento de proximidade de recuperação para o failover da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="12c9b-173">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-174">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="12c9b-174">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="12c9b-175">Especifica a ID do recurso de endereço IP público a ser associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-175">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-176">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="12c9b-176">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="12c9b-177">A ID do grupo de recursos do Azure na região de recuperação na qual o item protegido será recuperado no failover.</span><span class="sxs-lookup"><span data-stu-id="12c9b-177">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-178">-Size</span><span class="sxs-lookup"><span data-stu-id="12c9b-178">-Size</span></span>
<span data-ttu-id="12c9b-179">Especifica o tamanho da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="12c9b-179">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="12c9b-180">O valor deve ser do conjunto de tamanhos suportado por máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="12c9b-180">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-181">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="12c9b-181">-TfoAzureVMName</span></span>
<span data-ttu-id="12c9b-182">Especifica o nome da VM de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="12c9b-182">Specifies the name of the test failover VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-183">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="12c9b-183">-UpdateNic</span></span>
<span data-ttu-id="12c9b-184">Especifica a NIC da máquina virtual para a qual este cmdlet define que a propriedade de rede de recuperação precisa ser udpated.</span><span class="sxs-lookup"><span data-stu-id="12c9b-184">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-185">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="12c9b-185">-UseManagedDisk</span></span>
<span data-ttu-id="12c9b-186">Especifica se a máquina virtual do Azure criada no failover deve usar discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="12c9b-186">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c9b-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12c9b-187">-Confirm</span></span>
<span data-ttu-id="12c9b-188">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c9b-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c9b-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c9b-189">-WhatIf</span></span>
<span data-ttu-id="12c9b-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12c9b-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12c9b-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12c9b-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c9b-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c9b-192">CommonParameters</span></span>
<span data-ttu-id="12c9b-193">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c9b-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c9b-194">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12c9b-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c9b-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12c9b-195">INPUTS</span></span>

### <span data-ttu-id="12c9b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12c9b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="12c9b-197">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12c9b-197">OUTPUTS</span></span>

### <span data-ttu-id="12c9b-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="12c9b-198">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="12c9b-199">NOTES</span><span class="sxs-lookup"><span data-stu-id="12c9b-199">NOTES</span></span>

## <span data-ttu-id="12c9b-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12c9b-200">RELATED LINKS</span></span>

[<span data-ttu-id="12c9b-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12c9b-201">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="12c9b-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12c9b-202">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="12c9b-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12c9b-203">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
