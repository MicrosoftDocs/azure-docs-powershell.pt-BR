---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609588"
---
# <span data-ttu-id="12671-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="12671-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="12671-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12671-102">SYNOPSIS</span></span>
<span data-ttu-id="12671-103">Atualiza a direção de replicação para o item ou o plano de recuperação especificado duplicado.</span><span class="sxs-lookup"><span data-stu-id="12671-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="12671-104">Usado para proteger novamente/reverter a replicação de um item de failover ou de um plano de recuperação com failover.</span><span class="sxs-lookup"><span data-stu-id="12671-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12671-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12671-105">SYNTAX</span></span>

### <span data-ttu-id="12671-106">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="12671-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12671-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="12671-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12671-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="12671-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12671-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12671-109">DESCRIPTION</span></span>
<span data-ttu-id="12671-110">O cmdlet **Update-AzureRmRecoveryServicesAsrProtectionDirection** atualiza a direção de replicação para o objeto do Azure site Recovery especificado após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="12671-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="12671-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12671-111">EXAMPLES</span></span>

### <span data-ttu-id="12671-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12671-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="12671-113">Iniciar a operação de atualização de direção para o plano recoveyr especificado e retorna o objeto de trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="12671-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="12671-114">OS</span><span class="sxs-lookup"><span data-stu-id="12671-114">PARAMETERS</span></span>

### <span data-ttu-id="12671-115">-Direction</span><span class="sxs-lookup"><span data-stu-id="12671-115">-Direction</span></span>
<span data-ttu-id="12671-116">Especifica a direção a ser usada para a operação de atualização lançar um failover.</span><span class="sxs-lookup"><span data-stu-id="12671-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="12671-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="12671-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12671-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="12671-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="12671-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="12671-119">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="12671-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12671-120">-RecoveryPlan</span></span>
<span data-ttu-id="12671-121">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="12671-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="12671-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12671-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="12671-123">Especifica um item protegido de replicação ASR</span><span class="sxs-lookup"><span data-stu-id="12671-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="12671-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12671-124">-Confirm</span></span>
<span data-ttu-id="12671-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12671-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12671-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12671-126">-WhatIf</span></span>
<span data-ttu-id="12671-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12671-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12671-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12671-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12671-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12671-129">CommonParameters</span></span>
<span data-ttu-id="12671-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12671-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12671-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12671-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12671-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12671-132">INPUTS</span></span>

### <span data-ttu-id="12671-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="12671-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="12671-134">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="12671-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="12671-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12671-135">OUTPUTS</span></span>

### <span data-ttu-id="12671-136">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="12671-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="12671-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12671-137">NOTES</span></span>

## <span data-ttu-id="12671-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12671-138">RELATED LINKS</span></span>

