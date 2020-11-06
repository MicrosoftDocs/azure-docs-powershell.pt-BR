---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609594"
---
# <span data-ttu-id="a7ffa-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a7ffa-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="a7ffa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ffa-103">Inicia uma operação de failover não planejada.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7ffa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7ffa-104">SYNTAX</span></span>

### <span data-ttu-id="a7ffa-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7ffa-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ffa-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a7ffa-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ffa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ffa-108">O cmdlet **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** inicia o failover não planejado de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="a7ffa-109">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="a7ffa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7ffa-110">EXAMPLES</span></span>

### <span data-ttu-id="a7ffa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7ffa-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="a7ffa-112">Inicia a operação de failover não planejado para o plano de recuperação especificado usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a7ffa-113">OS</span><span class="sxs-lookup"><span data-stu-id="a7ffa-113">PARAMETERS</span></span>

### <span data-ttu-id="a7ffa-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a7ffa-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a7ffa-115">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="a7ffa-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a7ffa-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a7ffa-117">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="a7ffa-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="a7ffa-118">-Direction</span></span>
<span data-ttu-id="a7ffa-119">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="a7ffa-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a7ffa-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7ffa-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a7ffa-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="a7ffa-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a7ffa-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a7ffa-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="a7ffa-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="a7ffa-124">Indica que qualquer operação de site de origem especificada no plano de recuperação deve ser feita como parte do failover.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ffa-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7ffa-125">-RecoveryPlan</span></span>
<span data-ttu-id="a7ffa-126">Especifica um objeto de plano de recuperação ASR correspondente ao plano de recuperação no qual a operação de failover deve ser realizada.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="a7ffa-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a7ffa-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a7ffa-128">Especifica o objeto de item protegido da replicação ASR correspondente ao item protegido de replicação no qual a operação de failover deve ser realizada.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="a7ffa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7ffa-129">-Confirm</span></span>
<span data-ttu-id="a7ffa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ffa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ffa-131">-WhatIf</span></span>
<span data-ttu-id="a7ffa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7ffa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ffa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ffa-134">CommonParameters</span></span>
<span data-ttu-id="a7ffa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ffa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ffa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ffa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ffa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7ffa-137">INPUTS</span></span>

### <span data-ttu-id="a7ffa-138">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a7ffa-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="a7ffa-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a7ffa-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a7ffa-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7ffa-140">OUTPUTS</span></span>

### <span data-ttu-id="a7ffa-141">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a7ffa-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a7ffa-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7ffa-142">NOTES</span></span>

## <span data-ttu-id="a7ffa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7ffa-143">RELATED LINKS</span></span>

[<span data-ttu-id="a7ffa-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a7ffa-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


