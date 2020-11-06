---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610447"
---
# <span data-ttu-id="c690a-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="c690a-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="c690a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c690a-102">SYNOPSIS</span></span>
<span data-ttu-id="c690a-103">Cria uma política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="c690a-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c690a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c690a-104">SYNTAX</span></span>

### <span data-ttu-id="c690a-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="c690a-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c690a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c690a-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c690a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c690a-107">DESCRIPTION</span></span>
<span data-ttu-id="c690a-108">O cmdlet **New-AzureRmSiteRecoveryPolicy** cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c690a-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="c690a-109">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c690a-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="c690a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c690a-110">EXAMPLES</span></span>

## <span data-ttu-id="c690a-111">OS</span><span class="sxs-lookup"><span data-stu-id="c690a-111">PARAMETERS</span></span>

### <span data-ttu-id="c690a-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="c690a-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="c690a-113">Especifica a frequência do instantâneo consistente do aplicativo em horas.</span><span class="sxs-lookup"><span data-stu-id="c690a-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="c690a-114">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="c690a-114">-Authentication</span></span>
<span data-ttu-id="c690a-115">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="c690a-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="c690a-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c690a-116">Valid values are:</span></span>

- <span data-ttu-id="c690a-117">Certificado</span><span class="sxs-lookup"><span data-stu-id="c690a-117">Certificate</span></span>
-  <span data-ttu-id="c690a-118">V5</span><span class="sxs-lookup"><span data-stu-id="c690a-118">Kerberos</span></span>

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

### <span data-ttu-id="c690a-119">-Compactação</span><span class="sxs-lookup"><span data-stu-id="c690a-119">-Compression</span></span>
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

### <span data-ttu-id="c690a-120">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="c690a-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c690a-121">-Name</span></span>
<span data-ttu-id="c690a-122">Especifica um nome amigável que identifica a política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="c690a-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="c690a-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c690a-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c690a-124">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="c690a-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690a-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="c690a-125">-RecoveryPoints</span></span>
<span data-ttu-id="c690a-126">Especifica o número de horas para manter os pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c690a-126">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="c690a-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="c690a-127">-ReplicaDeletion</span></span>
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

### <span data-ttu-id="c690a-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="c690a-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="c690a-129">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="c690a-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="c690a-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c690a-130">Valid values are:</span></span>

- <span data-ttu-id="c690a-131">30</span><span class="sxs-lookup"><span data-stu-id="c690a-131">30</span></span>
- <span data-ttu-id="c690a-132">300</span><span class="sxs-lookup"><span data-stu-id="c690a-132">300</span></span>
- <span data-ttu-id="c690a-133">900</span><span class="sxs-lookup"><span data-stu-id="c690a-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690a-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="c690a-134">-ReplicationMethod</span></span>
<span data-ttu-id="c690a-135">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="c690a-135">Specifies the replication method.</span></span>
<span data-ttu-id="c690a-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c690a-136">Valid values are:</span></span>

- <span data-ttu-id="c690a-137">Internet</span><span class="sxs-lookup"><span data-stu-id="c690a-137">Online</span></span>
- <span data-ttu-id="c690a-138">Modo</span><span class="sxs-lookup"><span data-stu-id="c690a-138">Offline</span></span>

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

### <span data-ttu-id="c690a-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="c690a-139">-ReplicationPort</span></span>
<span data-ttu-id="c690a-140">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="c690a-140">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="c690a-141">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="c690a-141">-ReplicationProvider</span></span>
<span data-ttu-id="c690a-142">Especifica o provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="c690a-142">Specifies the replication provider.</span></span>
<span data-ttu-id="c690a-143">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c690a-143">Valid values are:</span></span>

- <span data-ttu-id="c690a-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="c690a-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="c690a-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="c690a-145">HyperVReplica2012</span></span>
- <span data-ttu-id="c690a-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="c690a-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690a-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="c690a-147">-ReplicationStartTime</span></span>
<span data-ttu-id="c690a-148">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="c690a-148">Specifies the replication start time.</span></span>
<span data-ttu-id="c690a-149">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c690a-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c690a-150">-DefaultProfile</span></span>
<span data-ttu-id="c690a-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c690a-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c690a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690a-152">CommonParameters</span></span>
<span data-ttu-id="c690a-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c690a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690a-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c690a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690a-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c690a-155">INPUTS</span></span>

## <span data-ttu-id="c690a-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c690a-156">OUTPUTS</span></span>

## <span data-ttu-id="c690a-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c690a-157">NOTES</span></span>

## <span data-ttu-id="c690a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c690a-158">RELATED LINKS</span></span>

[<span data-ttu-id="c690a-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="c690a-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="c690a-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="c690a-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
