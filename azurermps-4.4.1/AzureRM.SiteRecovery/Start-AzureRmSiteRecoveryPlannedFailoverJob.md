---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430615"
---
# <span data-ttu-id="39e63-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="39e63-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="39e63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39e63-102">SYNOPSIS</span></span>
<span data-ttu-id="39e63-103">Inicia uma operação de failover planejado de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="39e63-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39e63-104">SYNTAX</span></span>

### <span data-ttu-id="39e63-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="39e63-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39e63-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="39e63-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39e63-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="39e63-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39e63-108">DESCRIPTION</span></span>
<span data-ttu-id="39e63-109">O cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** inicia um failover planejado para uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="39e63-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="39e63-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="39e63-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="39e63-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39e63-111">EXAMPLES</span></span>

## <span data-ttu-id="39e63-112">OS</span><span class="sxs-lookup"><span data-stu-id="39e63-112">PARAMETERS</span></span>

### <span data-ttu-id="39e63-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="39e63-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="39e63-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="39e63-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39e63-115">Sim</span><span class="sxs-lookup"><span data-stu-id="39e63-115">Yes</span></span>
- <span data-ttu-id="39e63-116">Não</span><span class="sxs-lookup"><span data-stu-id="39e63-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="39e63-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="39e63-118">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="39e63-118">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="39e63-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="39e63-120">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="39e63-120">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-121">-Direction</span><span class="sxs-lookup"><span data-stu-id="39e63-121">-Direction</span></span>
<span data-ttu-id="39e63-122">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="39e63-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="39e63-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="39e63-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39e63-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="39e63-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="39e63-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="39e63-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-126">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="39e63-126">-Optimize</span></span>
<span data-ttu-id="39e63-127">Especifica o que otimizar para.</span><span class="sxs-lookup"><span data-stu-id="39e63-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="39e63-128">Esse parâmetro se aplica quando o failover é feito de um site do Azure para um site local que requer uma sincronização de dados considerável.</span><span class="sxs-lookup"><span data-stu-id="39e63-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="39e63-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="39e63-129">Valid values are:</span></span>

- <span data-ttu-id="39e63-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="39e63-130">ForDowntime</span></span>
- <span data-ttu-id="39e63-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="39e63-131">ForSynchronization</span></span>

<span data-ttu-id="39e63-132">Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="39e63-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="39e63-133">A sincronização é realizada sem desligar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="39e63-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="39e63-134">Após a conclusão da sincronização, o trabalho será suspenso.</span><span class="sxs-lookup"><span data-stu-id="39e63-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="39e63-135">Retome o trabalho para executar uma operação de sincronização adicional que desative a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="39e63-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="39e63-136">Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover, para que a sincronização de dados seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="39e63-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="39e63-137">Com essa configuração habilitada, a máquina virtual é encerrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="39e63-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="39e63-138">A sincronização começará após o desligamento para concluir a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="39e63-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="39e63-139">-ProtectionEntity</span></span>
<span data-ttu-id="39e63-140">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="39e63-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39e63-141">-RecoveryPlan</span></span>
<span data-ttu-id="39e63-142">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="39e63-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="39e63-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-144">-Servidor</span><span class="sxs-lookup"><span data-stu-id="39e63-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-145">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="39e63-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e63-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e63-146">-DefaultProfile</span></span>
<span data-ttu-id="39e63-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39e63-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e63-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e63-148">CommonParameters</span></span>
<span data-ttu-id="39e63-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e63-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e63-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e63-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e63-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39e63-151">INPUTS</span></span>

### <span data-ttu-id="39e63-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="39e63-152">ASRProtectionEntity</span></span>
<span data-ttu-id="39e63-153">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="39e63-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="39e63-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39e63-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="39e63-155">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="39e63-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="39e63-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="39e63-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="39e63-157">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="39e63-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="39e63-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39e63-158">OUTPUTS</span></span>

### <span data-ttu-id="39e63-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="39e63-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="39e63-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39e63-160">NOTES</span></span>

## <span data-ttu-id="39e63-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39e63-161">RELATED LINKS</span></span>

