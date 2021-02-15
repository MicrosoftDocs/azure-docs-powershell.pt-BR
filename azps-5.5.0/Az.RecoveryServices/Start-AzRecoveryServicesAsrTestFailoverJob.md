---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114923"
---
# <span data-ttu-id="e95c0-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e95c0-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="e95c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e95c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e95c0-103">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e95c0-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="e95c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e95c0-104">SYNTAX</span></span>

### <span data-ttu-id="e95c0-105">ByRPIObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e95c0-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95c0-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e95c0-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95c0-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e95c0-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95c0-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e95c0-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95c0-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e95c0-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95c0-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e95c0-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e95c0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e95c0-111">DESCRIPTION</span></span>
<span data-ttu-id="e95c0-112">O cmdlet **Start-AzRecoveryServicesAsrTestFailoverService** inicia o failover de teste de um item protegido ou plano de recuperação de Recuperação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e95c0-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e95c0-113">Você pode verificar se o trabalho foi bem-sucedido usando Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95c0-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e95c0-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e95c0-114">EXAMPLES</span></span>

### <span data-ttu-id="e95c0-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e95c0-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="e95c0-116">Inicia a operação de failover de teste para o plano de recuperação com os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="e95c0-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e95c0-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e95c0-117">Example 2</span></span>

<span data-ttu-id="e95c0-118">Inicia uma operação de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e95c0-118">Starts a test failover operation.</span></span> <span data-ttu-id="e95c0-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e95c0-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="e95c0-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e95c0-120">PARAMETERS</span></span>

### <span data-ttu-id="e95c0-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e95c0-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="e95c0-122">Especifica a ID de rede VM do Azure para recuperação de VM após o failover.</span><span class="sxs-lookup"><span data-stu-id="e95c0-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="e95c0-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="e95c0-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="e95c0-124">Especifica se um novo serviço de nuvem deve ser criado ou se o serviço de nuvem de recuperação configurado para o VM deve ser usado para o failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e95c0-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="e95c0-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e95c0-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e95c0-126">Especifica o arquivo de certificado principal.</span><span class="sxs-lookup"><span data-stu-id="e95c0-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="e95c0-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e95c0-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e95c0-128">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="e95c0-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="e95c0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95c0-129">-DefaultProfile</span></span>
<span data-ttu-id="e95c0-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e95c0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e95c0-131">-Direção</span><span class="sxs-lookup"><span data-stu-id="e95c0-131">-Direction</span></span>
<span data-ttu-id="e95c0-132">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="e95c0-132">Specifies the failover direction.</span></span>
<span data-ttu-id="e95c0-133">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e95c0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e95c0-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e95c0-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="e95c0-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e95c0-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="e95c0-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e95c0-136">-RecoveryPlan</span></span>
<span data-ttu-id="e95c0-137">Especifica um objeto de plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="e95c0-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="e95c0-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e95c0-138">-RecoveryPoint</span></span>
<span data-ttu-id="e95c0-139">Especifica um ponto de recuperação personalizado para testar o failover do computador protegido.</span><span class="sxs-lookup"><span data-stu-id="e95c0-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="e95c0-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="e95c0-140">-RecoveryTag</span></span>
<span data-ttu-id="e95c0-141">Especifica a marca de recuperação para testar o failover para</span><span class="sxs-lookup"><span data-stu-id="e95c0-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="e95c0-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e95c0-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e95c0-143">Especifica um item protegido por replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="e95c0-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="e95c0-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="e95c0-144">-VMNetwork</span></span>
<span data-ttu-id="e95c0-145">Especifica a rede de máquina virtual de Recuperação de Site para conectar as máquinas virtuais de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e95c0-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="e95c0-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e95c0-146">-Confirm</span></span>
<span data-ttu-id="e95c0-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95c0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95c0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95c0-148">-WhatIf</span></span>
<span data-ttu-id="e95c0-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e95c0-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e95c0-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e95c0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95c0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95c0-151">CommonParameters</span></span>
<span data-ttu-id="e95c0-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95c0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95c0-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e95c0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95c0-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="e95c0-154">INPUTS</span></span>

### <span data-ttu-id="e95c0-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e95c0-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="e95c0-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e95c0-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e95c0-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="e95c0-157">OUTPUTS</span></span>

### <span data-ttu-id="e95c0-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e95c0-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e95c0-159">Notas</span><span class="sxs-lookup"><span data-stu-id="e95c0-159">NOTES</span></span>

## <span data-ttu-id="e95c0-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e95c0-160">RELATED LINKS</span></span>

[<span data-ttu-id="e95c0-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e95c0-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
