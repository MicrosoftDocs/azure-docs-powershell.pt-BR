---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946400"
---
# <span data-ttu-id="cdd81-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="cdd81-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="cdd81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdd81-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd81-103">Atualiza o servidor de origem e de destino para a proteção de um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="cdd81-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="cdd81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdd81-104">SYNTAX</span></span>

### <span data-ttu-id="cdd81-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="cdd81-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdd81-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="cdd81-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdd81-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="cdd81-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdd81-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="cdd81-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cdd81-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdd81-109">DESCRIPTION</span></span>
<span data-ttu-id="cdd81-110">O cmdlet **Update-AzureSiteRecoveryProtectionDirection** atualiza o servidor de origem e de destino para a proteção de um objeto do Azure site Recovery após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="cdd81-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="cdd81-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdd81-111">EXAMPLES</span></span>

### <span data-ttu-id="cdd81-112">Exemplo 1: modificar a direção de um objeto protegido em um contêiner</span><span class="sxs-lookup"><span data-stu-id="cdd81-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
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

<span data-ttu-id="cdd81-113">O primeiro comando obtém os contêineres protegidos no cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena-os na variável $container.</span><span class="sxs-lookup"><span data-stu-id="cdd81-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="cdd81-114">O segundo comando obtém as máquinas virtuais que pertencem ao contêiner armazenado no $Container usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="cdd81-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="cdd81-115">O comando armazena os resultados na variável $Protected.</span><span class="sxs-lookup"><span data-stu-id="cdd81-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="cdd81-116">O comando final define a direção para RecoverToPrimary para os objetos armazenados em $Protected.</span><span class="sxs-lookup"><span data-stu-id="cdd81-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="cdd81-117">OS</span><span class="sxs-lookup"><span data-stu-id="cdd81-117">PARAMETERS</span></span>

### <span data-ttu-id="cdd81-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="cdd81-118">-Direction</span></span>
<span data-ttu-id="cdd81-119">Especifica a direção da confirmação.</span><span class="sxs-lookup"><span data-stu-id="cdd81-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="cdd81-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cdd81-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cdd81-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="cdd81-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="cdd81-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="cdd81-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="cdd81-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cdd81-123">-Profile</span></span>
<span data-ttu-id="cdd81-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cdd81-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cdd81-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cdd81-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cdd81-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="cdd81-126">-ProtectionContainerId</span></span>
<span data-ttu-id="cdd81-127">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="cdd81-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="cdd81-128">Esse cmdlet modifica a direção de uma máquina virtual protegida que pertence ao contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cdd81-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdd81-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="cdd81-129">-ProtectionEntity</span></span>
<span data-ttu-id="cdd81-130">Especifica o objeto da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="cdd81-130">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="cdd81-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="cdd81-131">-ProtectionEntityId</span></span>
<span data-ttu-id="cdd81-132">Especifica a ID de uma máquina virtual protegida.</span><span class="sxs-lookup"><span data-stu-id="cdd81-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="cdd81-133">Esse cmdlet modifica a direção da máquina virtual protegida que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cdd81-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdd81-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cdd81-134">-RecoveryPlan</span></span>
<span data-ttu-id="cdd81-135">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cdd81-135">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="cdd81-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="cdd81-136">-RPId</span></span>
<span data-ttu-id="cdd81-137">Especifica a ID de um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cdd81-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="cdd81-138">Esse cmdlet modifica a direção do plano de recuperação que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cdd81-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdd81-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cdd81-139">-WaitForCompletion</span></span>
<span data-ttu-id="cdd81-140">Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cdd81-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="cdd81-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd81-141">CommonParameters</span></span>
<span data-ttu-id="cdd81-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd81-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd81-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd81-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd81-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdd81-144">INPUTS</span></span>

## <span data-ttu-id="cdd81-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdd81-145">OUTPUTS</span></span>

## <span data-ttu-id="cdd81-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdd81-146">NOTES</span></span>

## <span data-ttu-id="cdd81-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdd81-147">RELATED LINKS</span></span>

[<span data-ttu-id="cdd81-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cdd81-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="cdd81-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="cdd81-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


