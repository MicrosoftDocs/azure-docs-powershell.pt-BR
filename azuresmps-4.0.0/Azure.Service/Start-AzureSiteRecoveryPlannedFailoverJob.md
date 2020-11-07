---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945751"
---
# <span data-ttu-id="57600-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="57600-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="57600-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57600-102">SYNOPSIS</span></span>
<span data-ttu-id="57600-103">Inicia uma operação de failover planejado de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="57600-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="57600-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57600-104">SYNTAX</span></span>

### <span data-ttu-id="57600-105">ByRPId (padrão)</span><span class="sxs-lookup"><span data-stu-id="57600-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57600-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="57600-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57600-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="57600-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57600-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="57600-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57600-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57600-109">DESCRIPTION</span></span>
<span data-ttu-id="57600-110">O cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** inicia um failover planejado para uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="57600-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="57600-111">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="57600-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="57600-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57600-112">EXAMPLES</span></span>

### <span data-ttu-id="57600-113">Exemplo 1: iniciar um trabalho de failover planejado</span><span class="sxs-lookup"><span data-stu-id="57600-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

<span data-ttu-id="57600-114">O primeiro comando obtém todos os contêineres protegidos no cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena os resultados na variável $container.</span><span class="sxs-lookup"><span data-stu-id="57600-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="57600-115">Neste exemplo, há um único contêiner.</span><span class="sxs-lookup"><span data-stu-id="57600-115">In this example, there is a single container.</span></span>

<span data-ttu-id="57600-116">O segundo comando obtém as máquinas virtuais protegidas que pertencem ao contêiner armazenado no $Container usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="57600-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="57600-117">O comando armazena os resultados na variável $Protected.</span><span class="sxs-lookup"><span data-stu-id="57600-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="57600-118">O comando final inicia o trabalho de failover na direção PrimaryToRecovery para as máquinas virtuais protegidas armazenadas em $Protected.</span><span class="sxs-lookup"><span data-stu-id="57600-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="57600-119">OS</span><span class="sxs-lookup"><span data-stu-id="57600-119">PARAMETERS</span></span>

### <span data-ttu-id="57600-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="57600-120">-Direction</span></span>
<span data-ttu-id="57600-121">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="57600-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="57600-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="57600-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57600-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="57600-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="57600-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="57600-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="57600-125">-Otimizar</span><span class="sxs-lookup"><span data-stu-id="57600-125">-Optimize</span></span>
<span data-ttu-id="57600-126">Especifica o que otimizar para.</span><span class="sxs-lookup"><span data-stu-id="57600-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="57600-127">Esse parâmetro se aplica para failover de um site do Azure para um site local que requer uma sincronização de dados significativa.</span><span class="sxs-lookup"><span data-stu-id="57600-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="57600-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="57600-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57600-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="57600-129">ForDowntime</span></span>
- <span data-ttu-id="57600-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="57600-130">ForSynchronization</span></span>

<span data-ttu-id="57600-131">Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.</span><span class="sxs-lookup"><span data-stu-id="57600-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="57600-132">A sincronização é realizada sem desligar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57600-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="57600-133">Após a conclusão da sincronização, o trabalho será suspenso.</span><span class="sxs-lookup"><span data-stu-id="57600-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="57600-134">Retome o trabalho para executar uma operação de sincronização adicional que desative a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57600-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="57600-135">Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover, para que a sincronização de dados seja minimizada.</span><span class="sxs-lookup"><span data-stu-id="57600-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="57600-136">Como essa configuração está habilitada, a máquina virtual é desligada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="57600-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="57600-137">A sincronização começará após o desligamento para concluir a operação de failover.</span><span class="sxs-lookup"><span data-stu-id="57600-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="57600-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="57600-138">-Profile</span></span>
<span data-ttu-id="57600-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="57600-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57600-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="57600-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57600-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="57600-141">-ProtectionContainerId</span></span>
<span data-ttu-id="57600-142">Especifica a ID do contêiner protegido para a qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="57600-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57600-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="57600-143">-ProtectionEntity</span></span>
<span data-ttu-id="57600-144">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="57600-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57600-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="57600-145">-ProtectionEntityId</span></span>
<span data-ttu-id="57600-146">Especifica um objeto **ASRProtectionEntity** para o qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="57600-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="57600-147">Para obter um objeto **ASRProtectionEntity** , use o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="57600-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57600-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57600-148">-RecoveryPlan</span></span>
<span data-ttu-id="57600-149">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="57600-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="57600-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="57600-150">-RPId</span></span>
<span data-ttu-id="57600-151">Especifica a ID de um plano de recuperação para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="57600-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57600-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="57600-152">-WaitForCompletion</span></span>
<span data-ttu-id="57600-153">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57600-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="57600-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57600-154">CommonParameters</span></span>
<span data-ttu-id="57600-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57600-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57600-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57600-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57600-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57600-157">INPUTS</span></span>

## <span data-ttu-id="57600-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57600-158">OUTPUTS</span></span>

## <span data-ttu-id="57600-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57600-159">NOTES</span></span>

## <span data-ttu-id="57600-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57600-160">RELATED LINKS</span></span>

[<span data-ttu-id="57600-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="57600-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="57600-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="57600-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


