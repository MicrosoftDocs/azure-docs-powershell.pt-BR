---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433036"
---
# <span data-ttu-id="09610-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="09610-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="09610-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09610-102">SYNOPSIS</span></span>
<span data-ttu-id="09610-103">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="09610-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09610-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09610-104">SYNTAX</span></span>

### <span data-ttu-id="09610-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="09610-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09610-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="09610-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09610-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="09610-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09610-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="09610-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09610-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="09610-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09610-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="09610-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09610-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09610-111">DESCRIPTION</span></span>
<span data-ttu-id="09610-112">O cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** inicia o failover de teste de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="09610-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="09610-113">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="09610-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="09610-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09610-114">EXAMPLES</span></span>

### <span data-ttu-id="09610-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09610-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="09610-116">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="09610-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="09610-117">OS</span><span class="sxs-lookup"><span data-stu-id="09610-117">PARAMETERS</span></span>

### <span data-ttu-id="09610-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="09610-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="09610-119">Especifica a ID de rede virtual do Azure para conectar o teste failover em relação a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="09610-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09610-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="09610-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="09610-121">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="09610-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="09610-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="09610-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="09610-123">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="09610-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="09610-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="09610-124">-Direction</span></span>
<span data-ttu-id="09610-125">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="09610-125">Specifies the failover direction.</span></span>
<span data-ttu-id="09610-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="09610-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09610-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="09610-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="09610-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="09610-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="09610-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="09610-129">-RecoveryPlan</span></span>
<span data-ttu-id="09610-130">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="09610-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09610-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="09610-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="09610-132">Especifica um item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="09610-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09610-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="09610-133">-VMNetwork</span></span>
<span data-ttu-id="09610-134">Especifica a rede de máquina virtual de recuperação de site para conectar as máquinas virtuais de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="09610-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09610-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09610-135">-Confirm</span></span>
<span data-ttu-id="09610-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09610-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09610-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09610-137">-WhatIf</span></span>
<span data-ttu-id="09610-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09610-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09610-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09610-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09610-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09610-140">CommonParameters</span></span>
<span data-ttu-id="09610-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09610-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09610-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09610-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09610-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09610-143">INPUTS</span></span>

### <span data-ttu-id="09610-144">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="09610-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="09610-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="09610-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="09610-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09610-146">OUTPUTS</span></span>

### <span data-ttu-id="09610-147">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="09610-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="09610-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09610-148">NOTES</span></span>

## <span data-ttu-id="09610-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09610-149">RELATED LINKS</span></span>

[<span data-ttu-id="09610-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="09610-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
