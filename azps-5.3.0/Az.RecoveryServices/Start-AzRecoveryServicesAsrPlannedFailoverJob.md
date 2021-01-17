---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428832"
---
# <span data-ttu-id="05574-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="05574-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="05574-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05574-102">SYNOPSIS</span></span>
<span data-ttu-id="05574-103">Inicia uma operação de failover planejada.</span><span class="sxs-lookup"><span data-stu-id="05574-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="05574-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05574-104">SYNTAX</span></span>

### <span data-ttu-id="05574-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="05574-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05574-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="05574-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05574-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05574-107">DESCRIPTION</span></span>
<span data-ttu-id="05574-108">O cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** inicia um failover planejado para um item protegido de replicação do Azure site Recovery ou plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="05574-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="05574-109">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="05574-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="05574-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05574-110">EXAMPLES</span></span>

### <span data-ttu-id="05574-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05574-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="05574-112">Inicia o failover planejado para o plano de recuperação ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="05574-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="05574-113">OS</span><span class="sxs-lookup"><span data-stu-id="05574-113">PARAMETERS</span></span>

### <span data-ttu-id="05574-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="05574-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="05574-115">Crie a máquina virtual se não for encontrada durante a retomada de failback para a região primária (usada na recuperação de localização alternativa). Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05574-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05574-116">Sim</span><span class="sxs-lookup"><span data-stu-id="05574-116">Yes</span></span>
- <span data-ttu-id="05574-117">Não</span><span class="sxs-lookup"><span data-stu-id="05574-117">No</span></span>

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

### <span data-ttu-id="05574-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="05574-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="05574-119">Especifica o arquivo de certificado primário.</span><span class="sxs-lookup"><span data-stu-id="05574-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="05574-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="05574-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="05574-121">Especifica o arquivo de certificado secundário.</span><span class="sxs-lookup"><span data-stu-id="05574-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="05574-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05574-122">-DefaultProfile</span></span>
<span data-ttu-id="05574-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05574-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="05574-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="05574-124">-Direction</span></span>
<span data-ttu-id="05574-125">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="05574-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="05574-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05574-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05574-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="05574-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="05574-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="05574-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="05574-129">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="05574-129">-Optimize</span></span>
<span data-ttu-id="05574-130">Especifica o que otimizar para.</span><span class="sxs-lookup"><span data-stu-id="05574-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="05574-131">Esse parâmetro se aplica quando o failover é feito de um site do Azure para um site local que requer sincronização de dados substancial.</span><span class="sxs-lookup"><span data-stu-id="05574-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="05574-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="05574-132">Valid values are:</span></span>

- <span data-ttu-id="05574-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="05574-133">ForDowntime</span></span>
- <span data-ttu-id="05574-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="05574-134">ForSynchronization</span></span>

<span data-ttu-id="05574-135">Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="05574-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="05574-136">A sincronização é realizada sem desligar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="05574-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="05574-137">Após a conclusão da sincronização, o trabalho será suspenso.</span><span class="sxs-lookup"><span data-stu-id="05574-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="05574-138">Retome o trabalho para executar uma operação de sincronização adicional que desative a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="05574-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="05574-139">Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover, para que a sincronização de dados seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="05574-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="05574-140">Com essa configuração habilitada, a máquina virtual é encerrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="05574-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="05574-141">A sincronização começará após o desligamento para concluir a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="05574-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="05574-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="05574-142">-RecoveryPlan</span></span>
<span data-ttu-id="05574-143">Especifica o objeto do plano de recuperação ASR correspondente ao plano de recuperação para failover.</span><span class="sxs-lookup"><span data-stu-id="05574-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="05574-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="05574-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="05574-145">Especifica o objeto de item protegido de replicação ASR correspondente ao item de replicação protegida a partir de failover.</span><span class="sxs-lookup"><span data-stu-id="05574-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="05574-146">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="05574-146">-ServicesProvider</span></span>
<span data-ttu-id="05574-147">Identifica o host para o qual criar a máquina virtual durante a falha em um local alternativo especificando o objeto do provedor de serviços ASR correspondente ao provedor de serviços ASR em execução no host.</span><span class="sxs-lookup"><span data-stu-id="05574-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="05574-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05574-148">-Confirm</span></span>
<span data-ttu-id="05574-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05574-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05574-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05574-150">-WhatIf</span></span>
<span data-ttu-id="05574-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05574-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05574-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05574-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05574-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05574-153">CommonParameters</span></span>
<span data-ttu-id="05574-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05574-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05574-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05574-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05574-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05574-156">INPUTS</span></span>

### <span data-ttu-id="05574-157">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="05574-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="05574-158">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="05574-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="05574-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05574-159">OUTPUTS</span></span>

### <span data-ttu-id="05574-160">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="05574-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05574-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05574-161">NOTES</span></span>

## <span data-ttu-id="05574-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05574-162">RELATED LINKS</span></span>
