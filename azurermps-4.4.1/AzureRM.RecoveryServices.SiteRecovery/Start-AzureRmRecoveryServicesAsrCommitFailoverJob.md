---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432589"
---
# <span data-ttu-id="270a3-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="270a3-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="270a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="270a3-102">SYNOPSIS</span></span>
<span data-ttu-id="270a3-103">Inicia a ação de failover de confirmação para um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="270a3-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="270a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="270a3-104">SYNTAX</span></span>

### <span data-ttu-id="270a3-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="270a3-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="270a3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="270a3-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="270a3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="270a3-107">DESCRIPTION</span></span>
<span data-ttu-id="270a3-108">O cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** inicia o processo de failover de confirmação para um objeto do Azure site Recovery após uma operação de failover.</span><span class="sxs-lookup"><span data-stu-id="270a3-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="270a3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="270a3-109">EXAMPLES</span></span>

### <span data-ttu-id="270a3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="270a3-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="270a3-111">Inicia o failover de confirmação para o plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="270a3-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="270a3-112">OS</span><span class="sxs-lookup"><span data-stu-id="270a3-112">PARAMETERS</span></span>

### <span data-ttu-id="270a3-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="270a3-113">-RecoveryPlan</span></span>
<span data-ttu-id="270a3-114">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="270a3-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="270a3-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="270a3-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="270a3-116">Especifica um objeto de item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="270a3-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="270a3-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="270a3-117">-Confirm</span></span>
<span data-ttu-id="270a3-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270a3-119">-WhatIf</span></span>
<span data-ttu-id="270a3-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="270a3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="270a3-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="270a3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270a3-122">CommonParameters</span></span>
<span data-ttu-id="270a3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270a3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270a3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="270a3-125">INPUTS</span></span>

### <span data-ttu-id="270a3-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="270a3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="270a3-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="270a3-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="270a3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="270a3-128">OUTPUTS</span></span>

### <span data-ttu-id="270a3-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="270a3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="270a3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="270a3-130">NOTES</span></span>

## <span data-ttu-id="270a3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="270a3-131">RELATED LINKS</span></span>

