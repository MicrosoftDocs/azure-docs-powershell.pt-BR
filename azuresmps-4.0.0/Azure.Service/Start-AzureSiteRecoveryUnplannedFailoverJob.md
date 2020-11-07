---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945806"
---
# <span data-ttu-id="a0b25-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a0b25-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="a0b25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0b25-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b25-103">Inicia o failover não planejado para uma entidade ou um plano de proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="a0b25-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="a0b25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0b25-104">SYNTAX</span></span>

### <span data-ttu-id="a0b25-105">ByRPId (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0b25-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0b25-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="a0b25-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0b25-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a0b25-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b25-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="a0b25-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0b25-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0b25-109">DESCRIPTION</span></span>
<span data-ttu-id="a0b25-110">O cmdlet **Start-AzureSiteRecoveryUnplannedFailoverJob** inicia o failover não planejado de uma entidade de proteção do Azure site Recovery ou um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a0b25-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="a0b25-111">Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="a0b25-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="a0b25-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0b25-112">EXAMPLES</span></span>

### <span data-ttu-id="a0b25-113">Exemplo 1: iniciar um trabalho de failover não planejado</span><span class="sxs-lookup"><span data-stu-id="a0b25-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="a0b25-114">O primeiro comando obtém um contêiner protegido usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena-o na variável $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="a0b25-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="a0b25-115">O segundo comando obtém as entidades protegidas que pertencem ao contêiner protegido armazenado no $ProtectionContainer usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="a0b25-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="a0b25-116">O comando armazena os resultados na variável $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="a0b25-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="a0b25-117">O comando final inicia o failover para as entidades protegidas armazenadas no $ProtectionEntity e especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="a0b25-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="a0b25-118">OS</span><span class="sxs-lookup"><span data-stu-id="a0b25-118">PARAMETERS</span></span>

### <span data-ttu-id="a0b25-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="a0b25-119">-Direction</span></span>
<span data-ttu-id="a0b25-120">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="a0b25-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="a0b25-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a0b25-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0b25-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a0b25-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="a0b25-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a0b25-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a0b25-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="a0b25-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="a0b25-125">Indica que a ação pode executar ações no lado da fonte.</span><span class="sxs-lookup"><span data-stu-id="a0b25-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="a0b25-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="a0b25-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="a0b25-127">Indica que operações do site de origem podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a0b25-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b25-128">-Primaryaction</span><span class="sxs-lookup"><span data-stu-id="a0b25-128">-PrimaryAction</span></span>
<span data-ttu-id="a0b25-129">Indica que as ações do site primário são necessárias.</span><span class="sxs-lookup"><span data-stu-id="a0b25-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b25-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0b25-130">-Profile</span></span>
<span data-ttu-id="a0b25-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a0b25-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0b25-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a0b25-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0b25-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="a0b25-133">-ProtectionContainerId</span></span>
<span data-ttu-id="a0b25-134">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="a0b25-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="a0b25-135">Esse cmdlet inicia o trabalho para uma máquina virtual protegida que pertence ao contêiner que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="a0b25-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a0b25-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a0b25-136">-ProtectionEntity</span></span>
<span data-ttu-id="a0b25-137">Especifica o objeto da entidade de proteção do site.</span><span class="sxs-lookup"><span data-stu-id="a0b25-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="a0b25-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="a0b25-138">-ProtectionEntityId</span></span>
<span data-ttu-id="a0b25-139">Especifica a ID de uma máquina virtual protegida para a qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0b25-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="a0b25-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a0b25-140">-RecoveryPlan</span></span>
<span data-ttu-id="a0b25-141">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a0b25-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="a0b25-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="a0b25-142">-RPId</span></span>
<span data-ttu-id="a0b25-143">Especifica a ID de um plano de recuperação para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0b25-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="a0b25-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a0b25-144">-WaitForCompletion</span></span>
<span data-ttu-id="a0b25-145">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0b25-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="a0b25-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b25-146">CommonParameters</span></span>
<span data-ttu-id="a0b25-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0b25-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b25-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b25-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b25-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0b25-149">INPUTS</span></span>

## <span data-ttu-id="a0b25-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0b25-150">OUTPUTS</span></span>

## <span data-ttu-id="a0b25-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0b25-151">NOTES</span></span>

## <span data-ttu-id="a0b25-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0b25-152">RELATED LINKS</span></span>

[<span data-ttu-id="a0b25-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a0b25-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="a0b25-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a0b25-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="a0b25-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a0b25-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="a0b25-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a0b25-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


