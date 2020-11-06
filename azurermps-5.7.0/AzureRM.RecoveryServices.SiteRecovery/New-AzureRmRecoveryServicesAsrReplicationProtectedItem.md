---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fab7fa9f02f70b5afa1c4c5ffcbd07a8e1706998
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609503"
---
# <span data-ttu-id="bfb96-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="bfb96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfb96-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb96-103">Habilita a replicação de um item protegido contra ASR criando um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfb96-104">SYNTAX</span></span>

### <span data-ttu-id="bfb96-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="bfb96-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb96-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb96-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb96-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb96-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb96-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfb96-110">DESCRIPTION</span></span>
<span data-ttu-id="bfb96-111">O cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="bfb96-111">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="bfb96-112">Use esse cmdlet para habilitar a replicação para um item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="bfb96-112">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="bfb96-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb96-113">EXAMPLES</span></span>

### <span data-ttu-id="bfb96-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfb96-114">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="bfb96-115">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-115">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bfb96-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bfb96-116">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="bfb96-117">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do vmWare para o Azure).</span><span class="sxs-lookup"><span data-stu-id="bfb96-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="bfb96-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bfb96-118">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="bfb96-119">Inicia a operação de criação de itens protegidos de replicação para o item protegido ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="bfb96-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="bfb96-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bfb96-120">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="bfb96-121">Inicia a operação de criação de itens protegidos de replicação para o VmId especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="bfb96-121">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="bfb96-122">OS</span><span class="sxs-lookup"><span data-stu-id="bfb96-122">PARAMETERS</span></span>

### <span data-ttu-id="bfb96-123">-Conta</span><span class="sxs-lookup"><span data-stu-id="bfb96-123">-Account</span></span>
<span data-ttu-id="bfb96-124">A conta Executar como a ser usada para instalar o serviço de mobilidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bfb96-124">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="bfb96-125">Deve ser uma da lista de contas Executar como na malha ASR.</span><span class="sxs-lookup"><span data-stu-id="bfb96-125">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-126">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-126">-AzureToAzure</span></span>
<span data-ttu-id="bfb96-127">Parâmetro de opção para especificar que o item replicado é uma máquina virtual do Azure que Replica em uma região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb96-127">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-128">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfb96-128">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="bfb96-129">Especifica a lista de discos da máquina virtual a ser replicada e a conta de armazenamento do cache e a conta de armazenamento de recuperação a serem usadas para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="bfb96-129">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-130">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="bfb96-130">-AzureVmId</span></span>
<span data-ttu-id="bfb96-131">Especifica a ID da VM do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="bfb96-131">Specifies the azure vm id to be replicated.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bfb96-132">-Confirm</span></span>
<span data-ttu-id="bfb96-133">Solicita confirmação antes de iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-133">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb96-134">-DefaultProfile</span></span>
<span data-ttu-id="bfb96-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb96-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="bfb96-136">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-136">-HyperVToAzure</span></span>
<span data-ttu-id="bfb96-137">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada para o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb96-137">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-138">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="bfb96-138">-IncludeDiskId</span></span>
<span data-ttu-id="bfb96-139">A lista de discos a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-139">The list of disks to include for replication.</span></span> <span data-ttu-id="bfb96-140">Por padrão, todos os discos são incluídos.</span><span class="sxs-lookup"><span data-stu-id="bfb96-140">By default all disks are included.</span></span>

```yaml
Type: String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-141">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bfb96-141">-LogStorageAccountId</span></span>
<span data-ttu-id="bfb96-142">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-142">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfb96-143">-Name</span></span>
<span data-ttu-id="bfb96-144">Especifica um nome para o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="bfb96-144">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="bfb96-145">O nome deve ser exclusivo no cofre.</span><span class="sxs-lookup"><span data-stu-id="bfb96-145">The name must be unique within the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-146">-OS</span><span class="sxs-lookup"><span data-stu-id="bfb96-146">-OS</span></span>
<span data-ttu-id="bfb96-147">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bfb96-147">Specifies the operating system family.</span></span>
<span data-ttu-id="bfb96-148">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="bfb96-148">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-149">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="bfb96-149">-OSDiskName</span></span>
<span data-ttu-id="bfb96-150">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bfb96-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="bfb96-151">-ProcessServer</span></span>
<span data-ttu-id="bfb96-152">O servidor de processo a ser usado para replicar este computador.</span><span class="sxs-lookup"><span data-stu-id="bfb96-152">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="bfb96-153">Use a lista de servidores de processo na malha ASR correspondente ao servidor de configuração para especificar um.</span><span class="sxs-lookup"><span data-stu-id="bfb96-153">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-154">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-154">-ProtectableItem</span></span>
<span data-ttu-id="bfb96-155">Especifica o objeto de item protectable ASR para o qual a replicação está sendo habilitada.</span><span class="sxs-lookup"><span data-stu-id="bfb96-155">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-156">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bfb96-156">-ProtectionContainerMapping</span></span>
<span data-ttu-id="bfb96-157">Especifica o objeto de mapeamento de contêiner de proteção ASR correspondente à política de replicação a ser usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-157">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-158">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="bfb96-158">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="bfb96-159">A ID do Availabilityset para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="bfb96-159">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-160">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="bfb96-160">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="bfb96-161">A ID da rede virtual do Azure para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="bfb96-161">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-162">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bfb96-162">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bfb96-163">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="bfb96-163">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-164">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="bfb96-164">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="bfb96-165">A sub-rede dentro da rede virtual de recuperação do Azure à qual a máquina virtual com failover deve ser anexada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="bfb96-165">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-166">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="bfb96-166">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="bfb96-167">Especifica a ID do recurso de recuperação do serviço de nuvem para a qual essa máquina virtual se desfailoveru.</span><span class="sxs-lookup"><span data-stu-id="bfb96-167">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-168">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bfb96-168">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="bfb96-169">Especifica o identificador de braço do grupo de recursos no qual a máquina virtual será criada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="bfb96-169">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-170">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="bfb96-170">-RecoveryVmName</span></span>
<span data-ttu-id="bfb96-171">Nome da VM de recuperação criada após o failover.</span><span class="sxs-lookup"><span data-stu-id="bfb96-171">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-172">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb96-172">-ReplicationGroupName</span></span>
<span data-ttu-id="bfb96-173">Especifica o nome do grupo de replicação a ser usado para criar pontos de recuperação consistentes de várias VMS.</span><span class="sxs-lookup"><span data-stu-id="bfb96-173">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="bfb96-174">Por padrão, cada item de replicação protegida é criado em um grupo de pontos de recuperação consistentes e com várias VMs não gerados.</span><span class="sxs-lookup"><span data-stu-id="bfb96-174">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="bfb96-175">Use essa opção somente se você precisar criar pontos de recuperação consistentes de várias VMs em um grupo de máquinas ao proteger todas as máquinas ao mesmo grupo de replicação.</span><span class="sxs-lookup"><span data-stu-id="bfb96-175">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-176">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bfb96-176">-VMwareToAzure</span></span>
<span data-ttu-id="bfb96-177">Parâmetro de opção para especificar o item replicado é uma máquina virtual do VMware ou um servidor físico que será replicado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb96-177">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-178">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="bfb96-178">-VmmToVmm</span></span>
<span data-ttu-id="bfb96-179">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada entre sites do Hyper-V gerenciados pelo VMM.</span><span class="sxs-lookup"><span data-stu-id="bfb96-179">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-180">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="bfb96-180">-WaitForCompletion</span></span>
<span data-ttu-id="bfb96-181">Especifica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="bfb96-181">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb96-182">-WhatIf</span></span>
<span data-ttu-id="bfb96-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfb96-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb96-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfb96-184">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb96-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb96-185">CommonParameters</span></span>
<span data-ttu-id="bfb96-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb96-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb96-187">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb96-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb96-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfb96-188">INPUTS</span></span>

### <span data-ttu-id="bfb96-189">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-189">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="bfb96-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfb96-190">OUTPUTS</span></span>

### <span data-ttu-id="bfb96-191">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bfb96-191">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bfb96-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfb96-192">NOTES</span></span>

## <span data-ttu-id="bfb96-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb96-193">RELATED LINKS</span></span>

[<span data-ttu-id="bfb96-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-194">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="bfb96-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-195">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="bfb96-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bfb96-196">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
