---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609897"
---
# <span data-ttu-id="576f3-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="576f3-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="576f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="576f3-102">SYNOPSIS</span></span>
<span data-ttu-id="576f3-103">Inicia uma operação de failover planejado de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="576f3-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="576f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="576f3-104">SYNTAX</span></span>

### <span data-ttu-id="576f3-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="576f3-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="576f3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="576f3-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="576f3-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="576f3-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="576f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="576f3-108">DESCRIPTION</span></span>
<span data-ttu-id="576f3-109">O cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** inicia um failover planejado para uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="576f3-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="576f3-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="576f3-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="576f3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="576f3-111">EXAMPLES</span></span>

## <span data-ttu-id="576f3-112">OS</span><span class="sxs-lookup"><span data-stu-id="576f3-112">PARAMETERS</span></span>

### <span data-ttu-id="576f3-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="576f3-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="576f3-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="576f3-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="576f3-115">Sim</span><span class="sxs-lookup"><span data-stu-id="576f3-115">Yes</span></span>
- <span data-ttu-id="576f3-116">Não</span><span class="sxs-lookup"><span data-stu-id="576f3-116">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="576f3-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="576f3-118">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="576f3-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="576f3-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="576f3-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="576f3-120">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="576f3-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="576f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576f3-121">-DefaultProfile</span></span>
<span data-ttu-id="576f3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="576f3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576f3-123">-Direction</span><span class="sxs-lookup"><span data-stu-id="576f3-123">-Direction</span></span>
<span data-ttu-id="576f3-124">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="576f3-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="576f3-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="576f3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="576f3-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="576f3-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="576f3-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="576f3-127">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-128">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="576f3-128">-Optimize</span></span>
<span data-ttu-id="576f3-129">Especifica o que otimizar para.</span><span class="sxs-lookup"><span data-stu-id="576f3-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="576f3-130">Esse parâmetro se aplica quando o failover é feito de um site do Azure para um site local que requer uma sincronização de dados considerável.</span><span class="sxs-lookup"><span data-stu-id="576f3-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="576f3-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="576f3-131">Valid values are:</span></span>

- <span data-ttu-id="576f3-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="576f3-132">ForDowntime</span></span>
- <span data-ttu-id="576f3-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="576f3-133">ForSynchronization</span></span>

<span data-ttu-id="576f3-134">Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="576f3-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="576f3-135">A sincronização é realizada sem desligar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="576f3-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="576f3-136">Após a conclusão da sincronização, o trabalho será suspenso.</span><span class="sxs-lookup"><span data-stu-id="576f3-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="576f3-137">Retome o trabalho para executar uma operação de sincronização adicional que desative a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="576f3-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="576f3-138">Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover, para que a sincronização de dados seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="576f3-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="576f3-139">Com essa configuração habilitada, a máquina virtual é encerrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="576f3-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="576f3-140">A sincronização começará após o desligamento para concluir a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="576f3-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="576f3-141">-ProtectionEntity</span></span>
<span data-ttu-id="576f3-142">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="576f3-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="576f3-143">-RecoveryPlan</span></span>
<span data-ttu-id="576f3-144">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="576f3-144">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="576f3-145">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-146">-Servidor</span><span class="sxs-lookup"><span data-stu-id="576f3-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-147">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="576f3-147">-ServicesProvider</span></span>
```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576f3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576f3-148">CommonParameters</span></span>
<span data-ttu-id="576f3-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576f3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576f3-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576f3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576f3-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="576f3-151">INPUTS</span></span>

### <span data-ttu-id="576f3-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="576f3-152">ASRProtectionEntity</span></span>
<span data-ttu-id="576f3-153">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="576f3-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="576f3-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="576f3-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="576f3-155">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="576f3-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="576f3-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="576f3-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="576f3-157">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="576f3-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="576f3-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="576f3-158">OUTPUTS</span></span>

### <span data-ttu-id="576f3-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="576f3-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="576f3-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="576f3-160">NOTES</span></span>

## <span data-ttu-id="576f3-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="576f3-161">RELATED LINKS</span></span>

