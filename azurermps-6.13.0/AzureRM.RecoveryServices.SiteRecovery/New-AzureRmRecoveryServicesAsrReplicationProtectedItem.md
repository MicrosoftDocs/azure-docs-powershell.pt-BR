---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426297"
---
# <span data-ttu-id="afa75-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afa75-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="afa75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afa75-102">SYNOPSIS</span></span>
<span data-ttu-id="afa75-103">Habilita a replicação de um item protegido contra ASR criando um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="afa75-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afa75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afa75-104">SYNTAX</span></span>

### <span data-ttu-id="afa75-105">EnterpriseToEnterprise (padrão)</span><span class="sxs-lookup"><span data-stu-id="afa75-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa75-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa75-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa75-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa75-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa75-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="afa75-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa75-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afa75-111">DESCRIPTION</span></span>
<span data-ttu-id="afa75-112">O cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cria um novo item de replicação protegida.</span><span class="sxs-lookup"><span data-stu-id="afa75-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="afa75-113">Use esse cmdlet para habilitar a replicação para um item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="afa75-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="afa75-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afa75-114">EXAMPLES</span></span>

### <span data-ttu-id="afa75-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afa75-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="afa75-116">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="afa75-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="afa75-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="afa75-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="afa75-118">Inicia a operação de criação de itens protegidos de replicação para o item protegido de ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do vmWare para o Azure).</span><span class="sxs-lookup"><span data-stu-id="afa75-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="afa75-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="afa75-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="afa75-120">Inicia a operação de criação de itens protegidos de replicação para o item protegido ASR especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="afa75-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="afa75-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="afa75-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="afa75-122">Inicia a operação de criação de itens protegidos de replicação para o VmId especificado e retorna o trabalho ASR usado para acompanhar a operação (cenário do Azure para o Azure).</span><span class="sxs-lookup"><span data-stu-id="afa75-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="afa75-123">OS</span><span class="sxs-lookup"><span data-stu-id="afa75-123">PARAMETERS</span></span>

### <span data-ttu-id="afa75-124">-Conta</span><span class="sxs-lookup"><span data-stu-id="afa75-124">-Account</span></span>
<span data-ttu-id="afa75-125">A conta Executar como a ser usada para instalar o serviço de mobilidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="afa75-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="afa75-126">Deve ser uma da lista de contas Executar como na malha ASR.</span><span class="sxs-lookup"><span data-stu-id="afa75-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="afa75-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-127">-AzureToAzure</span></span>
<span data-ttu-id="afa75-128">Parâmetro de opção para especificar que o item replicado é uma máquina virtual do Azure que Replica em uma região de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa75-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="afa75-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="afa75-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="afa75-130">Especifica a lista de discos da máquina virtual a ser replicada e a conta de armazenamento do cache e a conta de armazenamento de recuperação a serem usadas para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="afa75-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="afa75-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="afa75-131">-AzureVmId</span></span>
<span data-ttu-id="afa75-132">Especifica a ID da VM do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="afa75-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="afa75-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa75-133">-DefaultProfile</span></span>
<span data-ttu-id="afa75-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afa75-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-135">-HyperVToAzure</span></span>
<span data-ttu-id="afa75-136">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada para o Azure.</span><span class="sxs-lookup"><span data-stu-id="afa75-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="afa75-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="afa75-137">-IncludeDiskId</span></span>
<span data-ttu-id="afa75-138">A lista de discos a serem incluídos para replicação.</span><span class="sxs-lookup"><span data-stu-id="afa75-138">The list of disks to include for replication.</span></span> <span data-ttu-id="afa75-139">Por padrão, todos os discos são incluídos.</span><span class="sxs-lookup"><span data-stu-id="afa75-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="afa75-140">-LogStorageAccountId</span></span>
<span data-ttu-id="afa75-141">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="afa75-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="afa75-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="afa75-142">-Name</span></span>
<span data-ttu-id="afa75-143">Especifica um nome para o item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="afa75-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="afa75-144">O nome deve ser exclusivo no cofre.</span><span class="sxs-lookup"><span data-stu-id="afa75-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="afa75-145">-OS</span><span class="sxs-lookup"><span data-stu-id="afa75-145">-OS</span></span>
<span data-ttu-id="afa75-146">Especifica a família do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="afa75-146">Specifies the operating system family.</span></span>
<span data-ttu-id="afa75-147">Os valores aceitáveis para esse parâmetro são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="afa75-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="afa75-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="afa75-148">-OSDiskName</span></span>
<span data-ttu-id="afa75-149">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="afa75-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="afa75-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="afa75-150">-ProcessServer</span></span>
<span data-ttu-id="afa75-151">O servidor de processo a ser usado para replicar este computador.</span><span class="sxs-lookup"><span data-stu-id="afa75-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="afa75-152">Use a lista de servidores de processo na malha ASR correspondente ao servidor de configuração para especificar um.</span><span class="sxs-lookup"><span data-stu-id="afa75-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="afa75-153">-ProtectableItem</span></span>
<span data-ttu-id="afa75-154">Especifica o objeto de item protectable ASR para o qual a replicação está sendo habilitada.</span><span class="sxs-lookup"><span data-stu-id="afa75-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="afa75-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="afa75-156">Especifica o objeto de mapeamento de contêiner de proteção ASR correspondente à política de replicação a ser usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="afa75-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="afa75-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="afa75-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="afa75-158">A ID do Availabilityset para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="afa75-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="afa75-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="afa75-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="afa75-160">A ID da rede virtual do Azure para recuperar o computador em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="afa75-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="afa75-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="afa75-162">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="afa75-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="afa75-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="afa75-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="afa75-164">A sub-rede dentro da rede virtual de recuperação do Azure à qual a máquina virtual com failover deve ser anexada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="afa75-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="afa75-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="afa75-166">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="afa75-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="afa75-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="afa75-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="afa75-168">Especifica a ID do recurso de recuperação do serviço de nuvem para a qual essa máquina virtual se desfailoveru.</span><span class="sxs-lookup"><span data-stu-id="afa75-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="afa75-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="afa75-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="afa75-170">Especifica o identificador de braço do grupo de recursos no qual a máquina virtual será criada em caso de failover.</span><span class="sxs-lookup"><span data-stu-id="afa75-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="afa75-171">-RecoveryVmName</span></span>
<span data-ttu-id="afa75-172">Nome da VM de recuperação criada após o failover.</span><span class="sxs-lookup"><span data-stu-id="afa75-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="afa75-173">-ReplicationGroupName</span></span>
<span data-ttu-id="afa75-174">Especifica o nome do grupo de replicação a ser usado para criar pontos de recuperação consistentes de várias VMS.</span><span class="sxs-lookup"><span data-stu-id="afa75-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="afa75-175">Por padrão, cada item de replicação protegida é criado em um grupo de pontos de recuperação consistentes e com várias VMs não gerados.</span><span class="sxs-lookup"><span data-stu-id="afa75-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="afa75-176">Use essa opção somente se você precisar criar pontos de recuperação consistentes de várias VMs em um grupo de máquinas ao proteger todas as máquinas ao mesmo grupo de replicação.</span><span class="sxs-lookup"><span data-stu-id="afa75-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afa75-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="afa75-177">-VmmToVmm</span></span>
<span data-ttu-id="afa75-178">Parâmetro de opção para especificar o item replicado é uma máquina virtual Hyper-V que está sendo replicada entre sites do Hyper-V gerenciados pelo VMM.</span><span class="sxs-lookup"><span data-stu-id="afa75-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="afa75-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="afa75-179">-VMwareToAzure</span></span>
<span data-ttu-id="afa75-180">Parâmetro de opção para especificar o item replicado é uma máquina virtual do VMware ou um servidor físico que será replicado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="afa75-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="afa75-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="afa75-181">-WaitForCompletion</span></span>
<span data-ttu-id="afa75-182">Especifica que o cmdlet deve aguardar a conclusão da operação antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="afa75-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="afa75-183">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afa75-183">-Confirm</span></span>
<span data-ttu-id="afa75-184">Solicita confirmação antes de iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="afa75-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="afa75-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa75-185">-WhatIf</span></span>
<span data-ttu-id="afa75-186">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afa75-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa75-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afa75-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa75-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa75-188">CommonParameters</span></span>
<span data-ttu-id="afa75-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa75-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa75-190">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa75-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa75-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afa75-191">INPUTS</span></span>

### <span data-ttu-id="afa75-192">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="afa75-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="afa75-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afa75-193">OUTPUTS</span></span>

### <span data-ttu-id="afa75-194">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="afa75-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="afa75-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afa75-195">NOTES</span></span>

## <span data-ttu-id="afa75-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa75-196">RELATED LINKS</span></span>

[<span data-ttu-id="afa75-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afa75-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="afa75-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afa75-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="afa75-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afa75-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
