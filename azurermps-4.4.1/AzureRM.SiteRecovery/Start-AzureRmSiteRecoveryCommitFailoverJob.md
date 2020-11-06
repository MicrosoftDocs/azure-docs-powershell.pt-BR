---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429066"
---
# <span data-ttu-id="52812-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="52812-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="52812-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52812-102">SYNOPSIS</span></span>
<span data-ttu-id="52812-103">Inicia a ação de failover de confirmação para um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="52812-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52812-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52812-104">SYNTAX</span></span>

### <span data-ttu-id="52812-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="52812-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52812-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="52812-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52812-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="52812-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52812-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52812-108">DESCRIPTION</span></span>
<span data-ttu-id="52812-109">O cmdlet **Start-AzureRmSiteRecoveryCommitFailoverJob** inicia o processo de failover de confirmação para um objeto do Azure site Recovery após uma operação de failover.</span><span class="sxs-lookup"><span data-stu-id="52812-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="52812-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52812-110">EXAMPLES</span></span>

## <span data-ttu-id="52812-111">OS</span><span class="sxs-lookup"><span data-stu-id="52812-111">PARAMETERS</span></span>

### <span data-ttu-id="52812-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="52812-112">-ProtectionEntity</span></span>
<span data-ttu-id="52812-113">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="52812-113">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="52812-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="52812-114">-RecoveryPlan</span></span>
<span data-ttu-id="52812-115">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="52812-115">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="52812-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52812-116">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="52812-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52812-117">-DefaultProfile</span></span>
<span data-ttu-id="52812-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52812-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52812-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52812-119">CommonParameters</span></span>
<span data-ttu-id="52812-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52812-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52812-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52812-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52812-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52812-122">INPUTS</span></span>

### <span data-ttu-id="52812-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="52812-123">ASRProtectionEntity</span></span>
<span data-ttu-id="52812-124">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52812-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="52812-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="52812-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="52812-126">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52812-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="52812-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="52812-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="52812-128">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="52812-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="52812-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52812-129">OUTPUTS</span></span>

### <span data-ttu-id="52812-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="52812-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="52812-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52812-131">NOTES</span></span>

## <span data-ttu-id="52812-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52812-132">RELATED LINKS</span></span>

