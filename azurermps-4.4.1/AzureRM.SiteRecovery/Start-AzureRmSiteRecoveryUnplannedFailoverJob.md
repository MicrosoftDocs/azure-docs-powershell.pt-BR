---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427772"
---
# <span data-ttu-id="cdf37-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="cdf37-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="cdf37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdf37-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf37-103">Inicia o failover não planejado para uma entidade ou um plano de proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="cdf37-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdf37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdf37-104">SYNTAX</span></span>

### <span data-ttu-id="cdf37-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="cdf37-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdf37-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="cdf37-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdf37-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="cdf37-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdf37-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdf37-108">DESCRIPTION</span></span>
<span data-ttu-id="cdf37-109">O cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** inicia o failover não planejado de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cdf37-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="cdf37-110">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="cdf37-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="cdf37-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdf37-111">EXAMPLES</span></span>

## <span data-ttu-id="cdf37-112">OS</span><span class="sxs-lookup"><span data-stu-id="cdf37-112">PARAMETERS</span></span>

### <span data-ttu-id="cdf37-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="cdf37-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="cdf37-114">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="cdf37-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="cdf37-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="cdf37-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="cdf37-116">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="cdf37-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="cdf37-117">-Direction</span><span class="sxs-lookup"><span data-stu-id="cdf37-117">-Direction</span></span>
<span data-ttu-id="cdf37-118">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="cdf37-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="cdf37-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cdf37-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cdf37-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="cdf37-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="cdf37-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="cdf37-121">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="cdf37-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="cdf37-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="cdf37-123">Indica que a ação pode realizar operações de site de origem.</span><span class="sxs-lookup"><span data-stu-id="cdf37-123">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf37-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="cdf37-124">-ProtectionEntity</span></span>
<span data-ttu-id="cdf37-125">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="cdf37-125">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="cdf37-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cdf37-126">-RecoveryPlan</span></span>
<span data-ttu-id="cdf37-127">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cdf37-127">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="cdf37-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cdf37-128">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="cdf37-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf37-129">-DefaultProfile</span></span>
<span data-ttu-id="cdf37-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf37-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdf37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf37-131">CommonParameters</span></span>
<span data-ttu-id="cdf37-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf37-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf37-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf37-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdf37-134">INPUTS</span></span>

### <span data-ttu-id="cdf37-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="cdf37-135">ASRProtectionEntity</span></span>
<span data-ttu-id="cdf37-136">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cdf37-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="cdf37-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cdf37-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="cdf37-138">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cdf37-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="cdf37-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cdf37-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="cdf37-140">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cdf37-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="cdf37-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdf37-141">OUTPUTS</span></span>

### <span data-ttu-id="cdf37-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cdf37-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cdf37-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdf37-143">NOTES</span></span>

## <span data-ttu-id="cdf37-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdf37-144">RELATED LINKS</span></span>

[<span data-ttu-id="cdf37-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="cdf37-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


