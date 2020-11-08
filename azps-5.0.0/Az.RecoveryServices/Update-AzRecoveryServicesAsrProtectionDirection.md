---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125116"
---
# <span data-ttu-id="0f946-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="0f946-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="0f946-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f946-102">SYNOPSIS</span></span>
<span data-ttu-id="0f946-103">Atualiza a direção de replicação para o item ou o plano de recuperação especificado duplicado.</span><span class="sxs-lookup"><span data-stu-id="0f946-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="0f946-104">Usado para proteger novamente/reverter a replicação de um item de failover ou de um plano de recuperação com failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="0f946-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f946-105">SYNTAX</span></span>

### <span data-ttu-id="0f946-106">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f946-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f946-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="0f946-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f946-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f946-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f946-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0f946-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f946-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f946-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f946-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f946-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0f946-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f946-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="0f946-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f946-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f946-115">DESCRIPTION</span></span>
<span data-ttu-id="0f946-116">O cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** atualiza a direção de replicação para o objeto do Azure site Recovery especificado após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="0f946-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="0f946-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f946-117">EXAMPLES</span></span>

### <span data-ttu-id="0f946-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f946-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="0f946-119">Iniciar a operação de atualização de direção para o plano de recuperação especificado e retorna o objeto de trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="0f946-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="0f946-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0f946-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="0f946-121">Inicie a operação de atualização de direção para o item protegido de replicação especificado na região do Azure de destino definido pelo mapeamento de contêiner de proteção e usando armazenamento de cache (na mesma região da VM).</span><span class="sxs-lookup"><span data-stu-id="0f946-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="0f946-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0f946-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="0f946-123">Inicie a operação de atualização de direção para o item protegido de replicação especificado na região do Azure de destino definido pelo mapeamento de contêiner de proteção e a configuração de replicação de disco fornecida.</span><span class="sxs-lookup"><span data-stu-id="0f946-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="0f946-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0f946-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="0f946-125">Inicie a operação de atualização de direção para o item protegido de replicação criptografada na região de destino do Azure definido pelo mapeamento de contêiner de proteção e a configuração de replicação de disco fornecida.</span><span class="sxs-lookup"><span data-stu-id="0f946-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="0f946-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="0f946-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="0f946-127">Inicie a operação de atualização de direção para o item de replicação especificado na região de destino do Azure definido pelo mapeamento de contêiner de proteção e usando o armazenamento de cache (na mesma região da VM) e o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="0f946-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="0f946-128">OS</span><span class="sxs-lookup"><span data-stu-id="0f946-128">PARAMETERS</span></span>

### <span data-ttu-id="0f946-129">-Conta</span><span class="sxs-lookup"><span data-stu-id="0f946-129">-Account</span></span>
<span data-ttu-id="0f946-130">A conta Executar como a ser usada para instalar o serviço de mobilidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0f946-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="0f946-131">Deve ser uma da lista de contas Executar como na malha ASR.</span><span class="sxs-lookup"><span data-stu-id="0f946-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-132">-AzureToAzure</span></span>
<span data-ttu-id="0f946-133">Especifica a recuperação de desastre do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="0f946-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f946-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="0f946-135">Especifica a configuração de disco para a recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="0f946-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="0f946-136">-AzureToVMware</span></span>
<span data-ttu-id="0f946-137">Especifica o cenário de comutação do Azure para o vMWare.</span><span class="sxs-lookup"><span data-stu-id="0f946-137">Specifies the switch azure to vMWare scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-138">-Repositório de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0f946-138">-DataStore</span></span>
<span data-ttu-id="0f946-139">O armazenamento de dados do VMware a ser usado para o vmdisk.</span><span class="sxs-lookup"><span data-stu-id="0f946-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f946-140">-DefaultProfile</span></span>
<span data-ttu-id="0f946-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f946-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0f946-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="0f946-142">-Direction</span></span>
<span data-ttu-id="0f946-143">Especifica a direção a ser usada para a operação de atualização lançar um failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="0f946-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0f946-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f946-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0f946-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="0f946-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0f946-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="0f946-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="0f946-148">Especifica a URL do segredo de criptografia do disco com a versão (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="0f946-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="0f946-150">Especifica a ID do cofre de criptografia de disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-151">-HyperVToAzure</span></span>
<span data-ttu-id="0f946-152">Reproteger uma máquina virtual Hyper-V após o failback.</span><span class="sxs-lookup"><span data-stu-id="0f946-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0f946-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0f946-154">Especifica a URL da chave de criptografia do disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="0f946-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="0f946-156">Especifica a ID do cofre de chaves de criptografia de disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0f946-157">-LogStorageAccountId</span></span>
<span data-ttu-id="0f946-158">Especifica a ID da conta de armazenamento para armazenar o log de replicação de VMs.</span><span class="sxs-lookup"><span data-stu-id="0f946-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="0f946-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="0f946-159">-MasterTarget</span></span>
<span data-ttu-id="0f946-160">Detalhes do servidor de destino mestre.</span><span class="sxs-lookup"><span data-stu-id="0f946-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="0f946-161">-ProcessServer</span></span>
<span data-ttu-id="0f946-162">Servidor de processo a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="0f946-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0f946-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="0f946-164">ContainerMapping de proteção a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="0f946-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="0f946-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="0f946-166">O conjunto de disponibilidade em que a máquina virtual deve ser criada após o failover</span><span class="sxs-lookup"><span data-stu-id="0f946-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0f946-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="0f946-168">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="0f946-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0f946-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="0f946-170">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f946-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="0f946-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="0f946-172">A ID do recurso do serviço de nuvem de recuperação para o qual esta máquina virtual está em failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0f946-173">-RecoveryPlan</span></span>
<span data-ttu-id="0f946-174">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="0f946-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="0f946-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="0f946-176">A ID do recurso de recuperação do grupo de posicionamento de proximidade para a qual essa máquina virtual está em failover.</span><span class="sxs-lookup"><span data-stu-id="0f946-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="0f946-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="0f946-178">ID do MySource da recuperação para VM protegida.</span><span class="sxs-lookup"><span data-stu-id="0f946-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0f946-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0f946-180">Especifica um item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="0f946-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="0f946-181">-RetentionVolume</span></span>
<span data-ttu-id="0f946-182">Volume de retenção no servidor de destino mestre a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0f946-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="0f946-183">-VmmToVmm</span></span>
<span data-ttu-id="0f946-184">Atualize a direção de replicação para uma falha na máquina virtual Hyper-V que está protegida entre dois sites do Hyper-V gerenciados pelo VMM.</span><span class="sxs-lookup"><span data-stu-id="0f946-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="0f946-185">-VMwareToAzure</span></span>
<span data-ttu-id="0f946-186">Atualize a direção de replicação do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f946-186">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f946-187">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f946-187">-Confirm</span></span>
<span data-ttu-id="0f946-188">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f946-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f946-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f946-189">-WhatIf</span></span>
<span data-ttu-id="0f946-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f946-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f946-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f946-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f946-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f946-192">CommonParameters</span></span>
<span data-ttu-id="0f946-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f946-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f946-194">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f946-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f946-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f946-195">INPUTS</span></span>

### <span data-ttu-id="0f946-196">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0f946-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="0f946-197">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0f946-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0f946-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f946-198">OUTPUTS</span></span>

### <span data-ttu-id="0f946-199">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0f946-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0f946-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f946-200">NOTES</span></span>

## <span data-ttu-id="0f946-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f946-201">RELATED LINKS</span></span>
