---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429168"
---
# <span data-ttu-id="b5dad-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5dad-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b5dad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5dad-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dad-103">Cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b5dad-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5dad-104">SYNTAX</span></span>

### <span data-ttu-id="b5dad-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5dad-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5dad-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b5dad-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5dad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5dad-107">DESCRIPTION</span></span>
<span data-ttu-id="b5dad-108">O cmdlet **New-AzureRmRecoveryServicesAsrPolicy** cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b5dad-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="b5dad-109">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="b5dad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5dad-110">EXAMPLES</span></span>

### <span data-ttu-id="b5dad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5dad-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="b5dad-112">Inicia a operação de criação da política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b5dad-113">OS</span><span class="sxs-lookup"><span data-stu-id="b5dad-113">PARAMETERS</span></span>

### <span data-ttu-id="b5dad-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b5dad-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="b5dad-115">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b5dad-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="b5dad-116">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="b5dad-116">-Authentication</span></span>
<span data-ttu-id="b5dad-117">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="b5dad-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="b5dad-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b5dad-118">Valid values are:</span></span>

- <span data-ttu-id="b5dad-119">Certificado</span><span class="sxs-lookup"><span data-stu-id="b5dad-119">Certificate</span></span>
-  <span data-ttu-id="b5dad-120">V5</span><span class="sxs-lookup"><span data-stu-id="b5dad-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-121">-Compactação</span><span class="sxs-lookup"><span data-stu-id="b5dad-121">-Compression</span></span>
<span data-ttu-id="b5dad-122">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="b5dad-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-123">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="b5dad-123">-Encryption</span></span>
<span data-ttu-id="b5dad-124">Especifica se a criptografia deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b5dad-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5dad-125">-Name</span></span>
<span data-ttu-id="b5dad-126">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="b5dad-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="b5dad-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="b5dad-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="b5dad-128">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="b5dad-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b5dad-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="b5dad-130">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="b5dad-131">Usado como a conta de armazenamento de destino para replicação se uma alternativa não for fornecida ao habilitar a replicação usando o cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="b5dad-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b5dad-132">-ReplicaDeletion</span></span>
<span data-ttu-id="b5dad-133">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="b5dad-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b5dad-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="b5dad-135">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="b5dad-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="b5dad-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b5dad-136">Valid values are:</span></span>

- <span data-ttu-id="b5dad-137">30</span><span class="sxs-lookup"><span data-stu-id="b5dad-137">30</span></span>
- <span data-ttu-id="b5dad-138">300</span><span class="sxs-lookup"><span data-stu-id="b5dad-138">300</span></span>
- <span data-ttu-id="b5dad-139">900</span><span class="sxs-lookup"><span data-stu-id="b5dad-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b5dad-140">-ReplicationMethod</span></span>
<span data-ttu-id="b5dad-141">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-141">Specifies the replication method.</span></span>
<span data-ttu-id="b5dad-142">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b5dad-142">Valid values are:</span></span>

- <span data-ttu-id="b5dad-143">Internet</span><span class="sxs-lookup"><span data-stu-id="b5dad-143">Online</span></span>
- <span data-ttu-id="b5dad-144">Modo</span><span class="sxs-lookup"><span data-stu-id="b5dad-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b5dad-145">-ReplicationPort</span></span>
<span data-ttu-id="b5dad-146">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-147">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="b5dad-147">-ReplicationProvider</span></span>
<span data-ttu-id="b5dad-148">Especifica o provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-148">Specifies the replication provider.</span></span>
<span data-ttu-id="b5dad-149">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b5dad-149">Valid values are:</span></span>

- <span data-ttu-id="b5dad-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="b5dad-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="b5dad-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="b5dad-151">HyperVReplica2012</span></span>
- <span data-ttu-id="b5dad-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="b5dad-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b5dad-153">-ReplicationStartTime</span></span>
<span data-ttu-id="b5dad-154">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="b5dad-154">Specifies the replication start time.</span></span>
<span data-ttu-id="b5dad-155">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b5dad-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dad-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5dad-156">-Confirm</span></span>
<span data-ttu-id="b5dad-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5dad-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5dad-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5dad-158">-WhatIf</span></span>
<span data-ttu-id="b5dad-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5dad-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5dad-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5dad-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5dad-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dad-161">CommonParameters</span></span>
<span data-ttu-id="b5dad-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5dad-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dad-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5dad-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dad-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5dad-164">INPUTS</span></span>

### <span data-ttu-id="b5dad-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b5dad-165">None</span></span>

## <span data-ttu-id="b5dad-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5dad-166">OUTPUTS</span></span>

### <span data-ttu-id="b5dad-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="b5dad-167">System.Object</span></span>

## <span data-ttu-id="b5dad-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5dad-168">NOTES</span></span>

## <span data-ttu-id="b5dad-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5dad-169">RELATED LINKS</span></span>

[<span data-ttu-id="b5dad-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5dad-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="b5dad-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5dad-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
