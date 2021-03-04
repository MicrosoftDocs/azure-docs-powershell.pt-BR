---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: c6e25b9b8ec7fe22f76ccec954312914af8dd53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890357"
---
# <span data-ttu-id="816c1-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="816c1-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="816c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="816c1-102">SYNOPSIS</span></span>
<span data-ttu-id="816c1-103">Atualiza a direção de replicação para o item ou plano de recuperação protegido de replicação especificado.</span><span class="sxs-lookup"><span data-stu-id="816c1-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="816c1-104">Usado para resguardar/reverter replicar um item replicado ou plano de recuperação com falha.</span><span class="sxs-lookup"><span data-stu-id="816c1-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="816c1-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="816c1-105">SYNTAX</span></span>

### <span data-ttu-id="816c1-106">ByRPIObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="816c1-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816c1-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="816c1-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="816c1-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816c1-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816c1-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="816c1-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816c1-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-111">AzureToAzure</span></span>
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

### <span data-ttu-id="816c1-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="816c1-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="816c1-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="816c1-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="816c1-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="816c1-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="816c1-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="816c1-115">DESCRIPTION</span></span>
<span data-ttu-id="816c1-116">O cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** atualiza a direção de replicação do objeto de Recuperação de Site especificado do Azure após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="816c1-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="816c1-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="816c1-117">EXAMPLES</span></span>

### <span data-ttu-id="816c1-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="816c1-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="816c1-119">Inicie a operação de direção de atualização para o plano de recuperação especificado e retorna o objeto de trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="816c1-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="816c1-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="816c1-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="816c1-121">Inicie a operação de direção de atualização para o item protegido de replicação especificado na região do azure de destino definida pelo mapeamento de contêiner de proteção e usando o armazenamento de cache (na mesma região que a VM).</span><span class="sxs-lookup"><span data-stu-id="816c1-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="816c1-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="816c1-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="816c1-123">Inicie a operação de direção de atualização para o item protegido de replicação especificado na região do azure de destino definida pelo mapeamento de contêiner de proteção e pela configuração de replicação de disco fornecida.</span><span class="sxs-lookup"><span data-stu-id="816c1-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="816c1-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="816c1-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="816c1-125">Inicie a operação de direção de atualização para o item protegido de replicação criptografada especificado na região do azure de destino definida pelo mapeamento de contêineres de proteção e pela configuração de replicação de disco fornecida.</span><span class="sxs-lookup"><span data-stu-id="816c1-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="816c1-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="816c1-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="816c1-127">Inicie a operação de direção de atualização para o item protegido de replicação especificado na região do azure de destino definida pelo mapeamento de contêineres de proteção e usando o armazenamento de cache (na mesma região que a VM) e o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="816c1-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="816c1-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="816c1-128">PARAMETERS</span></span>

### <span data-ttu-id="816c1-129">-Account</span><span class="sxs-lookup"><span data-stu-id="816c1-129">-Account</span></span>
<span data-ttu-id="816c1-130">A conta de executar como a ser usada para pressionar a instalação do serviço mobility, se necessário.</span><span class="sxs-lookup"><span data-stu-id="816c1-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="816c1-131">Deve ser um da lista de contas de executar como no tecido ASR.</span><span class="sxs-lookup"><span data-stu-id="816c1-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="816c1-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-132">-AzureToAzure</span></span>
<span data-ttu-id="816c1-133">Especifica a recuperação de desastre do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="816c1-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="816c1-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="816c1-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="816c1-135">Especifica a configuração de disco para recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="816c1-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="816c1-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="816c1-136">-AzureToVMware</span></span>
<span data-ttu-id="816c1-137">Especifica o cenário de alterná-lo para vMWare.</span><span class="sxs-lookup"><span data-stu-id="816c1-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="816c1-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="816c1-138">-DataStore</span></span>
<span data-ttu-id="816c1-139">O armazenamento de dados VMware a ser usado para o vmdisk.</span><span class="sxs-lookup"><span data-stu-id="816c1-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="816c1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="816c1-140">-DefaultProfile</span></span>
<span data-ttu-id="816c1-141">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="816c1-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="816c1-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="816c1-142">-Direction</span></span>
<span data-ttu-id="816c1-143">Especifica a direção a ser usada para a operação de atualização postar um failover.</span><span class="sxs-lookup"><span data-stu-id="816c1-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="816c1-144">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="816c1-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="816c1-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="816c1-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="816c1-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="816c1-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="816c1-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="816c1-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="816c1-148">Especifica a URL secreta de criptografia de disco com a versão(criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="816c1-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="816c1-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="816c1-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="816c1-150">Especifica a ID do cofre secreto de criptografia de disco (criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="816c1-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="816c1-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-151">-HyperVToAzure</span></span>
<span data-ttu-id="816c1-152">Reproteja uma máquina virtual do Hyper-V após o failback.</span><span class="sxs-lookup"><span data-stu-id="816c1-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="816c1-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="816c1-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="816c1-154">Especifica a URL da chave de criptografia de disco(criptografia de disco do Azure) a ser usada como VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="816c1-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="816c1-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="816c1-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="816c1-156">Especifica a chave de chave de criptografia de discoVault ID(criptografia de disco do Azure) a ser usada para recuperação VM após o failover.</span><span class="sxs-lookup"><span data-stu-id="816c1-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="816c1-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="816c1-157">-LogStorageAccountId</span></span>
<span data-ttu-id="816c1-158">Especifica a ID da conta de armazenamento para armazenar o log de replicação de VMs.</span><span class="sxs-lookup"><span data-stu-id="816c1-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="816c1-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="816c1-159">-MasterTarget</span></span>
<span data-ttu-id="816c1-160">Detalhes do servidor de destino mestre.</span><span class="sxs-lookup"><span data-stu-id="816c1-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="816c1-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="816c1-161">-ProcessServer</span></span>
<span data-ttu-id="816c1-162">Process Server a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="816c1-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="816c1-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="816c1-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="816c1-164">Contêiner de proteçãoMapping a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="816c1-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="816c1-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="816c1-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="816c1-166">O conjunto de disponibilidade em que a máquina virtual deve ser criada após o failover</span><span class="sxs-lookup"><span data-stu-id="816c1-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="816c1-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="816c1-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="816c1-168">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="816c1-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="816c1-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="816c1-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="816c1-170">Especifica a conta de armazenamento para diagnósticos de inicialização para a VM do azure de recuperação.</span><span class="sxs-lookup"><span data-stu-id="816c1-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="816c1-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="816c1-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="816c1-172">A ID de recurso do serviço de nuvem de recuperação para o failover dessa máquina virtual para.</span><span class="sxs-lookup"><span data-stu-id="816c1-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="816c1-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="816c1-173">-RecoveryPlan</span></span>
<span data-ttu-id="816c1-174">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="816c1-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="816c1-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="816c1-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="816c1-176">A ID do recurso do grupo de posicionamento de proximidade de recuperação para o failover dessa máquina virtual para.</span><span class="sxs-lookup"><span data-stu-id="816c1-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="816c1-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="816c1-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="816c1-178">Recuperação resourceGroup id para Vm protegido.</span><span class="sxs-lookup"><span data-stu-id="816c1-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="816c1-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="816c1-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="816c1-180">Especifica um item protegido por replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="816c1-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="816c1-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="816c1-181">-RetentionVolume</span></span>
<span data-ttu-id="816c1-182">Volume de retenção no servidor de destino mestre a ser usado.</span><span class="sxs-lookup"><span data-stu-id="816c1-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="816c1-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="816c1-183">-VmmToVmm</span></span>
<span data-ttu-id="816c1-184">Atualize a direção de replicação para uma máquina virtual do Hyper-V com falha protegida entre dois sites do Hyper-V gerenciados por VMM.</span><span class="sxs-lookup"><span data-stu-id="816c1-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="816c1-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="816c1-185">-VMwareToAzure</span></span>
<span data-ttu-id="816c1-186">Atualize a direção de replicação da VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="816c1-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="816c1-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="816c1-187">-Confirm</span></span>
<span data-ttu-id="816c1-188">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="816c1-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="816c1-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="816c1-189">-WhatIf</span></span>
<span data-ttu-id="816c1-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="816c1-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="816c1-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="816c1-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="816c1-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816c1-192">CommonParameters</span></span>
<span data-ttu-id="816c1-193">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="816c1-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816c1-194">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="816c1-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816c1-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="816c1-195">INPUTS</span></span>

### <span data-ttu-id="816c1-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="816c1-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="816c1-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="816c1-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="816c1-198">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="816c1-198">OUTPUTS</span></span>

### <span data-ttu-id="816c1-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="816c1-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="816c1-200">NOTES</span><span class="sxs-lookup"><span data-stu-id="816c1-200">NOTES</span></span>

## <span data-ttu-id="816c1-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="816c1-201">RELATED LINKS</span></span>
