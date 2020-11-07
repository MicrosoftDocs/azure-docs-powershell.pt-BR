---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6f422bd0207c56f3d834d5ce788e78203a7938e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772651"
---
# <span data-ttu-id="18361-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="18361-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="18361-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18361-102">SYNOPSIS</span></span>
<span data-ttu-id="18361-103">Atualiza uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="18361-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="18361-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18361-104">SYNTAX</span></span>

### <span data-ttu-id="18361-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="18361-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18361-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18361-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18361-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="18361-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18361-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18361-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="18361-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18361-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18361-111">DESCRIPTION</span></span>
<span data-ttu-id="18361-112">O cmdlet **Update-AzRecoveryServicesAsrPolicy** atualiza a política de replicação do Azure site Recovery especificada.</span><span class="sxs-lookup"><span data-stu-id="18361-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="18361-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18361-113">EXAMPLES</span></span>

### <span data-ttu-id="18361-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18361-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="18361-115">Inicia a operação atualizar política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="18361-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="18361-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18361-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="18361-117">Inicia a operação atualizar o Azure para a política de replicação do Azure usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="18361-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="18361-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="18361-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="18361-119">Inicia a política atualizar o Azure para replicação do Azure usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="18361-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="18361-120">OS</span><span class="sxs-lookup"><span data-stu-id="18361-120">PARAMETERS</span></span>

### <span data-ttu-id="18361-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="18361-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="18361-122">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18361-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="18361-123">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="18361-123">-Authentication</span></span>
<span data-ttu-id="18361-124">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="18361-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-125">-AzureToAzure</span></span>
<span data-ttu-id="18361-126">{{Fill AzureToAzure descrição}}</span><span class="sxs-lookup"><span data-stu-id="18361-126">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="18361-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="18361-127">-AzureToVMware</span></span>
<span data-ttu-id="18361-128">{{Fill AzureToVMware descrição}}</span><span class="sxs-lookup"><span data-stu-id="18361-128">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="18361-129">-Compactação</span><span class="sxs-lookup"><span data-stu-id="18361-129">-Compression</span></span>
<span data-ttu-id="18361-130">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="18361-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18361-131">-DefaultProfile</span></span>
<span data-ttu-id="18361-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18361-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="18361-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-133">-HyperVToAzure</span></span>
<span data-ttu-id="18361-134">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do Hyper-V para o Azure.</span><span class="sxs-lookup"><span data-stu-id="18361-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="18361-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18361-135">-InputObject</span></span>
<span data-ttu-id="18361-136">Objeto de entrada para o cmdlet: especifica o objeto da política de replicação ASR correspondente à política de replicação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="18361-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18361-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="18361-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="18361-138">Especifica o status de sincronização do multiVm para a política.</span><span class="sxs-lookup"><span data-stu-id="18361-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="18361-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="18361-140">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="18361-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="18361-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="18361-142">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="18361-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="18361-143">Usado como a conta de armazenamento de destino para replicação se uma alternativa não for fornecida ao habilitar a replicação usando o cmdlet New-AzRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="18361-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="18361-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="18361-145">Tempo em horas para manter os pontos de recuperação após a criação.</span><span class="sxs-lookup"><span data-stu-id="18361-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="18361-146">-ReplicaDeletion</span></span>
<span data-ttu-id="18361-147">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="18361-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="18361-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="18361-149">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="18361-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="18361-150">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="18361-150">Valid values are:</span></span>

- <span data-ttu-id="18361-151">30</span><span class="sxs-lookup"><span data-stu-id="18361-151">30</span></span>
- <span data-ttu-id="18361-152">300</span><span class="sxs-lookup"><span data-stu-id="18361-152">300</span></span>
- <span data-ttu-id="18361-153">900</span><span class="sxs-lookup"><span data-stu-id="18361-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="18361-154">-ReplicationMethod</span></span>
<span data-ttu-id="18361-155">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="18361-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="18361-156">-ReplicationPort</span></span>
<span data-ttu-id="18361-157">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="18361-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="18361-158">-ReplicationStartTime</span></span>
<span data-ttu-id="18361-159">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="18361-159">Specifies the replication start time.</span></span>
<span data-ttu-id="18361-160">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="18361-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="18361-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="18361-162">O valor de limite de RPO em minutos para avisar.</span><span class="sxs-lookup"><span data-stu-id="18361-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18361-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="18361-163">-VmmToVmm</span></span>
<span data-ttu-id="18361-164">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do Hyper-V gerenciados pelo VMM entre dois sites do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="18361-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="18361-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="18361-165">-VMwareToAzure</span></span>
<span data-ttu-id="18361-166">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="18361-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="18361-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18361-167">-Confirm</span></span>
<span data-ttu-id="18361-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18361-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18361-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18361-169">-WhatIf</span></span>
<span data-ttu-id="18361-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18361-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18361-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18361-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18361-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18361-172">CommonParameters</span></span>
<span data-ttu-id="18361-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18361-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18361-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18361-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18361-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18361-175">INPUTS</span></span>

### <span data-ttu-id="18361-176">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="18361-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="18361-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18361-177">OUTPUTS</span></span>

### <span data-ttu-id="18361-178">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="18361-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="18361-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18361-179">NOTES</span></span>

## <span data-ttu-id="18361-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18361-180">RELATED LINKS</span></span>