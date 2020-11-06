---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: a05467b19aaf69bccdca64c8e17b894941f3ac6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599590"
---
# <span data-ttu-id="8d735-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8d735-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="8d735-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d735-102">SYNOPSIS</span></span>
<span data-ttu-id="8d735-103">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="8d735-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="8d735-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d735-104">SYNTAX</span></span>

### <span data-ttu-id="8d735-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d735-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d735-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8d735-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d735-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d735-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d735-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d735-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d735-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d735-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d735-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d735-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d735-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d735-111">DESCRIPTION</span></span>
<span data-ttu-id="8d735-112">O cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** inicia o failover de teste de um item protegido de replicação do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8d735-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8d735-113">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="8d735-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8d735-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d735-114">EXAMPLES</span></span>

### <span data-ttu-id="8d735-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d735-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="8d735-116">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="8d735-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8d735-117">OS</span><span class="sxs-lookup"><span data-stu-id="8d735-117">PARAMETERS</span></span>

### <span data-ttu-id="8d735-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d735-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="8d735-119">{{Fill AzureVMNetworkId descrição}}</span><span class="sxs-lookup"><span data-stu-id="8d735-119">{{Fill AzureVMNetworkId Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="8d735-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="8d735-121">Especifica se um novo serviço de nuvem deve ser criado ou se o serviço de nuvem de recuperação configurado para a VM deve ser usado para o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="8d735-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d735-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8d735-123">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="8d735-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="8d735-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d735-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8d735-125">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="8d735-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="8d735-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d735-126">-DefaultProfile</span></span>
<span data-ttu-id="8d735-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d735-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-128">-Direction</span><span class="sxs-lookup"><span data-stu-id="8d735-128">-Direction</span></span>
<span data-ttu-id="8d735-129">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="8d735-129">Specifies the failover direction.</span></span>
<span data-ttu-id="8d735-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8d735-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d735-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8d735-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="8d735-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8d735-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8d735-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d735-133">-RecoveryPlan</span></span>
<span data-ttu-id="8d735-134">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="8d735-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8d735-135">-RecoveryPoint</span></span>
<span data-ttu-id="8d735-136">Especifica um ponto de recuperação personalizado para testar o failover da máquina protegida.</span><span class="sxs-lookup"><span data-stu-id="8d735-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="8d735-137">-RecoveryTag</span></span>
<span data-ttu-id="8d735-138">Especifica a marca de recuperação para o qual testar o failover</span><span class="sxs-lookup"><span data-stu-id="8d735-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d735-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8d735-140">Especifica um item protegido de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="8d735-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d735-141">-VMNetwork</span></span>
<span data-ttu-id="8d735-142">Especifica a rede de máquina virtual de recuperação de site para conectar as máquinas virtuais de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="8d735-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d735-143">-Confirm</span></span>
<span data-ttu-id="8d735-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d735-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d735-145">-WhatIf</span></span>
<span data-ttu-id="8d735-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d735-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d735-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d735-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d735-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d735-148">CommonParameters</span></span>
<span data-ttu-id="8d735-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d735-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d735-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d735-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d735-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d735-151">INPUTS</span></span>

### <span data-ttu-id="8d735-152">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d735-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="8d735-153">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d735-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8d735-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d735-154">OUTPUTS</span></span>

### <span data-ttu-id="8d735-155">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8d735-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8d735-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d735-156">NOTES</span></span>

## <span data-ttu-id="8d735-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d735-157">RELATED LINKS</span></span>

[<span data-ttu-id="8d735-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8d735-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
