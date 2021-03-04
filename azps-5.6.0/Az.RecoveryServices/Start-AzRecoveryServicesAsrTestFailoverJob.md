---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: b5a06683e5254077a63d4c0b1933d51d9c1ad8e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889888"
---
# <span data-ttu-id="fdc41-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="fdc41-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="fdc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdc41-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc41-103">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="fdc41-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="fdc41-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fdc41-104">SYNTAX</span></span>

### <span data-ttu-id="fdc41-105">ByRPIObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fdc41-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc41-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fdc41-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc41-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="fdc41-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc41-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fdc41-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc41-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="fdc41-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc41-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fdc41-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdc41-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fdc41-111">DESCRIPTION</span></span>
<span data-ttu-id="fdc41-112">O cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** inicia o failover de teste de um item ou plano de recuperação protegido de replicação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc41-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="fdc41-113">Você pode verificar se o trabalho foi bem-sucedido usando Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc41-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="fdc41-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdc41-114">EXAMPLES</span></span>

### <span data-ttu-id="fdc41-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdc41-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="fdc41-116">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="fdc41-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fdc41-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fdc41-117">Example 2</span></span>

<span data-ttu-id="fdc41-118">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="fdc41-118">Starts a test failover operation.</span></span> <span data-ttu-id="fdc41-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="fdc41-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="fdc41-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fdc41-120">PARAMETERS</span></span>

### <span data-ttu-id="fdc41-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fdc41-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="fdc41-122">Especifica a ID de rede vm do Azure para vM de recuperação após o failover.</span><span class="sxs-lookup"><span data-stu-id="fdc41-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="fdc41-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="fdc41-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="fdc41-124">Especifica se um novo serviço de nuvem deve ser criado ou se o serviço de nuvem de recuperação configurado para a VM deve ser usado para o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="fdc41-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="fdc41-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fdc41-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="fdc41-126">Especifica o arquivo de certificado principal.</span><span class="sxs-lookup"><span data-stu-id="fdc41-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="fdc41-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fdc41-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="fdc41-128">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="fdc41-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="fdc41-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc41-129">-DefaultProfile</span></span>
<span data-ttu-id="fdc41-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc41-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fdc41-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="fdc41-131">-Direction</span></span>
<span data-ttu-id="fdc41-132">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="fdc41-132">Specifies the failover direction.</span></span>
<span data-ttu-id="fdc41-133">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fdc41-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdc41-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="fdc41-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="fdc41-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="fdc41-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="fdc41-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fdc41-136">-RecoveryPlan</span></span>
<span data-ttu-id="fdc41-137">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="fdc41-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="fdc41-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fdc41-138">-RecoveryPoint</span></span>
<span data-ttu-id="fdc41-139">Especifica um ponto de recuperação personalizado para testar o failover do computador protegido.</span><span class="sxs-lookup"><span data-stu-id="fdc41-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="fdc41-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="fdc41-140">-RecoveryTag</span></span>
<span data-ttu-id="fdc41-141">Especifica a marca de recuperação para testar o failover para</span><span class="sxs-lookup"><span data-stu-id="fdc41-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="fdc41-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdc41-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fdc41-143">Especifica um item protegido por replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="fdc41-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="fdc41-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="fdc41-144">-VMNetwork</span></span>
<span data-ttu-id="fdc41-145">Especifica a rede de máquina virtual de Recuperação de Site para conectar as máquinas virtuais de failover de teste à.</span><span class="sxs-lookup"><span data-stu-id="fdc41-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="fdc41-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdc41-146">-Confirm</span></span>
<span data-ttu-id="fdc41-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc41-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc41-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc41-148">-WhatIf</span></span>
<span data-ttu-id="fdc41-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fdc41-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdc41-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdc41-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc41-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc41-151">CommonParameters</span></span>
<span data-ttu-id="fdc41-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc41-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc41-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdc41-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc41-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdc41-154">INPUTS</span></span>

### <span data-ttu-id="fdc41-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fdc41-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="fdc41-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fdc41-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fdc41-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fdc41-157">OUTPUTS</span></span>

### <span data-ttu-id="fdc41-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="fdc41-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fdc41-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="fdc41-159">NOTES</span></span>

## <span data-ttu-id="fdc41-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdc41-160">RELATED LINKS</span></span>

[<span data-ttu-id="fdc41-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="fdc41-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
