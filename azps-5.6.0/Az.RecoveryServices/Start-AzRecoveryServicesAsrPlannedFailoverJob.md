---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: 78aa310d6fd3cdb7a27de066e234744b3e450520
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891772"
---
# <span data-ttu-id="ead2b-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ead2b-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="ead2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead2b-102">SYNOPSIS</span></span>
<span data-ttu-id="ead2b-103">Inicia uma operação de failover planejada.</span><span class="sxs-lookup"><span data-stu-id="ead2b-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="ead2b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ead2b-104">SYNTAX</span></span>

### <span data-ttu-id="ead2b-105">ByRPIObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ead2b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ead2b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ead2b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ead2b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ead2b-107">DESCRIPTION</span></span>
<span data-ttu-id="ead2b-108">O cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** inicia um failover planejado para um item ou plano de recuperação protegido de replicação de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="ead2b-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ead2b-109">Você pode verificar se o trabalho é bem-sucedido usando Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead2b-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ead2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ead2b-110">EXAMPLES</span></span>

### <span data-ttu-id="ead2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ead2b-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="ead2b-112">Inicia o failover planejado para o plano de recuperação ASR especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="ead2b-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ead2b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ead2b-113">PARAMETERS</span></span>

### <span data-ttu-id="ead2b-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="ead2b-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="ead2b-115">Crie a máquina virtual se não for encontrada enquanto estiver falhando na região primária (usada na recuperação de local alternativo).) Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ead2b-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ead2b-116">Sim</span><span class="sxs-lookup"><span data-stu-id="ead2b-116">Yes</span></span>
- <span data-ttu-id="ead2b-117">Não</span><span class="sxs-lookup"><span data-stu-id="ead2b-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead2b-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ead2b-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ead2b-119">Especifica o arquivo de certificado principal.</span><span class="sxs-lookup"><span data-stu-id="ead2b-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="ead2b-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ead2b-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ead2b-121">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="ead2b-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="ead2b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead2b-122">-DefaultProfile</span></span>
<span data-ttu-id="ead2b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ead2b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ead2b-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="ead2b-124">-Direction</span></span>
<span data-ttu-id="ead2b-125">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="ead2b-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ead2b-126">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ead2b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ead2b-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ead2b-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="ead2b-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ead2b-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ead2b-129">-Optimize</span><span class="sxs-lookup"><span data-stu-id="ead2b-129">-Optimize</span></span>
<span data-ttu-id="ead2b-130">Especifica para o que otimizar.</span><span class="sxs-lookup"><span data-stu-id="ead2b-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="ead2b-131">Esse parâmetro se aplica quando o failover é feito de um site do Azure para um site local que requer uma sincronização substancial de dados.</span><span class="sxs-lookup"><span data-stu-id="ead2b-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="ead2b-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="ead2b-132">Valid values are:</span></span>

- <span data-ttu-id="ead2b-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="ead2b-133">ForDowntime</span></span>
- <span data-ttu-id="ead2b-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="ead2b-134">ForSynchronization</span></span>

<span data-ttu-id="ead2b-135">Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="ead2b-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="ead2b-136">A sincronização é executada sem desligar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ead2b-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="ead2b-137">Depois que a sincronização for concluída, o trabalho será suspenso.</span><span class="sxs-lookup"><span data-stu-id="ead2b-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="ead2b-138">Retome o trabalho para fazer uma operação de sincronização adicional que desligue a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ead2b-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="ead2b-139">Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover apenas para que a sincronização de dados seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="ead2b-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="ead2b-140">Com essa configuração habilitada, a máquina virtual é fechada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ead2b-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="ead2b-141">A sincronização é iniciada após o desligamento para concluir a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="ead2b-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead2b-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ead2b-142">-RecoveryPlan</span></span>
<span data-ttu-id="ead2b-143">Especifica o objeto do plano de recuperação ASR correspondente ao plano de recuperação a ser reprovado.</span><span class="sxs-lookup"><span data-stu-id="ead2b-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead2b-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ead2b-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ead2b-145">Especifica o objeto de item protegido de replicação ASR correspondente ao item protegido de replicação a ser reprovado.</span><span class="sxs-lookup"><span data-stu-id="ead2b-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead2b-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ead2b-146">-ServicesProvider</span></span>
<span data-ttu-id="ead2b-147">Identifica o host para o qual criar a máquina virtual ao falhar em um local alternativo especificando o objeto do provedor de serviços ASR correspondente ao provedor de serviços ASR em execução no host.</span><span class="sxs-lookup"><span data-stu-id="ead2b-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead2b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ead2b-148">-Confirm</span></span>
<span data-ttu-id="ead2b-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead2b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead2b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead2b-150">-WhatIf</span></span>
<span data-ttu-id="ead2b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ead2b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ead2b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ead2b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead2b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead2b-153">CommonParameters</span></span>
<span data-ttu-id="ead2b-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead2b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead2b-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead2b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead2b-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ead2b-156">INPUTS</span></span>

### <span data-ttu-id="ead2b-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ead2b-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ead2b-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ead2b-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ead2b-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ead2b-159">OUTPUTS</span></span>

### <span data-ttu-id="ead2b-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ead2b-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ead2b-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="ead2b-161">NOTES</span></span>

## <span data-ttu-id="ead2b-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ead2b-162">RELATED LINKS</span></span>
