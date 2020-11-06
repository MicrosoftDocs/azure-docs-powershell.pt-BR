---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426588"
---
# <span data-ttu-id="663dd-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="663dd-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="663dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="663dd-102">SYNOPSIS</span></span>
<span data-ttu-id="663dd-103">Inicia o failover não planejado para uma entidade ou um plano de proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="663dd-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="663dd-104">SYNTAX</span></span>

### <span data-ttu-id="663dd-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="663dd-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663dd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="663dd-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663dd-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="663dd-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="663dd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="663dd-108">DESCRIPTION</span></span>
<span data-ttu-id="663dd-109">O cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** inicia o failover não planejado de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="663dd-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="663dd-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="663dd-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="663dd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="663dd-111">EXAMPLES</span></span>

## <span data-ttu-id="663dd-112">OS</span><span class="sxs-lookup"><span data-stu-id="663dd-112">PARAMETERS</span></span>

### <span data-ttu-id="663dd-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="663dd-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="663dd-114">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="663dd-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="663dd-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="663dd-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="663dd-116">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="663dd-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="663dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663dd-117">-DefaultProfile</span></span>
<span data-ttu-id="663dd-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="663dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="663dd-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="663dd-119">-Direction</span></span>
<span data-ttu-id="663dd-120">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="663dd-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="663dd-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="663dd-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="663dd-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="663dd-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="663dd-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="663dd-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="663dd-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="663dd-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="663dd-125">Indica que a ação pode realizar operações de site de origem.</span><span class="sxs-lookup"><span data-stu-id="663dd-125">Indicates that the action can perform source site operations.</span></span>

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

### <span data-ttu-id="663dd-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="663dd-126">-ProtectionEntity</span></span>
<span data-ttu-id="663dd-127">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="663dd-127">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="663dd-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="663dd-128">-RecoveryPlan</span></span>
<span data-ttu-id="663dd-129">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="663dd-129">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="663dd-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="663dd-130">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="663dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663dd-131">CommonParameters</span></span>
<span data-ttu-id="663dd-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663dd-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663dd-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="663dd-134">INPUTS</span></span>

### <span data-ttu-id="663dd-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="663dd-135">ASRProtectionEntity</span></span>
<span data-ttu-id="663dd-136">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="663dd-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="663dd-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="663dd-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="663dd-138">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="663dd-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="663dd-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="663dd-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="663dd-140">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="663dd-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="663dd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="663dd-141">OUTPUTS</span></span>

### <span data-ttu-id="663dd-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="663dd-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="663dd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="663dd-143">NOTES</span></span>

## <span data-ttu-id="663dd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="663dd-144">RELATED LINKS</span></span>

[<span data-ttu-id="663dd-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="663dd-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

