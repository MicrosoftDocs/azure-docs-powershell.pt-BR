---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115706"
---
# <span data-ttu-id="ecca1-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ecca1-101">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="ecca1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecca1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecca1-103">Define propriedades de recuperação, como a rede de destino e o tamanho da máquina virtual para o item protegido de replicação especificado.</span><span class="sxs-lookup"><span data-stu-id="ecca1-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

## <span data-ttu-id="ecca1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecca1-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecca1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecca1-105">DESCRIPTION</span></span>
<span data-ttu-id="ecca1-106">O cmdlet **set-AzRecoveryServicesAsrReplicationProtectedItem** define as propriedades de recuperação para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-106">The **Set-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="ecca1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecca1-107">EXAMPLES</span></span>

### <span data-ttu-id="ecca1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecca1-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="ecca1-109">Inicia a operação de atualização das configurações do item protegido de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-109">Starts the operation of updating the replication protected item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ecca1-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ecca1-110">Example 2</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

<span data-ttu-id="ecca1-111">Inicia a operação de atualização das configurações da placa de interface de rede (redução da NIC) do item protegido de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-111">Starts the operation of updating the replication protected item Network Interface card(NIC Reduction) settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ecca1-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ecca1-112">Example 3</span></span>
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

<span data-ttu-id="ecca1-113">Inicia a operação de atualização do item protegido da NIC primária (usada para a VM recuperada) usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-113">Starts the operation of updating the replication protected item primary NIC(to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ecca1-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ecca1-114">Example 4</span></span>
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

<span data-ttu-id="ecca1-115">Inicia a operação de atualização da NIC de item protegido de replicação (usado para a VM recuperada) usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-115">Starts the operation of updating the replication protected item NIC (to used for recovered vm )settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ecca1-116">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="ecca1-116">Example 5</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

<span data-ttu-id="ecca1-117">Inicia a operação de atualização do item protegido de replicação selecionado o NOC PA habilitar a rede acelerada na VM de recuperação (para recuperação de desastres do Azure para Azure).</span><span class="sxs-lookup"><span data-stu-id="ecca1-117">Starts the operation of updating the replication protected item selected noc tp enable accelerated networking on recovery VM(for Azure to Azure disaster recovery).</span></span>
<span data-ttu-id="ecca1-118">Don t Pass-EnableAcceleratedNetworkingOnRecovery para desativar a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="ecca1-118">Don�t pass -EnableAcceleratedNetworkingOnRecovery to disable accelerated Networking.</span></span>

### <span data-ttu-id="ecca1-119">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="ecca1-119">Example 6</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="ecca1-120">Inicie a operação de atualização para o item protegido de replicação criptografada para usar detalhes de criptografia fornecidos para a VM de failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-120">Start the update operation for the specified encrypted replication protected item to use supplied encryption details for failover VM.</span></span>

### <span data-ttu-id="ecca1-121">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="ecca1-121">Example 7</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="ecca1-122">Inicie a operação de atualização para o item protegido de replicação especificado para usar o grupo de posicionamento de proximidade fornecido para a VM de failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-122">Start the update operation for the specified replication protected item to use the supplied proximity placement group for failover VM.</span></span>


## <span data-ttu-id="ecca1-123">OS</span><span class="sxs-lookup"><span data-stu-id="ecca1-123">PARAMETERS</span></span>

### <span data-ttu-id="ecca1-124">-ASRVMNicConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecca1-124">-ASRVMNicConfiguration</span></span>
<span data-ttu-id="ecca1-125">Especifica os detalhes de failover de teste e de configuração da NIC de failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-125">Specifies the test failover and failover NIC configuration details.</span></span>

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

### <span data-ttu-id="ecca1-126">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecca1-126">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="ecca1-127">Especifica a configuração de disco a ser udpated para a VM de disco gerenciado (Azure DR para Azure scenrio).</span><span class="sxs-lookup"><span data-stu-id="ecca1-127">Specifies the disk configuration to udpated for managed disk Vm (Azure to Azure DR scenrio).</span></span>

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

### <span data-ttu-id="ecca1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecca1-128">-DefaultProfile</span></span>
<span data-ttu-id="ecca1-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecca1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ecca1-130">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="ecca1-130">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="ecca1-131">Especifica a URL do segredo de criptografia do disco com a versão (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-131">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ecca1-132">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ecca1-132">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="ecca1-133">Especifica a ID do cofre da chave secreta de criptografia do disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-133">Specifies the disk encryption secret key vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ecca1-134">-DiskIdToDiskEncryptionSetMap</span><span class="sxs-lookup"><span data-stu-id="ecca1-134">-DiskIdToDiskEncryptionSetMap</span></span>
<span data-ttu-id="ecca1-135">O dicionário da ID do recurso de disco para a identificação do ARM do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="ecca1-135">The dictionary of disk resource Id to disk encryption set ARM Id.</span></span>

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

### <span data-ttu-id="ecca1-136">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="ecca1-136">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="ecca1-137">Especifica o NIC especificado na VM de recuperação após o failover usar a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="ecca1-137">Specifies the specified NIC on recovery vm after failover uses accelerated networking.</span></span>

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

### <span data-ttu-id="ecca1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecca1-138">-InputObject</span></span>
<span data-ttu-id="ecca1-139">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item de replicação protegida a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="ecca1-139">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

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

### <span data-ttu-id="ecca1-140">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ecca1-140">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ecca1-141">Especifica a versão da URL da chave de criptografia do disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-141">Specifies the disk encryption key URL version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="ecca1-142">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ecca1-142">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="ecca1-143">Especifica a ID do cofre de chaves de criptografia de disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-143">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>


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

### <span data-ttu-id="ecca1-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ecca1-144">-LicenseType</span></span>
<span data-ttu-id="ecca1-145">Especifique a seleção do tipo de licença a ser usada para máquinas virtuais do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ecca1-145">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="ecca1-146">Se você tem o direito de usar o centro de uso híbrido do Azure (HUB) para migrações e gostaria de especificar que a configuração do HUB seja usada durante a falha desse item protegido, defina o tipo de licença como WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="ecca1-146">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

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

### <span data-ttu-id="ecca1-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecca1-147">-Name</span></span>
<span data-ttu-id="ecca1-148">Especifica o nome da máquina virtual de recuperação que será criada no failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-148">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="ecca1-149">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="ecca1-149">-NicSelectionType</span></span>
<span data-ttu-id="ecca1-150">Especifica as propriedades da NIC (placa de interface de rede) definidas por usuário ou definidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="ecca1-150">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="ecca1-151">Você pode especificar não selecionado para voltar aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="ecca1-151">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="ecca1-152">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="ecca1-152">-PrimaryNic</span></span>
<span data-ttu-id="ecca1-153">Especifica a NIC que será usada como NIC primário para a VM recvcovery após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-153">Specifies the NIC which will be used as primary NIC for recvcovery VM after after failover.</span></span>

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

### <span data-ttu-id="ecca1-154">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ecca1-154">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="ecca1-155">Conjunto de disponibilidade para o item protegido da replicação após o failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-155">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="ecca1-156">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ecca1-156">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="ecca1-157">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecca1-157">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="ecca1-158">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="ecca1-158">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="ecca1-159">A ID do recurso do serviço de nuvem de recuperação para o qual esta máquina virtual está em failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-159">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="ecca1-160">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ecca1-160">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="ecca1-161">Especifica os pools de endereços de back-end de destino a serem associados à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-161">Specifies the target backend address pools to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ecca1-162">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="ecca1-162">-RecoveryNetworkId</span></span>
<span data-ttu-id="ecca1-163">Especifica a ID da rede virtual do Azure para a qual o item protegido deve ter failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-163">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="ecca1-164">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ecca1-164">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="ecca1-165">Especifica a ID do grupo de segurança de rede a ser associada à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-165">Specifies the ID of the network security group to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ecca1-166">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="ecca1-166">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="ecca1-167">Especifica o endereço IP estático que deve ser atribuído à NIC primária na recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-167">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="ecca1-168">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="ecca1-168">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="ecca1-169">Especifica o nome da sub-rede na rede virtual do Azure de recuperação à qual essa NIC do item protegido deve estar conectada no failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-169">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="ecca1-170">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ecca1-170">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="ecca1-171">Especifica a ID do recurso de recuperação do grupo de posicionamento de proximidade para a qual a máquina virtual será desactivada.</span><span class="sxs-lookup"><span data-stu-id="ecca1-171">Specifies the Resource Id of the recovery proximity placement group to failover teh virtual machine to.</span></span>

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

### <span data-ttu-id="ecca1-172">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="ecca1-172">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="ecca1-173">Especifica a ID do recurso de endereço IP público a ser associado à NIC de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-173">Specifies the ID of the public IP address resource to be associated with the recovery NIC.</span></span>

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

### <span data-ttu-id="ecca1-174">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ecca1-174">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="ecca1-175">A ID do grupo de recursos do Azure na região de recuperação na qual o item protegido será recuperado no failover.</span><span class="sxs-lookup"><span data-stu-id="ecca1-175">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="ecca1-176">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="ecca1-176">-Size</span></span>
<span data-ttu-id="ecca1-177">Especifica o tamanho da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ecca1-177">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="ecca1-178">O valor deve ser do conjunto de tamanhos com suporte nas máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecca1-178">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="ecca1-179">-TfoAzureVMName</span><span class="sxs-lookup"><span data-stu-id="ecca1-179">-TfoAzureVMName</span></span>
<span data-ttu-id="ecca1-180">Especifica o nome da VM de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="ecca1-180">Specifies the name of the test failover VM.</span></span>

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

### <span data-ttu-id="ecca1-181">-UpdateNic</span><span class="sxs-lookup"><span data-stu-id="ecca1-181">-UpdateNic</span></span>
<span data-ttu-id="ecca1-182">Especifica a NIC da máquina virtual para a qual esse cmdlet define a propriedade de recuperação de rede necessária para udpated.</span><span class="sxs-lookup"><span data-stu-id="ecca1-182">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property needs to udpated.</span></span>

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

### <span data-ttu-id="ecca1-183">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ecca1-183">-UseManagedDisk</span></span>
<span data-ttu-id="ecca1-184">Especifica se a máquina virtual do Azure criada no failover deve usar discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="ecca1-184">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

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

### <span data-ttu-id="ecca1-185">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecca1-185">-Confirm</span></span>
<span data-ttu-id="ecca1-186">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecca1-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecca1-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecca1-187">-WhatIf</span></span>
<span data-ttu-id="ecca1-188">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecca1-188">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecca1-189">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecca1-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecca1-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecca1-190">CommonParameters</span></span>
<span data-ttu-id="ecca1-191">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecca1-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecca1-192">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecca1-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecca1-193">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecca1-193">INPUTS</span></span>

### <span data-ttu-id="ecca1-194">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ecca1-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ecca1-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecca1-195">OUTPUTS</span></span>

### <span data-ttu-id="ecca1-196">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ecca1-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ecca1-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecca1-197">NOTES</span></span>

## <span data-ttu-id="ecca1-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecca1-198">RELATED LINKS</span></span>

[<span data-ttu-id="ecca1-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ecca1-199">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ecca1-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ecca1-200">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ecca1-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ecca1-201">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
