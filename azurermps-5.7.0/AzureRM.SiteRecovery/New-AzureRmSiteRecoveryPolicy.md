---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 65e5e507259198cdacc69ff0764b4f4f18bf9077
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609909"
---
# <span data-ttu-id="542f4-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="542f4-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="542f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="542f4-102">SYNOPSIS</span></span>
<span data-ttu-id="542f4-103">Cria uma política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="542f4-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="542f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="542f4-104">SYNTAX</span></span>

### <span data-ttu-id="542f4-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="542f4-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="542f4-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="542f4-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542f4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="542f4-107">DESCRIPTION</span></span>
<span data-ttu-id="542f4-108">O cmdlet **New-AzureRmSiteRecoveryPolicy** cria uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="542f4-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="542f4-109">A política de replicação é usada para especificar configurações de replicação, como a frequência de replicação e o número de pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="542f4-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="542f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="542f4-110">EXAMPLES</span></span>

## <span data-ttu-id="542f4-111">OS</span><span class="sxs-lookup"><span data-stu-id="542f4-111">PARAMETERS</span></span>

### <span data-ttu-id="542f4-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="542f4-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="542f4-113">Especifica a frequência do instantâneo consistente do aplicativo em horas.</span><span class="sxs-lookup"><span data-stu-id="542f4-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="542f4-114">-Autenticação</span><span class="sxs-lookup"><span data-stu-id="542f4-114">-Authentication</span></span>
<span data-ttu-id="542f4-115">Especifica o tipo de autenticação usado.</span><span class="sxs-lookup"><span data-stu-id="542f4-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="542f4-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="542f4-116">Valid values are:</span></span>

- <span data-ttu-id="542f4-117">Certificado</span><span class="sxs-lookup"><span data-stu-id="542f4-117">Certificate</span></span>
-  <span data-ttu-id="542f4-118">V5</span><span class="sxs-lookup"><span data-stu-id="542f4-118">Kerberos</span></span>

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

### <span data-ttu-id="542f4-119">-Compactação</span><span class="sxs-lookup"><span data-stu-id="542f4-119">-Compression</span></span>
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

### <span data-ttu-id="542f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542f4-120">-DefaultProfile</span></span>
<span data-ttu-id="542f4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="542f4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="542f4-122">-Criptografia</span><span class="sxs-lookup"><span data-stu-id="542f4-122">-Encryption</span></span>
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

### <span data-ttu-id="542f4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="542f4-123">-Name</span></span>
<span data-ttu-id="542f4-124">Especifica um nome amigável que identifica a política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="542f4-124">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="542f4-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="542f4-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="542f4-126">Especifica a ID da conta de armazenamento do Azure do destino de replicação.</span><span class="sxs-lookup"><span data-stu-id="542f4-126">Specifies the Azure storage account ID of the replication target.</span></span>

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

### <span data-ttu-id="542f4-127">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="542f4-127">-RecoveryPoints</span></span>
<span data-ttu-id="542f4-128">Especifica o número de horas para manter os pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="542f4-128">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="542f4-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="542f4-129">-ReplicaDeletion</span></span>
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

### <span data-ttu-id="542f4-130">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="542f4-130">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="542f4-131">Especifica o intervalo de frequência de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="542f4-131">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="542f4-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="542f4-132">Valid values are:</span></span>

- <span data-ttu-id="542f4-133">30</span><span class="sxs-lookup"><span data-stu-id="542f4-133">30</span></span>
- <span data-ttu-id="542f4-134">300</span><span class="sxs-lookup"><span data-stu-id="542f4-134">300</span></span>
- <span data-ttu-id="542f4-135">900</span><span class="sxs-lookup"><span data-stu-id="542f4-135">900</span></span>

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

### <span data-ttu-id="542f4-136">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="542f4-136">-ReplicationMethod</span></span>
<span data-ttu-id="542f4-137">Especifica o método de replicação.</span><span class="sxs-lookup"><span data-stu-id="542f4-137">Specifies the replication method.</span></span>
<span data-ttu-id="542f4-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="542f4-138">Valid values are:</span></span>

- <span data-ttu-id="542f4-139">Internet</span><span class="sxs-lookup"><span data-stu-id="542f4-139">Online</span></span>
- <span data-ttu-id="542f4-140">Modo</span><span class="sxs-lookup"><span data-stu-id="542f4-140">Offline</span></span>

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

### <span data-ttu-id="542f4-141">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="542f4-141">-ReplicationPort</span></span>
<span data-ttu-id="542f4-142">Especifica a porta usada para replicação.</span><span class="sxs-lookup"><span data-stu-id="542f4-142">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="542f4-143">-Replicationprovider</span><span class="sxs-lookup"><span data-stu-id="542f4-143">-ReplicationProvider</span></span>
<span data-ttu-id="542f4-144">Especifica o provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="542f4-144">Specifies the replication provider.</span></span>
<span data-ttu-id="542f4-145">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="542f4-145">Valid values are:</span></span>

- <span data-ttu-id="542f4-146">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="542f4-146">HyperVReplica2012R2</span></span>
- <span data-ttu-id="542f4-147">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="542f4-147">HyperVReplica2012</span></span>
- <span data-ttu-id="542f4-148">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="542f4-148">HyperVReplicaAzure</span></span>

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

### <span data-ttu-id="542f4-149">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="542f4-149">-ReplicationStartTime</span></span>
<span data-ttu-id="542f4-150">Especifica a hora de início da replicação.</span><span class="sxs-lookup"><span data-stu-id="542f4-150">Specifies the replication start time.</span></span>
<span data-ttu-id="542f4-151">Ele não deve ser posterior a 24 horas do início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="542f4-151">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="542f4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542f4-152">CommonParameters</span></span>
<span data-ttu-id="542f4-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542f4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542f4-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542f4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542f4-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="542f4-155">INPUTS</span></span>

### <span data-ttu-id="542f4-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="542f4-156">None</span></span>
<span data-ttu-id="542f4-157">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="542f4-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="542f4-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="542f4-158">OUTPUTS</span></span>

## <span data-ttu-id="542f4-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="542f4-159">NOTES</span></span>

## <span data-ttu-id="542f4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="542f4-160">RELATED LINKS</span></span>

[<span data-ttu-id="542f4-161">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="542f4-161">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="542f4-162">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="542f4-162">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
