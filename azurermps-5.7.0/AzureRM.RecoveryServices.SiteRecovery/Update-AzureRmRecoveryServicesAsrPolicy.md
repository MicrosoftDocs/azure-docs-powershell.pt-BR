---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426636"
---
# <span data-ttu-id="73750-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="73750-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="73750-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73750-102">SYNOPSIS</span></span>
<span data-ttu-id="73750-103">Atualiza uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73750-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73750-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73750-104">SYNTAX</span></span>

### <span data-ttu-id="73750-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="73750-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73750-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73750-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73750-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="73750-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73750-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73750-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="73750-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73750-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73750-111">DESCRIPTION</span></span>
<span data-ttu-id="73750-112">O cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** atualiza a política de replicação do Azure site Recovery especificada.</span><span class="sxs-lookup"><span data-stu-id="73750-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="73750-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73750-113">EXAMPLES</span></span>

### <span data-ttu-id="73750-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73750-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="73750-115">Inicia a operação atualizar política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="73750-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="73750-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="73750-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="73750-117">Inicia a operação atualizar o Azure para a política de replicação do Azure usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="73750-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="73750-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="73750-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="73750-119">Inicia a política atualizar o Azure para replicação do Azure usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="73750-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="73750-120">OS</span><span class="sxs-lookup"><span data-stu-id="73750-120">PARAMETERS</span></span>

### <span data-ttu-id="73750-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="73750-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="73750-122">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73750-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-123">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="73750-123">-Authentication</span></span>
<span data-ttu-id="73750-124">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="73750-124">Specifies the type of authentication used.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-125">-AzureToAzure</span></span>
<span data-ttu-id="73750-126">Parâmetro de alternância especificando que a política de replicação usada para replicar máquinas virtuais do Azure entre duas regiões do Azure será atualizada.</span><span class="sxs-lookup"><span data-stu-id="73750-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="73750-127">-AzureToVMware</span></span>
<span data-ttu-id="73750-128">Parâmetro de opção que indica que a política especificada é usada para replicar falhas em máquinas virtuais executadas no Azure de volta a um site do VMware local.</span><span class="sxs-lookup"><span data-stu-id="73750-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-129">-Compactação</span><span class="sxs-lookup"><span data-stu-id="73750-129">-Compression</span></span>
<span data-ttu-id="73750-130">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="73750-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73750-131">-Confirm</span></span>
<span data-ttu-id="73750-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73750-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73750-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73750-133">-DefaultProfile</span></span>
<span data-ttu-id="73750-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73750-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="73750-135">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="73750-135">-Encryption</span></span>
<span data-ttu-id="73750-136">Especifica se a criptografia deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="73750-136">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-137">-HyperVToAzure</span></span>
<span data-ttu-id="73750-138">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do Hyper-V para o Azure.</span><span class="sxs-lookup"><span data-stu-id="73750-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73750-139">-InputObject</span></span>
<span data-ttu-id="73750-140">Objeto de entrada para o cmdlet: especifica o objeto da política de replicação ASR correspondente à política de replicação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="73750-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73750-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="73750-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="73750-142">Especifica o status de sincronização do multiVm para a política.</span><span class="sxs-lookup"><span data-stu-id="73750-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="73750-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="73750-144">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="73750-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="73750-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="73750-146">O valor de limite de RPO em minutos para avisar.</span><span class="sxs-lookup"><span data-stu-id="73750-146">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="73750-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="73750-148">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="73750-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="73750-149">Usado como a conta de armazenamento de destino para replicação se uma alternativa não for fornecida ao habilitar a replicação usando o cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="73750-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-150">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="73750-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="73750-151">Tempo em horas para manter os pontos de recuperação após a criação.</span><span class="sxs-lookup"><span data-stu-id="73750-151">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-152">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="73750-152">-ReplicaDeletion</span></span>
<span data-ttu-id="73750-153">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="73750-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="73750-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="73750-155">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="73750-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="73750-156">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="73750-156">Valid values are:</span></span>

- <span data-ttu-id="73750-157">30</span><span class="sxs-lookup"><span data-stu-id="73750-157">30</span></span>
- <span data-ttu-id="73750-158">300</span><span class="sxs-lookup"><span data-stu-id="73750-158">300</span></span>
- <span data-ttu-id="73750-159">900</span><span class="sxs-lookup"><span data-stu-id="73750-159">900</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="73750-160">-ReplicationMethod</span></span>
<span data-ttu-id="73750-161">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="73750-161">Specifies the replication method.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="73750-162">-ReplicationPort</span></span>
<span data-ttu-id="73750-163">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="73750-163">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="73750-164">-ReplicationStartTime</span></span>
<span data-ttu-id="73750-165">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="73750-165">Specifies the replication start time.</span></span>
<span data-ttu-id="73750-166">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="73750-166">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="73750-167">-VMwareToAzure</span></span>
<span data-ttu-id="73750-168">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="73750-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="73750-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="73750-169">-VmmToVmm</span></span>
<span data-ttu-id="73750-170">Parâmetro de opção que indica que a política especificada é usada para replicar máquinas virtuais do Hyper-V gerenciados pelo VMM entre dois sites do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="73750-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73750-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73750-171">-WhatIf</span></span>
<span data-ttu-id="73750-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73750-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73750-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73750-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73750-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73750-174">CommonParameters</span></span>
<span data-ttu-id="73750-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73750-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73750-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73750-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73750-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73750-177">INPUTS</span></span>

### <span data-ttu-id="73750-178">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="73750-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="73750-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73750-179">OUTPUTS</span></span>

### <span data-ttu-id="73750-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="73750-180">System.Object</span></span>

## <span data-ttu-id="73750-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73750-181">NOTES</span></span>

## <span data-ttu-id="73750-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73750-182">RELATED LINKS</span></span>
