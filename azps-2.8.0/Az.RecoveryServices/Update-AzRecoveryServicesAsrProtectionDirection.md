---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772949"
---
# <span data-ttu-id="47ca4-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="47ca4-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="47ca4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="47ca4-103">Atualiza a direção de replicação para o item ou o plano de recuperação especificado duplicado.</span><span class="sxs-lookup"><span data-stu-id="47ca4-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="47ca4-104">Usado para proteger novamente/reverter a replicação de um item de failover ou de um plano de recuperação com failover.</span><span class="sxs-lookup"><span data-stu-id="47ca4-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="47ca4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47ca4-105">SYNTAX</span></span>

### <span data-ttu-id="47ca4-106">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="47ca4-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ca4-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="47ca4-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47ca4-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ca4-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ca4-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="47ca4-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ca4-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47ca4-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47ca4-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47ca4-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="47ca4-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ca4-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="47ca4-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ca4-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47ca4-115">DESCRIPTION</span></span>
<span data-ttu-id="47ca4-116">O cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** atualiza a direção de replicação para o objeto do Azure site Recovery especificado após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="47ca4-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="47ca4-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47ca4-117">EXAMPLES</span></span>

### <span data-ttu-id="47ca4-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47ca4-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="47ca4-119">Iniciar a operação de atualização de direção para o plano de recuperação especificado e retorna o objeto de trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="47ca4-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="47ca4-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47ca4-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="47ca4-121">Inicie a operação de atualização de direção para o item protegido de replicação especificado na região do Azure de destino definido pelo mapeamento de contêiner de proteção e usando armazenamento de cache (na mesma região da VM).</span><span class="sxs-lookup"><span data-stu-id="47ca4-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="47ca4-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="47ca4-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="47ca4-123">Inicie a operação de atualização de direção para o item protegido de replicação especificado na região do Azure de destino definido pelo mapeamento de contêiner de proteção e a configuração de replicação de disco fornecida.</span><span class="sxs-lookup"><span data-stu-id="47ca4-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="47ca4-124">OS</span><span class="sxs-lookup"><span data-stu-id="47ca4-124">PARAMETERS</span></span>

### <span data-ttu-id="47ca4-125">-Conta</span><span class="sxs-lookup"><span data-stu-id="47ca4-125">-Account</span></span>
<span data-ttu-id="47ca4-126">A conta Executar como a ser usada para instalar o serviço de mobilidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="47ca4-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="47ca4-127">Deve ser uma da lista de contas Executar como na malha ASR.</span><span class="sxs-lookup"><span data-stu-id="47ca4-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="47ca4-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-128">-AzureToAzure</span></span>
<span data-ttu-id="47ca4-129">{{Fill AzureToAzure descrição}}</span><span class="sxs-lookup"><span data-stu-id="47ca4-129">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="47ca4-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="47ca4-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="47ca4-131">{{Fill AzureToAzureDiskReplicationConfiguration descrição}}</span><span class="sxs-lookup"><span data-stu-id="47ca4-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="47ca4-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="47ca4-132">-AzureToVMware</span></span>
<span data-ttu-id="47ca4-133">{{Fill AzureToVMware descrição}}</span><span class="sxs-lookup"><span data-stu-id="47ca4-133">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="47ca4-134">-Repositório de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47ca4-134">-DataStore</span></span>
<span data-ttu-id="47ca4-135">O repositório de armazenamento do VMware a ser usado para o vmdisk.</span><span class="sxs-lookup"><span data-stu-id="47ca4-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="47ca4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ca4-136">-DefaultProfile</span></span>
<span data-ttu-id="47ca4-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ca4-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="47ca4-138">-Direction</span><span class="sxs-lookup"><span data-stu-id="47ca4-138">-Direction</span></span>
<span data-ttu-id="47ca4-139">Especifica a direção a ser usada para a operação de atualização lançar um failover.</span><span class="sxs-lookup"><span data-stu-id="47ca4-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="47ca4-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="47ca4-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47ca4-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="47ca4-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="47ca4-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="47ca4-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="47ca4-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-143">-HyperVToAzure</span></span>
<span data-ttu-id="47ca4-144">Reproteger uma máquina virtual Hyper-V após o failback.</span><span class="sxs-lookup"><span data-stu-id="47ca4-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="47ca4-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47ca4-145">-LogStorageAccountId</span></span>
<span data-ttu-id="47ca4-146">Especifica a ID da conta de armazenamento para armazenar o log de replicação de VMs.</span><span class="sxs-lookup"><span data-stu-id="47ca4-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="47ca4-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="47ca4-147">-MasterTarget</span></span>
<span data-ttu-id="47ca4-148">Detalhes do servidor de destino mestre.</span><span class="sxs-lookup"><span data-stu-id="47ca4-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="47ca4-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="47ca4-149">-ProcessServer</span></span>
<span data-ttu-id="47ca4-150">Servidor de processo a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="47ca4-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="47ca4-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="47ca4-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="47ca4-152">ContainerMapping de proteção a ser usado para replicação.</span><span class="sxs-lookup"><span data-stu-id="47ca4-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="47ca4-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="47ca4-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="47ca4-154">O conjunto de disponibilidade em que a máquina virtual deve ser criada após o failover</span><span class="sxs-lookup"><span data-stu-id="47ca4-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="47ca4-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47ca4-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="47ca4-156">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="47ca4-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="47ca4-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47ca4-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="47ca4-158">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="47ca4-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="47ca4-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="47ca4-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="47ca4-160">A ID do recurso do serviço de nuvem de recuperação para o qual esta máquina virtual está em failover.</span><span class="sxs-lookup"><span data-stu-id="47ca4-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="47ca4-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47ca4-161">-RecoveryPlan</span></span>
<span data-ttu-id="47ca4-162">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="47ca4-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="47ca4-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="47ca4-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="47ca4-164">ID do MySource da recuperação para VM protegida.</span><span class="sxs-lookup"><span data-stu-id="47ca4-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="47ca4-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47ca4-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="47ca4-166">Especifica um item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="47ca4-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="47ca4-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="47ca4-167">-RetentionVolume</span></span>
<span data-ttu-id="47ca4-168">Volume de retenção no servidor de destino mestre a ser usado.</span><span class="sxs-lookup"><span data-stu-id="47ca4-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="47ca4-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="47ca4-169">-VmmToVmm</span></span>
<span data-ttu-id="47ca4-170">Atualize a direção de replicação para uma falha na máquina virtual Hyper-V que está protegida entre dois sites do Hyper-V gerenciados pelo VMM.</span><span class="sxs-lookup"><span data-stu-id="47ca4-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="47ca4-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="47ca4-171">-VMwareToAzure</span></span>
<span data-ttu-id="47ca4-172">Atualize a direção de replicação do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47ca4-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="47ca4-173">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47ca4-173">-Confirm</span></span>
<span data-ttu-id="47ca4-174">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ca4-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ca4-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ca4-175">-WhatIf</span></span>
<span data-ttu-id="47ca4-176">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47ca4-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47ca4-177">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47ca4-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ca4-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ca4-178">CommonParameters</span></span>
<span data-ttu-id="47ca4-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ca4-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ca4-180">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ca4-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ca4-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47ca4-181">INPUTS</span></span>

### <span data-ttu-id="47ca4-182">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="47ca4-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="47ca4-183">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="47ca4-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="47ca4-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47ca4-184">OUTPUTS</span></span>

### <span data-ttu-id="47ca4-185">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="47ca4-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="47ca4-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47ca4-186">NOTES</span></span>

## <span data-ttu-id="47ca4-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47ca4-187">RELATED LINKS</span></span>
