---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945891"
---
# <span data-ttu-id="7f712-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="7f712-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="7f712-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f712-102">SYNOPSIS</span></span>
<span data-ttu-id="7f712-103">Cria um objeto de perfil de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7f712-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="7f712-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f712-104">SYNTAX</span></span>

### <span data-ttu-id="7f712-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f712-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7f712-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7f712-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f712-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f712-107">DESCRIPTION</span></span>
<span data-ttu-id="7f712-108">O cmdlet **New-AzureSiteRecoveryProtectionProfileObject** cria um objeto de perfil de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7f712-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="7f712-109">Esse cmdlet cria um objeto **ASRProtectionProfile** para usar com outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7f712-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="7f712-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f712-110">EXAMPLES</span></span>

### <span data-ttu-id="7f712-111">Exemplo 1: criar um perfil de proteção</span><span class="sxs-lookup"><span data-stu-id="7f712-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="7f712-112">Esse comando cria um objeto de perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="7f712-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="7f712-113">Exemplo 2: criar um perfil de proteção para o provedor de HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="7f712-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="7f712-114">Esse comando cria um perfil de proteção para um provedor de HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="7f712-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="7f712-115">OS</span><span class="sxs-lookup"><span data-stu-id="7f712-115">PARAMETERS</span></span>

### <span data-ttu-id="7f712-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="7f712-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="7f712-117">Indica que o perfil de proteção permite a exclusão de entidades de réplica.</span><span class="sxs-lookup"><span data-stu-id="7f712-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="7f712-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="7f712-119">Especifica a frequência, em horas, para instantâneos consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f712-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="7f712-120">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="7f712-120">-Authentication</span></span>
<span data-ttu-id="7f712-121">Especifica o tipo de autenticação a ser usado.</span><span class="sxs-lookup"><span data-stu-id="7f712-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="7f712-122">Os valores aceitáveis para esse parâmetro são: Certificate e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7f712-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="7f712-123">-CompressionEnabled</span></span>
<span data-ttu-id="7f712-124">Indica que o perfil de proteção permite compactação.</span><span class="sxs-lookup"><span data-stu-id="7f712-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7f712-125">-Force</span></span>
<span data-ttu-id="7f712-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7f712-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f712-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f712-127">-Name</span></span>
<span data-ttu-id="7f712-128">Especifica um nome para o perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="7f712-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="7f712-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7f712-129">-Profile</span></span>
<span data-ttu-id="7f712-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7f712-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f712-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7f712-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7f712-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="7f712-133">Especifica o nome de uma conta de armazenamento do Azure na qual armazenar a entidade da réplica do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f712-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7f712-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="7f712-135">Especifica a ID de uma assinatura do Azure para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f712-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="7f712-136">Esse parâmetro se refere à conta em que será armazenada a entidade de réplica do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f712-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="7f712-137">-RecoveryPoints</span></span>
<span data-ttu-id="7f712-138">Especifica o número de horas para manter os pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7f712-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="7f712-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="7f712-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="7f712-140">Especifica o intervalo de frequência, em segundos, para replicação.</span><span class="sxs-lookup"><span data-stu-id="7f712-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="7f712-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f712-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f712-142">30</span><span class="sxs-lookup"><span data-stu-id="7f712-142">30</span></span> 
- <span data-ttu-id="7f712-143">300</span><span class="sxs-lookup"><span data-stu-id="7f712-143">300</span></span> 
- <span data-ttu-id="7f712-144">900</span><span class="sxs-lookup"><span data-stu-id="7f712-144">900</span></span>

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

### <span data-ttu-id="7f712-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="7f712-145">-ReplicationMethod</span></span>
<span data-ttu-id="7f712-146">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="7f712-146">Specifies the replication method.</span></span> <span data-ttu-id="7f712-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f712-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f712-148">Internet.</span><span class="sxs-lookup"><span data-stu-id="7f712-148">Online.</span></span>
<span data-ttu-id="7f712-149">Replicação pela rede.</span><span class="sxs-lookup"><span data-stu-id="7f712-149">Replication over the network.</span></span>
- <span data-ttu-id="7f712-150">Modo.</span><span class="sxs-lookup"><span data-stu-id="7f712-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f712-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="7f712-151">-ReplicationPort</span></span>
<span data-ttu-id="7f712-152">Especifica o número da porta na qual a replicação ocorre.</span><span class="sxs-lookup"><span data-stu-id="7f712-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="7f712-153">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="7f712-153">-ReplicationProvider</span></span>
<span data-ttu-id="7f712-154">Especifica o tipo de provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="7f712-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="7f712-155">Os valores aceitáveis para esse parâmetro são: HyperVReplica e HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="7f712-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="7f712-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="7f712-156">-ReplicationStartTime</span></span>
<span data-ttu-id="7f712-157">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="7f712-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="7f712-158">Especifique um horário dentro de 24 horas depois de iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="7f712-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="7f712-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f712-159">CommonParameters</span></span>
<span data-ttu-id="7f712-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f712-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f712-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f712-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f712-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f712-162">INPUTS</span></span>

## <span data-ttu-id="7f712-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f712-163">OUTPUTS</span></span>

## <span data-ttu-id="7f712-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f712-164">NOTES</span></span>

## <span data-ttu-id="7f712-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f712-165">RELATED LINKS</span></span>

[<span data-ttu-id="7f712-166">Cmdlets de serviços de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="7f712-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


