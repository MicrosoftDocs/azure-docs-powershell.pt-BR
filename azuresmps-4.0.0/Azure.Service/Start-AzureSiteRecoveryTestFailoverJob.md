---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946028"
---
# <span data-ttu-id="e6c68-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e6c68-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="e6c68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6c68-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c68-103">Inicia um failover de teste para uma entidade de proteção de site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e6c68-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="e6c68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6c68-104">SYNTAX</span></span>

### <span data-ttu-id="e6c68-105">ByPEId (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6c68-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="e6c68-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e6c68-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e6c68-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e6c68-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e6c68-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e6c68-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6c68-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e6c68-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e6c68-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="e6c68-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6c68-121">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6c68-121">DESCRIPTION</span></span>
<span data-ttu-id="e6c68-122">O cmdlet **Start-AzureSiteRecoveryTestFailoverJob** inicia o failover de teste de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e6c68-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="e6c68-123">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet **Get-AzureRMSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="e6c68-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="e6c68-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6c68-124">EXAMPLES</span></span>

### <span data-ttu-id="e6c68-125">Exemplo 1: iniciar um failover de teste</span><span class="sxs-lookup"><span data-stu-id="e6c68-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e6c68-126">O primeiro comando usa o cmdlet **Get-AzureSiteRecoveryProtectionContainer** para obter um contêiner protegido e, em seguida, armazena-o na variável $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="e6c68-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="e6c68-127">O segundo comando obtém as entidades protegidas que pertencem ao contêiner protegido armazenado no $ProtectionContainer usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="e6c68-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="e6c68-128">O comando armazena os resultados na variável $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="e6c68-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="e6c68-129">O comando final inicia a operação de failover de teste para as entidades protegidas armazenadas no $ProtectionEntity e especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="e6c68-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="e6c68-130">Exemplo 2: iniciar um failover de teste usando um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="e6c68-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="e6c68-131">Este comando obtém o plano de recuperação chamado RecoveryPlan01 para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="e6c68-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="e6c68-132">O comando armazena o plano na variável $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="e6c68-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="e6c68-133">O segundo comando inicia a operação de failover de teste para o plano de recuperação armazenado no $RecoveryPlan e especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="e6c68-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="e6c68-134">OS</span><span class="sxs-lookup"><span data-stu-id="e6c68-134">PARAMETERS</span></span>

### <span data-ttu-id="e6c68-135">-Direction</span><span class="sxs-lookup"><span data-stu-id="e6c68-135">-Direction</span></span>
<span data-ttu-id="e6c68-136">Especifica a direção de failover.</span><span class="sxs-lookup"><span data-stu-id="e6c68-136">Specifies the failover direction.</span></span>
<span data-ttu-id="e6c68-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e6c68-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6c68-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e6c68-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="e6c68-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e6c68-139">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="e6c68-140">-LogicalNetworkId</span></span>
<span data-ttu-id="e6c68-141">Especifica a ID da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="e6c68-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-142">-Rede</span><span class="sxs-lookup"><span data-stu-id="e6c68-142">-Network</span></span>
<span data-ttu-id="e6c68-143">Especifica o objeto de rede a ser usado para failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e6c68-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="e6c68-144">Para obter uma rede, use o cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="e6c68-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="e6c68-145">-NetworkType</span></span>
<span data-ttu-id="e6c68-146">Especifica o tipo de rede a ser usado para failover de teste.</span><span class="sxs-lookup"><span data-stu-id="e6c68-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="e6c68-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e6c68-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6c68-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e6c68-148">None</span></span>
- <span data-ttu-id="e6c68-149">Novo</span><span class="sxs-lookup"><span data-stu-id="e6c68-149">New</span></span>
- <span data-ttu-id="e6c68-150">Atual</span><span class="sxs-lookup"><span data-stu-id="e6c68-150">Existing</span></span>

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

### <span data-ttu-id="e6c68-151">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e6c68-151">-Profile</span></span>
<span data-ttu-id="e6c68-152">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e6c68-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6c68-153">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e6c68-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="e6c68-154">-ProtectionContainerId</span></span>
<span data-ttu-id="e6c68-155">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="e6c68-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="e6c68-156">Esse cmdlet inicia o trabalho para uma máquina virtual protegida que pertence ao contêiner que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="e6c68-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e6c68-157">-ProtectionEntity</span></span>
<span data-ttu-id="e6c68-158">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="e6c68-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="e6c68-159">-ProtectionEntityId</span></span>
<span data-ttu-id="e6c68-160">Especifica a ID de uma máquina virtual protegida para a qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6c68-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6c68-161">-RecoveryPlan</span></span>
<span data-ttu-id="e6c68-162">Especifica um plano de recuperação para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6c68-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="e6c68-163">-RpId</span></span>
<span data-ttu-id="e6c68-164">Especifica a ID de um plano de recuperação para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6c68-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="e6c68-165">-VmNetworkId</span></span>
<span data-ttu-id="e6c68-166">Especifica a ID da rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6c68-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e6c68-167">-WaitForCompletion</span></span>
<span data-ttu-id="e6c68-168">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6c68-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c68-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c68-169">CommonParameters</span></span>
<span data-ttu-id="e6c68-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c68-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c68-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c68-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c68-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6c68-172">INPUTS</span></span>

## <span data-ttu-id="e6c68-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6c68-173">OUTPUTS</span></span>

## <span data-ttu-id="e6c68-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6c68-174">NOTES</span></span>

## <span data-ttu-id="e6c68-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6c68-175">RELATED LINKS</span></span>

[<span data-ttu-id="e6c68-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e6c68-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e6c68-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="e6c68-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="e6c68-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e6c68-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="e6c68-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e6c68-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e6c68-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e6c68-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


