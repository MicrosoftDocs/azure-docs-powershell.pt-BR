---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 98031226919b143431206fd9e3b512e6c653b8a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772977"
---
# <span data-ttu-id="97a59-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="97a59-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="97a59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97a59-102">SYNOPSIS</span></span>
<span data-ttu-id="97a59-103">Cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="97a59-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="97a59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97a59-104">SYNTAX</span></span>

### <span data-ttu-id="97a59-105">HyperVToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="97a59-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a59-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="97a59-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a59-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="97a59-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a59-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="97a59-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a59-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="97a59-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a59-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97a59-110">DESCRIPTION</span></span>
<span data-ttu-id="97a59-111">O cmdlet **New-AzRecoveryServicesAsrPolicy** cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="97a59-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="97a59-112">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="97a59-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="97a59-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97a59-113">EXAMPLES</span></span>

### <span data-ttu-id="97a59-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97a59-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="97a59-115">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="97a59-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="97a59-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97a59-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="97a59-117">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="97a59-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="97a59-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="97a59-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="97a59-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="97a59-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="97a59-120">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="97a59-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="97a59-121">OS</span><span class="sxs-lookup"><span data-stu-id="97a59-121">PARAMETERS</span></span>

### <span data-ttu-id="97a59-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="97a59-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="97a59-123">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a59-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="97a59-124">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="97a59-124">-Authentication</span></span>
<span data-ttu-id="97a59-125">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="97a59-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="97a59-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="97a59-126">Valid values are:</span></span>

- <span data-ttu-id="97a59-127">Certificado</span><span class="sxs-lookup"><span data-stu-id="97a59-127">Certificate</span></span>
-  <span data-ttu-id="97a59-128">V5</span><span class="sxs-lookup"><span data-stu-id="97a59-128">Kerberos</span></span>

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

### <span data-ttu-id="97a59-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="97a59-129">-AzureToAzure</span></span>
<span data-ttu-id="97a59-130">{{Fill AzureToAzure descrição}}</span><span class="sxs-lookup"><span data-stu-id="97a59-130">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="97a59-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="97a59-131">-AzureToVMware</span></span>
<span data-ttu-id="97a59-132">{{Fill AzureToVMware descrição}}</span><span class="sxs-lookup"><span data-stu-id="97a59-132">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="97a59-133">-Compactação</span><span class="sxs-lookup"><span data-stu-id="97a59-133">-Compression</span></span>
<span data-ttu-id="97a59-134">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="97a59-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="97a59-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a59-135">-DefaultProfile</span></span>
<span data-ttu-id="97a59-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97a59-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="97a59-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="97a59-137">-HyperVToAzure</span></span>
<span data-ttu-id="97a59-138">O parâmetro de opção para especificar a política deve ser usado para replicar máquinas virtuais do Hyper-V para o Azure</span><span class="sxs-lookup"><span data-stu-id="97a59-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="97a59-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="97a59-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="97a59-140">Especifica o status de sincronização do multiVm para a política.</span><span class="sxs-lookup"><span data-stu-id="97a59-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="97a59-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="97a59-141">-Name</span></span>
<span data-ttu-id="97a59-142">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="97a59-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="97a59-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="97a59-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="97a59-144">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="97a59-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="97a59-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="97a59-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="97a59-146">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="97a59-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="97a59-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="97a59-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="97a59-148">Manter os pontos de recuperação para um determinado momento em horas.</span><span class="sxs-lookup"><span data-stu-id="97a59-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="97a59-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="97a59-149">-ReplicaDeletion</span></span>
<span data-ttu-id="97a59-150">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="97a59-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="97a59-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="97a59-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="97a59-152">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="97a59-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="97a59-153">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="97a59-153">Valid values are:</span></span>

- <span data-ttu-id="97a59-154">30</span><span class="sxs-lookup"><span data-stu-id="97a59-154">30</span></span>
- <span data-ttu-id="97a59-155">300</span><span class="sxs-lookup"><span data-stu-id="97a59-155">300</span></span>
- <span data-ttu-id="97a59-156">900</span><span class="sxs-lookup"><span data-stu-id="97a59-156">900</span></span>

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

### <span data-ttu-id="97a59-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="97a59-157">-ReplicationMethod</span></span>
<span data-ttu-id="97a59-158">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="97a59-158">Specifies the replication method.</span></span>
<span data-ttu-id="97a59-159">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="97a59-159">Valid values are:</span></span>

- <span data-ttu-id="97a59-160">Internet</span><span class="sxs-lookup"><span data-stu-id="97a59-160">Online</span></span>
- <span data-ttu-id="97a59-161">Modo</span><span class="sxs-lookup"><span data-stu-id="97a59-161">Offline</span></span>

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

### <span data-ttu-id="97a59-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="97a59-162">-ReplicationPort</span></span>
<span data-ttu-id="97a59-163">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="97a59-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="97a59-164">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="97a59-164">-ReplicationProvider</span></span>
<span data-ttu-id="97a59-165">Especifica o provedor de replicação da política.</span><span class="sxs-lookup"><span data-stu-id="97a59-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="97a59-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="97a59-166">-ReplicationStartTime</span></span>
<span data-ttu-id="97a59-167">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="97a59-167">Specifies the replication start time.</span></span>
<span data-ttu-id="97a59-168">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="97a59-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="97a59-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="97a59-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="97a59-170">O valor de limite de RPO em minutos para avisar.</span><span class="sxs-lookup"><span data-stu-id="97a59-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="97a59-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="97a59-171">-VmmToVmm</span></span>
<span data-ttu-id="97a59-172">O parâmetro de opção para especificar a política deve ser usado para replicação entre sites do Hyper-V gerenciados por um servidor VMM.</span><span class="sxs-lookup"><span data-stu-id="97a59-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="97a59-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="97a59-173">-VMwareToAzure</span></span>
<span data-ttu-id="97a59-174">Parâmetro de alternância especificando que a política de replicação que está sendo criada será usada para replicar máquinas virtuais do VMware e/ou servidores físicos para o Azure.</span><span class="sxs-lookup"><span data-stu-id="97a59-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="97a59-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97a59-175">-Confirm</span></span>
<span data-ttu-id="97a59-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a59-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a59-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a59-177">-WhatIf</span></span>
<span data-ttu-id="97a59-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97a59-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97a59-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97a59-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a59-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a59-180">CommonParameters</span></span>
<span data-ttu-id="97a59-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a59-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a59-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a59-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a59-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97a59-183">INPUTS</span></span>

### <span data-ttu-id="97a59-184">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97a59-184">None</span></span>

## <span data-ttu-id="97a59-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97a59-185">OUTPUTS</span></span>

### <span data-ttu-id="97a59-186">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="97a59-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97a59-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97a59-187">NOTES</span></span>

## <span data-ttu-id="97a59-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97a59-188">RELATED LINKS</span></span>

[<span data-ttu-id="97a59-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="97a59-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="97a59-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="97a59-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)