---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3d9cd1bface4175e60b45d6865815f1a4ea964f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942688"
---
# <span data-ttu-id="19358-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19358-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="19358-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19358-102">SYNOPSIS</span></span>
<span data-ttu-id="19358-103">Habilita a replicação de um item protegido contra ASR criando um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="19358-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="19358-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19358-104">SYNTAX</span></span>

### <span data-ttu-id="19358-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="19358-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="19358-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19358-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="19358-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19358-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19358-112">DESCRIPTION</span></span>
<span data-ttu-id="19358-113">O cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="19358-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="19358-114">Use esse cmdlet para habilitar a replicação para um item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="19358-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="19358-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19358-115">EXAMPLES</span></span>

### <span data-ttu-id="19358-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="19358-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="19358-117">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="19358-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="19358-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="19358-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="19358-119">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do vmWare para o Azure).</span><span class="sxs-lookup"><span data-stu-id="19358-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="19358-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="19358-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="19358-121">Inicia a operação de criação de itens protegidos de replicação para o item protegido ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="19358-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="19358-122">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="19358-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="19358-123">Inicia a operação de criação de itens protegidos de replicação para o VmId especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="19358-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="19358-124">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="19358-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="19358-125">Inicia a operação de criação de itens protegidos de replicação para o item protegido ASR especificado, incluindo discos seletivos e retorna o trabalho ASR usado para acompanhar a operação (cenário do vmWare para o Azure) com discos selecionados.</span><span class="sxs-lookup"><span data-stu-id="19358-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="19358-126">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="19358-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="19358-127">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="19358-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="19358-128">Inicia a operação de criação de itens protegidos de replicação para o VmId especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure). Para ver os detalhes da VM de failover aprovados cmdlet para criptografia serão usados.</span><span class="sxs-lookup"><span data-stu-id="19358-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

## <span data-ttu-id="19358-129">OS</span><span class="sxs-lookup"><span data-stu-id="19358-129">PARAMETERS</span></span>

### <span data-ttu-id="19358-130">-Conta</span><span class="sxs-lookup"><span data-stu-id="19358-130">-Account</span></span>
<span data-ttu-id="19358-131">A conta Executar como a ser usada para instalar o serviço de mobilidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="19358-131">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="19358-132">Deve ser uma da lista de contas Executar como na malha ASR.</span><span class="sxs-lookup"><span data-stu-id="19358-132">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-133">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-133">-AzureToAzure</span></span>
<span data-ttu-id="19358-134">Parâmetro switch especifica a criação do item replicado no cenário do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-134">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-135">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="19358-135">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="19358-136">Especifica a configuração de disco para usar VM do cenário de recuperação de desastres do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-136">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-137">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="19358-137">-AzureVmId</span></span>
<span data-ttu-id="19358-138">Especifica a ID de VM do Azure para proteção de recuperação de desastre em região de recuperação.</span><span class="sxs-lookup"><span data-stu-id="19358-138">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19358-139">-DefaultProfile</span></span>
<span data-ttu-id="19358-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="19358-141">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="19358-141">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="19358-142">Especifica a URL do segredo de criptografia do disco com a versão (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-142">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-143">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="19358-143">-DiskEncryptionSetId</span></span>
<span data-ttu-id="19358-144">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para a criptografia dos discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="19358-144">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-145">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="19358-145">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="19358-146">Especifica a ID do cofre de criptografia de disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-146">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-147">-Disktype</span><span class="sxs-lookup"><span data-stu-id="19358-147">-DiskType</span></span>
<span data-ttu-id="19358-148">Especifica o tipo de disco gerenciado VM de recuperação.</span><span class="sxs-lookup"><span data-stu-id="19358-148">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-149">-HyperVToAzure</span></span>
<span data-ttu-id="19358-150">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada para o Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-150">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-151">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="19358-151">-IncludeDiskId</span></span>
<span data-ttu-id="19358-152">A lista de discos a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="19358-152">The list of disks to include for replication.</span></span> <span data-ttu-id="19358-153">Por padrão, todos os discos são incluídos.</span><span class="sxs-lookup"><span data-stu-id="19358-153">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-154">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="19358-154">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="19358-155">Especifica a entrada de configuração de disco para o ID de disco do vMWare para proteger de um item de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="19358-155">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-156">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="19358-156">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="19358-157">Especifica a URL da chave de criptografia de disco com a versão (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-157">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-158">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="19358-158">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="19358-159">Especifica a ID do cofre de chaves de criptografia de disco (criptografia de disco do Azure) a ser usada para a VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-159">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-160">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19358-160">-LogStorageAccountId</span></span>
<span data-ttu-id="19358-161">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="19358-161">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="19358-162">-Name</span></span>
<span data-ttu-id="19358-163">Especifica um nome para o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="19358-163">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="19358-164">O nome deve ser exclusivo no cofre.</span><span class="sxs-lookup"><span data-stu-id="19358-164">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="19358-165">-OS</span><span class="sxs-lookup"><span data-stu-id="19358-165">-OS</span></span>
<span data-ttu-id="19358-166">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="19358-166">Specifies the operating system family.</span></span>
<span data-ttu-id="19358-167">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="19358-167">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-168">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="19358-168">-OSDiskName</span></span>
<span data-ttu-id="19358-169">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="19358-169">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-170">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="19358-170">-ProcessServer</span></span>
<span data-ttu-id="19358-171">O servidor de processo a ser usado para replicar este computador.</span><span class="sxs-lookup"><span data-stu-id="19358-171">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="19358-172">Use a lista de servidores de processo na malha ASR correspondente ao servidor de configuração para especificar um.</span><span class="sxs-lookup"><span data-stu-id="19358-172">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-173">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="19358-173">-ProtectableItem</span></span>
<span data-ttu-id="19358-174">Especifica o objeto de item protectable ASR para o qual a replicação está sendo habilitada.</span><span class="sxs-lookup"><span data-stu-id="19358-174">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19358-175">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19358-175">-ProtectionContainerMapping</span></span>
<span data-ttu-id="19358-176">Especifica o objeto de mapeamento de contêiner de proteção ASR correspondente à política de replicação a ser usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="19358-176">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-177">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="19358-177">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="19358-178">A ID do Availabilityset para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="19358-178">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-179">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="19358-179">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="19358-180">Especifica a zona de disponibilidade da VM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-180">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-181">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="19358-181">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="19358-182">A ID da rede virtual do Azure para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="19358-182">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-183">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19358-183">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="19358-184">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="19358-184">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-185">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="19358-185">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="19358-186">A sub-rede dentro da rede virtual de recuperação do Azure à qual a máquina virtual com failover deve ser anexada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="19358-186">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-187">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19358-187">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="19358-188">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-188">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-189">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="19358-189">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="19358-190">Especifica a ID do recurso de recuperação do serviço de nuvem para a qual essa máquina virtual se desfailoveru.</span><span class="sxs-lookup"><span data-stu-id="19358-190">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-191">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="19358-191">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="19358-192">Especifica o identificador de braço do grupo de recursos no qual a máquina virtual será criada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="19358-192">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-193">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="19358-193">-RecoveryVmName</span></span>
<span data-ttu-id="19358-194">Nome da VM de recuperação criada após o failover.</span><span class="sxs-lookup"><span data-stu-id="19358-194">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-195">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="19358-195">-ReplicationGroupName</span></span>
<span data-ttu-id="19358-196">Especifica o nome do grupo de replicação a ser usado para criar pontos de recuperação consistentes de várias VMS.</span><span class="sxs-lookup"><span data-stu-id="19358-196">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="19358-197">Por padrão, cada item de replicação protegida é criado em um grupo de pontos de recuperação consistentes e com várias VMs não gerados.</span><span class="sxs-lookup"><span data-stu-id="19358-197">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="19358-198">Use essa opção somente se você precisar criar pontos de recuperação consistentes de várias VMs em um grupo de máquinas ao proteger todas as máquinas ao mesmo grupo de replicação.</span><span class="sxs-lookup"><span data-stu-id="19358-198">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-199">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="19358-199">-VmmToVmm</span></span>
<span data-ttu-id="19358-200">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada entre sites do Hyper-V gerenciados pelo VMM.</span><span class="sxs-lookup"><span data-stu-id="19358-200">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-201">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="19358-201">-VMwareToAzure</span></span>
<span data-ttu-id="19358-202">Parâmetro de opção para especificar o item replicado é uma máquina virtual do VMware ou um servidor físico que será replicado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="19358-202">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19358-203">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="19358-203">-WaitForCompletion</span></span>
<span data-ttu-id="19358-204">Especifica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="19358-204">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="19358-205">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19358-205">-Confirm</span></span>
<span data-ttu-id="19358-206">Solicita confirmação antes de iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="19358-206">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="19358-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19358-207">-WhatIf</span></span>
<span data-ttu-id="19358-208">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19358-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19358-209">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19358-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19358-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19358-210">CommonParameters</span></span>
<span data-ttu-id="19358-211">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19358-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19358-212">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19358-212">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19358-213">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19358-213">INPUTS</span></span>

### <span data-ttu-id="19358-214">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="19358-214">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="19358-215">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19358-215">OUTPUTS</span></span>

### <span data-ttu-id="19358-216">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="19358-216">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="19358-217">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19358-217">NOTES</span></span>

## <span data-ttu-id="19358-218">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19358-218">RELATED LINKS</span></span>

[<span data-ttu-id="19358-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19358-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="19358-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19358-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="19358-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="19358-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
