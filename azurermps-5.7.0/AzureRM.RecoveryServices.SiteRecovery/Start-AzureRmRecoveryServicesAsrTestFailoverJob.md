---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: bab9cb87f347b198b430c1dadc65a002dfa94141
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426643"
---
# <span data-ttu-id="a853b-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a853b-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="a853b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a853b-102">SYNOPSIS</span></span>
<span data-ttu-id="a853b-103">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="a853b-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a853b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a853b-104">SYNTAX</span></span>

### <span data-ttu-id="a853b-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="a853b-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a853b-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853b-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="a853b-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853b-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a853b-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853b-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="a853b-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853b-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a853b-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a853b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a853b-111">DESCRIPTION</span></span>
<span data-ttu-id="a853b-112">O cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** inicia o failover de teste de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a853b-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="a853b-113">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="a853b-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="a853b-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a853b-114">EXAMPLES</span></span>

### <span data-ttu-id="a853b-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a853b-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="a853b-116">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="a853b-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a853b-117">OS</span><span class="sxs-lookup"><span data-stu-id="a853b-117">PARAMETERS</span></span>

### <span data-ttu-id="a853b-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a853b-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="a853b-119">Especifica a ID de rede virtual do Azure para conectar o teste failover em relação a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a853b-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="a853b-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="a853b-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="a853b-121">Especifica se um novo serviço de nuvem deve ser criado ou se o serviço de nuvem de recuperação configurado para a VM deve ser usado para o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="a853b-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a853b-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a853b-122">-Confirm</span></span>
<span data-ttu-id="a853b-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a853b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a853b-124">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a853b-124">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a853b-125">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="a853b-125">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="a853b-126">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a853b-126">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a853b-127">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="a853b-127">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="a853b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a853b-128">-DefaultProfile</span></span>
<span data-ttu-id="a853b-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a853b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="a853b-130">-Direction</span><span class="sxs-lookup"><span data-stu-id="a853b-130">-Direction</span></span>
<span data-ttu-id="a853b-131">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="a853b-131">Specifies the failover direction.</span></span>
<span data-ttu-id="a853b-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a853b-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a853b-133">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a853b-133">PrimaryToRecovery</span></span>
- <span data-ttu-id="a853b-134">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a853b-134">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a853b-135">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a853b-135">-RecoveryPlan</span></span>
<span data-ttu-id="a853b-136">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="a853b-136">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="a853b-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a853b-137">-RecoveryPoint</span></span>
<span data-ttu-id="a853b-138">Especifica um ponto de recuperação personalizado para testar o failover da máquina protegida.</span><span class="sxs-lookup"><span data-stu-id="a853b-138">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a853b-139">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="a853b-139">-RecoveryTag</span></span>
<span data-ttu-id="a853b-140">Especifica a marca de recuperação para o qual testar o failover</span><span class="sxs-lookup"><span data-stu-id="a853b-140">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a853b-141">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a853b-141">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a853b-142">Especifica um item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="a853b-142">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="a853b-143">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="a853b-143">-VMNetwork</span></span>
<span data-ttu-id="a853b-144">Especifica a rede de máquina virtual de recuperação de site para conectar as máquinas virtuais de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="a853b-144">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="a853b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a853b-145">-WhatIf</span></span>
<span data-ttu-id="a853b-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a853b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a853b-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a853b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a853b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a853b-148">CommonParameters</span></span>
<span data-ttu-id="a853b-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a853b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a853b-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a853b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a853b-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a853b-151">INPUTS</span></span>

### <span data-ttu-id="a853b-152">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a853b-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="a853b-153">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a853b-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a853b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a853b-154">OUTPUTS</span></span>

### <span data-ttu-id="a853b-155">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a853b-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a853b-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a853b-156">NOTES</span></span>

## <span data-ttu-id="a853b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a853b-157">RELATED LINKS</span></span>

[<span data-ttu-id="a853b-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a853b-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
