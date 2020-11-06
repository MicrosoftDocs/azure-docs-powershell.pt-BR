---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426301"
---
# <span data-ttu-id="9c54b-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9c54b-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="9c54b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c54b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c54b-103">Cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9c54b-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c54b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c54b-104">SYNTAX</span></span>

### <span data-ttu-id="9c54b-105">HyperVToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c54b-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c54b-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9c54b-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c54b-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9c54b-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c54b-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9c54b-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c54b-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9c54b-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c54b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c54b-110">DESCRIPTION</span></span>
<span data-ttu-id="9c54b-111">O cmdlet **New-AzureRmRecoveryServicesAsrPolicy** cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9c54b-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="9c54b-112">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="9c54b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c54b-113">EXAMPLES</span></span>

### <span data-ttu-id="9c54b-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c54b-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="9c54b-115">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9c54b-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c54b-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="9c54b-117">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9c54b-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9c54b-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="9c54b-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9c54b-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="9c54b-120">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9c54b-121">OS</span><span class="sxs-lookup"><span data-stu-id="9c54b-121">PARAMETERS</span></span>

### <span data-ttu-id="9c54b-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="9c54b-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="9c54b-123">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9c54b-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-124">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="9c54b-124">-Authentication</span></span>
<span data-ttu-id="9c54b-125">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="9c54b-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="9c54b-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c54b-126">Valid values are:</span></span>

- <span data-ttu-id="9c54b-127">Certificado</span><span class="sxs-lookup"><span data-stu-id="9c54b-127">Certificate</span></span>
-  <span data-ttu-id="9c54b-128">V5</span><span class="sxs-lookup"><span data-stu-id="9c54b-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="9c54b-129">-AzureToAzure</span></span>
<span data-ttu-id="9c54b-130">Parâmetro de alternância especificando que a política de replicação que está sendo criada será usada para máquinas virtuais do Azure replicadas entre duas regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c54b-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="9c54b-131">-AzureToVMware</span></span>
<span data-ttu-id="9c54b-132">Parâmetro de alternância especificando que a política de replicação que está sendo criada será usada para reverter a replicação com máquinas virtuais VMware e servidores físicos executados no Azure de volta a um site do VMware local.</span><span class="sxs-lookup"><span data-stu-id="9c54b-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="9c54b-133">-Compactação</span><span class="sxs-lookup"><span data-stu-id="9c54b-133">-Compression</span></span>
<span data-ttu-id="9c54b-134">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="9c54b-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c54b-135">-DefaultProfile</span></span>
<span data-ttu-id="9c54b-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c54b-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9c54b-137">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="9c54b-137">-Encryption</span></span>
<span data-ttu-id="9c54b-138">{{Descrição da criptografia de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="9c54b-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="9c54b-139">-HyperVToAzure</span></span>
<span data-ttu-id="9c54b-140">O parâmetro de opção para especificar a política deve ser usado para replicar máquinas virtuais do Hyper-V para o Azure</span><span class="sxs-lookup"><span data-stu-id="9c54b-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="9c54b-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="9c54b-142">Especifica o status de sincronização do multiVm para a política.</span><span class="sxs-lookup"><span data-stu-id="9c54b-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c54b-143">-Name</span></span>
<span data-ttu-id="9c54b-144">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="9c54b-144">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="9c54b-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="9c54b-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="9c54b-146">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="9c54b-146">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9c54b-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="9c54b-148">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="9c54b-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="9c54b-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="9c54b-150">Manter os pontos de recuperação para um determinado momento em horas.</span><span class="sxs-lookup"><span data-stu-id="9c54b-150">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="9c54b-151">-ReplicaDeletion</span></span>
<span data-ttu-id="9c54b-152">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="9c54b-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="9c54b-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="9c54b-154">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="9c54b-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="9c54b-155">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c54b-155">Valid values are:</span></span>

- <span data-ttu-id="9c54b-156">30</span><span class="sxs-lookup"><span data-stu-id="9c54b-156">30</span></span>
- <span data-ttu-id="9c54b-157">300</span><span class="sxs-lookup"><span data-stu-id="9c54b-157">300</span></span>
- <span data-ttu-id="9c54b-158">900</span><span class="sxs-lookup"><span data-stu-id="9c54b-158">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="9c54b-159">-ReplicationMethod</span></span>
<span data-ttu-id="9c54b-160">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-160">Specifies the replication method.</span></span>
<span data-ttu-id="9c54b-161">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c54b-161">Valid values are:</span></span>

- <span data-ttu-id="9c54b-162">Internet</span><span class="sxs-lookup"><span data-stu-id="9c54b-162">Online</span></span>
- <span data-ttu-id="9c54b-163">Modo</span><span class="sxs-lookup"><span data-stu-id="9c54b-163">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="9c54b-164">-ReplicationPort</span></span>
<span data-ttu-id="9c54b-165">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-165">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-166">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="9c54b-166">-ReplicationProvider</span></span>
<span data-ttu-id="9c54b-167">Especifica o provedor de replicação da política.</span><span class="sxs-lookup"><span data-stu-id="9c54b-167">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="9c54b-168">-ReplicationStartTime</span></span>
<span data-ttu-id="9c54b-169">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="9c54b-169">Specifies the replication start time.</span></span>
<span data-ttu-id="9c54b-170">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9c54b-170">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="9c54b-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="9c54b-172">O valor de limite de RPO em minutos para avisar.</span><span class="sxs-lookup"><span data-stu-id="9c54b-172">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c54b-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="9c54b-173">-VmmToVmm</span></span>
<span data-ttu-id="9c54b-174">O parâmetro de opção para especificar a política deve ser usado para replicação entre sites do Hyper-V gerenciados por um servidor VMM.</span><span class="sxs-lookup"><span data-stu-id="9c54b-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="9c54b-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="9c54b-175">-VMwareToAzure</span></span>
<span data-ttu-id="9c54b-176">Parâmetro de alternância especificando que a política de replicação que está sendo criada será usada para replicar máquinas virtuais do VMware e/ou servidores físicos para o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c54b-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="9c54b-177">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c54b-177">-Confirm</span></span>
<span data-ttu-id="9c54b-178">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c54b-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c54b-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c54b-179">-WhatIf</span></span>
<span data-ttu-id="9c54b-180">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c54b-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c54b-181">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c54b-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c54b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c54b-182">CommonParameters</span></span>
<span data-ttu-id="9c54b-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c54b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c54b-184">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c54b-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c54b-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c54b-185">INPUTS</span></span>

### <span data-ttu-id="9c54b-186">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c54b-186">None</span></span>

## <span data-ttu-id="9c54b-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c54b-187">OUTPUTS</span></span>

### <span data-ttu-id="9c54b-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="9c54b-188">System.Object</span></span>

## <span data-ttu-id="9c54b-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c54b-189">NOTES</span></span>

## <span data-ttu-id="9c54b-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c54b-190">RELATED LINKS</span></span>

[<span data-ttu-id="9c54b-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9c54b-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="9c54b-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9c54b-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
