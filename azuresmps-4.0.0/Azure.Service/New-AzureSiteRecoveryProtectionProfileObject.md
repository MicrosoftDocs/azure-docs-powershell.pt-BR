---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403639"
---
# <span data-ttu-id="178b8-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="178b8-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="178b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="178b8-102">SYNOPSIS</span></span>
<span data-ttu-id="178b8-103">Cria um objeto de perfil de proteção de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="178b8-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="178b8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="178b8-104">SYNTAX</span></span>

### <span data-ttu-id="178b8-105">EnterpriseToAzure (Padrão)</span><span class="sxs-lookup"><span data-stu-id="178b8-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="178b8-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="178b8-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="178b8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="178b8-107">DESCRIPTION</span></span>
<span data-ttu-id="178b8-108">O **cmdlet New-AzureSiteRecoveryProtectionProfileObject** cria um objeto de perfil de proteção de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="178b8-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="178b8-109">Esse cmdlet cria um **objeto ASRProtectionProfile** para usar com outros cmdlets.</span><span class="sxs-lookup"><span data-stu-id="178b8-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="178b8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="178b8-110">EXAMPLES</span></span>

### <span data-ttu-id="178b8-111">Exemplo 1: Criar um perfil de proteção</span><span class="sxs-lookup"><span data-stu-id="178b8-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="178b8-112">Esse comando cria um objeto de perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="178b8-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="178b8-113">Exemplo 2: Criar um perfil de proteção para o provedor HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="178b8-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="178b8-114">Esse comando cria um perfil de proteção para um provedor HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="178b8-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="178b8-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="178b8-115">PARAMETERS</span></span>

### <span data-ttu-id="178b8-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="178b8-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="178b8-117">Indica que o perfil de proteção permite a exclusão de entidades replicadas.</span><span class="sxs-lookup"><span data-stu-id="178b8-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="178b8-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="178b8-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="178b8-119">Especifica a frequência, em horas, para instantâneos consistentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="178b8-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="178b8-120">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="178b8-120">-Authentication</span></span>
<span data-ttu-id="178b8-121">Especifica o tipo de autenticação a ser usada.</span><span class="sxs-lookup"><span data-stu-id="178b8-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="178b8-122">Os valores aceitáveis para este parâmetro são: Certificado e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="178b8-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="178b8-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="178b8-123">-CompressionEnabled</span></span>
<span data-ttu-id="178b8-124">Indica que o perfil de proteção habilita a compactação.</span><span class="sxs-lookup"><span data-stu-id="178b8-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="178b8-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="178b8-125">-Force</span></span>
<span data-ttu-id="178b8-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="178b8-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="178b8-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="178b8-127">-Name</span></span>
<span data-ttu-id="178b8-128">Especifica um nome para o perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="178b8-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="178b8-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="178b8-129">-Profile</span></span>
<span data-ttu-id="178b8-130">Especifica o perfil do Azure do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="178b8-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="178b8-131">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="178b8-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="178b8-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178b8-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="178b8-133">Especifica o nome de uma conta de Armazenamento do Azure na qual armazenar a entidade de replica do Azure.</span><span class="sxs-lookup"><span data-stu-id="178b8-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="178b8-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="178b8-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="178b8-135">Especifica a ID de uma Assinatura do Azure para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="178b8-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="178b8-136">Este parâmetro se refere à conta na qual a entidade de replicação do Azure será armazenada.</span><span class="sxs-lookup"><span data-stu-id="178b8-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="178b8-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="178b8-137">-RecoveryPoints</span></span>
<span data-ttu-id="178b8-138">Especifica o número de horas para reter pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="178b8-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="178b8-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="178b8-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="178b8-140">Especifica o intervalo de frequência, em segundos, para replicação.</span><span class="sxs-lookup"><span data-stu-id="178b8-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="178b8-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="178b8-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="178b8-142">30</span><span class="sxs-lookup"><span data-stu-id="178b8-142">30</span></span> 
- <span data-ttu-id="178b8-143">300</span><span class="sxs-lookup"><span data-stu-id="178b8-143">300</span></span> 
- <span data-ttu-id="178b8-144">900</span><span class="sxs-lookup"><span data-stu-id="178b8-144">900</span></span>

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

### <span data-ttu-id="178b8-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="178b8-145">-ReplicationMethod</span></span>
<span data-ttu-id="178b8-146">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="178b8-146">Specifies the replication method.</span></span> <span data-ttu-id="178b8-147">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="178b8-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="178b8-148">Online.</span><span class="sxs-lookup"><span data-stu-id="178b8-148">Online.</span></span>
<span data-ttu-id="178b8-149">Replicação pela rede.</span><span class="sxs-lookup"><span data-stu-id="178b8-149">Replication over the network.</span></span>
- <span data-ttu-id="178b8-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="178b8-150">Offline.</span></span>

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

### <span data-ttu-id="178b8-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="178b8-151">-ReplicationPort</span></span>
<span data-ttu-id="178b8-152">Especifica o número da porta na qual ocorre a replicação.</span><span class="sxs-lookup"><span data-stu-id="178b8-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="178b8-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="178b8-153">-ReplicationProvider</span></span>
<span data-ttu-id="178b8-154">Especifica o tipo de provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="178b8-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="178b8-155">Os valores aceitáveis para este parâmetro são: HyperVReplica e HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="178b8-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="178b8-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="178b8-156">-ReplicationStartTime</span></span>
<span data-ttu-id="178b8-157">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="178b8-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="178b8-158">Especifique um horário dentro de 24 horas após iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="178b8-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="178b8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178b8-159">CommonParameters</span></span>
<span data-ttu-id="178b8-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178b8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178b8-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178b8-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178b8-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="178b8-162">INPUTS</span></span>

## <span data-ttu-id="178b8-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="178b8-163">OUTPUTS</span></span>

## <span data-ttu-id="178b8-164">Notas</span><span class="sxs-lookup"><span data-stu-id="178b8-164">NOTES</span></span>

## <span data-ttu-id="178b8-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="178b8-165">RELATED LINKS</span></span>




