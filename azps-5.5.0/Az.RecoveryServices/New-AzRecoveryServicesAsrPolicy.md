---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114559"
---
# <span data-ttu-id="71350-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="71350-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="71350-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71350-102">SYNOPSIS</span></span>
<span data-ttu-id="71350-103">Cria uma política de replicação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="71350-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="71350-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71350-104">SYNTAX</span></span>

### <span data-ttu-id="71350-105">HyperVToAzure (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71350-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71350-106">V LtdIToAzure</span><span class="sxs-lookup"><span data-stu-id="71350-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71350-107">AzureToV Ltd</span><span class="sxs-lookup"><span data-stu-id="71350-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71350-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="71350-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71350-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="71350-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71350-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="71350-110">DESCRIPTION</span></span>
<span data-ttu-id="71350-111">O **cmdlet New-AzRecoveryServicesAsrPolicy** cria uma política de replicação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="71350-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="71350-112">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="71350-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="71350-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71350-113">EXAMPLES</span></span>

### <span data-ttu-id="71350-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71350-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="71350-115">Inicia a operação de criação de política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="71350-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="71350-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="71350-116">Example 2</span></span>
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

<span data-ttu-id="71350-117">Inicia a operação de criação de política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="71350-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="71350-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="71350-118">Example 3</span></span>
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

### <span data-ttu-id="71350-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="71350-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="71350-120">Inicia a operação de criação de política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="71350-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="71350-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71350-121">PARAMETERS</span></span>

### <span data-ttu-id="71350-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="71350-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="71350-123">Especifica a frequência(em horas) na qual se cria pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71350-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="71350-124">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="71350-124">-Authentication</span></span>
<span data-ttu-id="71350-125">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="71350-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="71350-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="71350-126">Valid values are:</span></span>

- <span data-ttu-id="71350-127">Certificado</span><span class="sxs-lookup"><span data-stu-id="71350-127">Certificate</span></span>
-  <span data-ttu-id="71350-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="71350-128">Kerberos</span></span>

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

### <span data-ttu-id="71350-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="71350-129">-AzureToAzure</span></span>
<span data-ttu-id="71350-130">A opção parâmetro especifica o cenário do azure para a criação de política do Azure.</span><span class="sxs-lookup"><span data-stu-id="71350-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="71350-131">-AzureToV Ltd</span><span class="sxs-lookup"><span data-stu-id="71350-131">-AzureToVMware</span></span>
<span data-ttu-id="71350-132">A opção parâmetro especifica o cenário para a criação de política do azure para vMWare.</span><span class="sxs-lookup"><span data-stu-id="71350-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="71350-133">-Compactação</span><span class="sxs-lookup"><span data-stu-id="71350-133">-Compression</span></span>
<span data-ttu-id="71350-134">Especifica se a compactação deve estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="71350-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="71350-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71350-135">-DefaultProfile</span></span>
<span data-ttu-id="71350-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71350-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71350-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="71350-137">-HyperVToAzure</span></span>
<span data-ttu-id="71350-138">Alternar parâmetro para especificar a política deve ser usada para replicar máquinas virtuais Hyper-V para o Azure</span><span class="sxs-lookup"><span data-stu-id="71350-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="71350-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="71350-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="71350-140">Especifica o status de sincronização multiVm para a política.</span><span class="sxs-lookup"><span data-stu-id="71350-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="71350-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="71350-141">-Name</span></span>
<span data-ttu-id="71350-142">Especifica o nome da política de replicação asR.</span><span class="sxs-lookup"><span data-stu-id="71350-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="71350-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="71350-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="71350-144">Especifica os pontos de recuperação de número a manter.</span><span class="sxs-lookup"><span data-stu-id="71350-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="71350-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71350-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="71350-146">Especifica a ID da conta de armazenamento do Azure para a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="71350-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="71350-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="71350-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="71350-148">Mantenha os pontos de recuperação por determinado tempo em horas.</span><span class="sxs-lookup"><span data-stu-id="71350-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="71350-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="71350-149">-ReplicaDeletion</span></span>
<span data-ttu-id="71350-150">Especifica se a máquina virtual de réplica deve ser excluída na desabilitação da replicação de um site gerenciado de VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="71350-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="71350-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="71350-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="71350-152">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="71350-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="71350-153">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="71350-153">Valid values are:</span></span>

- <span data-ttu-id="71350-154">30</span><span class="sxs-lookup"><span data-stu-id="71350-154">30</span></span>
- <span data-ttu-id="71350-155">300</span><span class="sxs-lookup"><span data-stu-id="71350-155">300</span></span>
- <span data-ttu-id="71350-156">900</span><span class="sxs-lookup"><span data-stu-id="71350-156">900</span></span>

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

### <span data-ttu-id="71350-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="71350-157">-ReplicationMethod</span></span>
<span data-ttu-id="71350-158">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="71350-158">Specifies the replication method.</span></span>
<span data-ttu-id="71350-159">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="71350-159">Valid values are:</span></span>

- <span data-ttu-id="71350-160">Online</span><span class="sxs-lookup"><span data-stu-id="71350-160">Online</span></span>
- <span data-ttu-id="71350-161">Offline</span><span class="sxs-lookup"><span data-stu-id="71350-161">Offline</span></span>

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

### <span data-ttu-id="71350-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="71350-162">-ReplicationPort</span></span>
<span data-ttu-id="71350-163">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="71350-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="71350-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="71350-164">-ReplicationProvider</span></span>
<span data-ttu-id="71350-165">Especifica o provedor de replicação da política.</span><span class="sxs-lookup"><span data-stu-id="71350-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="71350-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="71350-166">-ReplicationStartTime</span></span>
<span data-ttu-id="71350-167">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="71350-167">Specifies the replication start time.</span></span>
<span data-ttu-id="71350-168">Não deve ser mais do que 24 horas a partir do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="71350-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="71350-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="71350-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="71350-170">O valor limite de RPO em minutos para avisar.</span><span class="sxs-lookup"><span data-stu-id="71350-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="71350-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="71350-171">-VmmToVmm</span></span>
<span data-ttu-id="71350-172">Alternar parâmetro para especificar a política deve ser usada para replicar entre sites HiperV gerenciados por um servidor VMM.</span><span class="sxs-lookup"><span data-stu-id="71350-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="71350-173">-V FazerAzure</span><span class="sxs-lookup"><span data-stu-id="71350-173">-VMwareToAzure</span></span>
<span data-ttu-id="71350-174">Alternar o parâmetro especificando que a política de replicação que está sendo criada será usada para replicar máquinas virtuais VLique e/ou servidores físicos para o Azure.</span><span class="sxs-lookup"><span data-stu-id="71350-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="71350-175">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="71350-175">-Confirm</span></span>
<span data-ttu-id="71350-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71350-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71350-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71350-177">-WhatIf</span></span>
<span data-ttu-id="71350-178">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="71350-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71350-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71350-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71350-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71350-180">CommonParameters</span></span>
<span data-ttu-id="71350-181">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71350-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71350-182">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71350-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71350-183">Entradas</span><span class="sxs-lookup"><span data-stu-id="71350-183">INPUTS</span></span>

### <span data-ttu-id="71350-184">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71350-184">None</span></span>

## <span data-ttu-id="71350-185">Saídas</span><span class="sxs-lookup"><span data-stu-id="71350-185">OUTPUTS</span></span>

### <span data-ttu-id="71350-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="71350-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71350-187">Notas</span><span class="sxs-lookup"><span data-stu-id="71350-187">NOTES</span></span>

## <span data-ttu-id="71350-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71350-188">RELATED LINKS</span></span>

[<span data-ttu-id="71350-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="71350-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="71350-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="71350-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
