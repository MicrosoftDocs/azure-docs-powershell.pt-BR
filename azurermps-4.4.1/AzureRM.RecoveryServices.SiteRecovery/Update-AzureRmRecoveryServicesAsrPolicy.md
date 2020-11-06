---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433033"
---
# <span data-ttu-id="476ee-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="476ee-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="476ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="476ee-102">SYNOPSIS</span></span>
<span data-ttu-id="476ee-103">Atualiza uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="476ee-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="476ee-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="476ee-105">DESCRIPTION</span></span>
<span data-ttu-id="476ee-106">O cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** atualiza a política de replicação do Azure site Recovery especificada.</span><span class="sxs-lookup"><span data-stu-id="476ee-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="476ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="476ee-107">EXAMPLES</span></span>

### <span data-ttu-id="476ee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="476ee-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="476ee-109">Inicia a operação atualizar política de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="476ee-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="476ee-110">OS</span><span class="sxs-lookup"><span data-stu-id="476ee-110">PARAMETERS</span></span>

### <span data-ttu-id="476ee-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="476ee-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="476ee-112">Especifica a frequência (em horas) na qual criar pontos de recuperação consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="476ee-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="476ee-113">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="476ee-113">-Authentication</span></span>
<span data-ttu-id="476ee-114">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="476ee-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="476ee-115">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="476ee-115">Valid values are:</span></span>

- <span data-ttu-id="476ee-116">Certificado</span><span class="sxs-lookup"><span data-stu-id="476ee-116">Certificate</span></span>
-  <span data-ttu-id="476ee-117">V5</span><span class="sxs-lookup"><span data-stu-id="476ee-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-118">-Compactação</span><span class="sxs-lookup"><span data-stu-id="476ee-118">-Compression</span></span>
<span data-ttu-id="476ee-119">Especifica se a compactação deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="476ee-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-120">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="476ee-120">-Encryption</span></span>
<span data-ttu-id="476ee-121">Especifica se a criptografia deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="476ee-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="476ee-122">-InputObject</span></span>
<span data-ttu-id="476ee-123">Objeto de entrada para o cmdlet: especifica o objeto da política de replicação ASR correspondente à política de replicação a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="476ee-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="476ee-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="476ee-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="476ee-125">Especifica o número de pontos de recuperação a serem mantidos.</span><span class="sxs-lookup"><span data-stu-id="476ee-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="476ee-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="476ee-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="476ee-127">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="476ee-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="476ee-128">Usado como a conta de armazenamento de destino para replicação se uma alternativa não for fornecida ao habilitar a replicação usando o cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="476ee-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="476ee-129">-ReplicaDeletion</span></span>
<span data-ttu-id="476ee-130">Especifica se a máquina virtual de réplica deve ser excluída ao desabilitar a replicação de um site gerenciado pelo VMM para outro.</span><span class="sxs-lookup"><span data-stu-id="476ee-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="476ee-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="476ee-132">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="476ee-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="476ee-133">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="476ee-133">Valid values are:</span></span>

- <span data-ttu-id="476ee-134">30</span><span class="sxs-lookup"><span data-stu-id="476ee-134">30</span></span>
- <span data-ttu-id="476ee-135">300</span><span class="sxs-lookup"><span data-stu-id="476ee-135">300</span></span>
- <span data-ttu-id="476ee-136">900</span><span class="sxs-lookup"><span data-stu-id="476ee-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="476ee-137">-ReplicationMethod</span></span>
<span data-ttu-id="476ee-138">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="476ee-138">Specifies the replication method.</span></span>
<span data-ttu-id="476ee-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="476ee-139">Valid values are:</span></span>

- <span data-ttu-id="476ee-140">Internet</span><span class="sxs-lookup"><span data-stu-id="476ee-140">Online</span></span>
- <span data-ttu-id="476ee-141">Modo</span><span class="sxs-lookup"><span data-stu-id="476ee-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="476ee-142">-ReplicationPort</span></span>
<span data-ttu-id="476ee-143">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="476ee-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476ee-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="476ee-144">-ReplicationStartTime</span></span>
<span data-ttu-id="476ee-145">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="476ee-145">Specifies the replication start time.</span></span>
<span data-ttu-id="476ee-146">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="476ee-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="476ee-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="476ee-147">-Confirm</span></span>
<span data-ttu-id="476ee-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476ee-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476ee-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476ee-149">-WhatIf</span></span>
<span data-ttu-id="476ee-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="476ee-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="476ee-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="476ee-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476ee-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476ee-152">CommonParameters</span></span>
<span data-ttu-id="476ee-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476ee-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476ee-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476ee-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476ee-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="476ee-155">INPUTS</span></span>

### <span data-ttu-id="476ee-156">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="476ee-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="476ee-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="476ee-157">OUTPUTS</span></span>

### <span data-ttu-id="476ee-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="476ee-158">System.Object</span></span>

## <span data-ttu-id="476ee-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="476ee-159">NOTES</span></span>

## <span data-ttu-id="476ee-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="476ee-160">RELATED LINKS</span></span>

