---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945778"
---
# <span data-ttu-id="05f58-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="05f58-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="05f58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05f58-102">SYNOPSIS</span></span>
<span data-ttu-id="05f58-103">Inicia a ação de failover de confirmação para um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="05f58-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="05f58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05f58-104">SYNTAX</span></span>

### <span data-ttu-id="05f58-105">ByRPId (padrão)</span><span class="sxs-lookup"><span data-stu-id="05f58-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05f58-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="05f58-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05f58-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="05f58-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="05f58-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="05f58-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05f58-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05f58-109">DESCRIPTION</span></span>
<span data-ttu-id="05f58-110">O cmdlet **Start-AzureSiteRecoveryCommitFailoverJob** inicia o processo de failover de confirmação para um objeto do Azure site Recovery após uma operação de failover.</span><span class="sxs-lookup"><span data-stu-id="05f58-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="05f58-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05f58-111">EXAMPLES</span></span>

### <span data-ttu-id="05f58-112">Exemplo 1: iniciar um trabalho de failover de confirmação</span><span class="sxs-lookup"><span data-stu-id="05f58-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="05f58-113">O primeiro comando obtém todos os contêineres protegidos para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena os resultados na variável $container.</span><span class="sxs-lookup"><span data-stu-id="05f58-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="05f58-114">O segundo comando obtém as máquinas virtuais protegidas que pertencem ao contêiner armazenado no $Container usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="05f58-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="05f58-115">O comando armazena os resultados na variável $Protected.</span><span class="sxs-lookup"><span data-stu-id="05f58-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="05f58-116">O comando final inicia o trabalho de failover para os objetos protegidos armazenados em $Protected.</span><span class="sxs-lookup"><span data-stu-id="05f58-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="05f58-117">OS</span><span class="sxs-lookup"><span data-stu-id="05f58-117">PARAMETERS</span></span>

### <span data-ttu-id="05f58-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="05f58-118">-Direction</span></span>
<span data-ttu-id="05f58-119">Especifica a direção do failover.</span><span class="sxs-lookup"><span data-stu-id="05f58-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="05f58-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="05f58-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05f58-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="05f58-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="05f58-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="05f58-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="05f58-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="05f58-123">-Profile</span></span>
<span data-ttu-id="05f58-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="05f58-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05f58-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="05f58-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05f58-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="05f58-126">-ProtectionContainerId</span></span>
<span data-ttu-id="05f58-127">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="05f58-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="05f58-128">Esse cmdlet inicia o trabalho para uma máquina virtual protegida que pertence ao contêiner que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="05f58-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="05f58-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="05f58-129">-ProtectionEntity</span></span>
<span data-ttu-id="05f58-130">Especifica um objeto **ASRProtectionEntity** para o qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="05f58-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="05f58-131">Para obter um objeto **ASRProtectionEntity** , use o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="05f58-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="05f58-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="05f58-132">-ProtectionEntityId</span></span>
<span data-ttu-id="05f58-133">Especifica a ID de uma máquina virtual protegida para a qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="05f58-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="05f58-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="05f58-134">-RecoveryPlan</span></span>
<span data-ttu-id="05f58-135">Especifica um objeto de plano de recuperação para o qual iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="05f58-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="05f58-136">Para obter um objeto **ASRRecoveryPlan** , use o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="05f58-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="05f58-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="05f58-137">-RPId</span></span>
<span data-ttu-id="05f58-138">Especifica a ID de um plano de recuperação para iniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="05f58-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="05f58-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="05f58-139">-WaitForCompletion</span></span>
<span data-ttu-id="05f58-140">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="05f58-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="05f58-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f58-141">CommonParameters</span></span>
<span data-ttu-id="05f58-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f58-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f58-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f58-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f58-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05f58-144">INPUTS</span></span>

## <span data-ttu-id="05f58-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05f58-145">OUTPUTS</span></span>

## <span data-ttu-id="05f58-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05f58-146">NOTES</span></span>

## <span data-ttu-id="05f58-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05f58-147">RELATED LINKS</span></span>

[<span data-ttu-id="05f58-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="05f58-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="05f58-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="05f58-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="05f58-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="05f58-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


