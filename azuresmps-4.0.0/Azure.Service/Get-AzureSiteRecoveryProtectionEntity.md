---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945588"
---
# <span data-ttu-id="c48ac-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c48ac-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="c48ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c48ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c48ac-103">Obtém as entidades protegidas ou protegidas em um cofre de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="c48ac-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="c48ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c48ac-104">SYNTAX</span></span>

### <span data-ttu-id="c48ac-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c48ac-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c48ac-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="c48ac-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c48ac-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="c48ac-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c48ac-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c48ac-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c48ac-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="c48ac-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c48ac-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="c48ac-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c48ac-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c48ac-111">DESCRIPTION</span></span>
<span data-ttu-id="c48ac-112">O cmdlet **Get-AzureSiteRecoveryProtectionEntity** Obtém as entidades protegidas ou protegidas, como máquinas virtuais, no cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="c48ac-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c48ac-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c48ac-113">EXAMPLES</span></span>

### <span data-ttu-id="c48ac-114">Exemplo 1: exibir uma máquina virtual protegida em um contêiner</span><span class="sxs-lookup"><span data-stu-id="c48ac-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="c48ac-115">O primeiro comando obtém um contêiner protegido usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e armazena esse objeto na variável $container.</span><span class="sxs-lookup"><span data-stu-id="c48ac-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="c48ac-116">O segundo comando obtém a máquina virtual protegida que pertence ao contêiner no $Container e, em seguida, exibe-a.</span><span class="sxs-lookup"><span data-stu-id="c48ac-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="c48ac-117">OS</span><span class="sxs-lookup"><span data-stu-id="c48ac-117">PARAMETERS</span></span>

### <span data-ttu-id="c48ac-118">-ID</span><span class="sxs-lookup"><span data-stu-id="c48ac-118">-Id</span></span>
<span data-ttu-id="c48ac-119">Especifica a ID de uma entidade de proteção a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c48ac-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48ac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c48ac-120">-Name</span></span>
<span data-ttu-id="c48ac-121">Especifica o nome de uma entidade de proteção a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c48ac-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48ac-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c48ac-122">-Profile</span></span>
<span data-ttu-id="c48ac-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c48ac-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c48ac-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c48ac-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c48ac-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c48ac-125">-ProtectionContainer</span></span>
<span data-ttu-id="c48ac-126">Especifica um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="c48ac-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ac-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="c48ac-127">-ProtectionContainerId</span></span>
<span data-ttu-id="c48ac-128">Especifica a ID de um contêiner protegido.</span><span class="sxs-lookup"><span data-stu-id="c48ac-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48ac-129">CommonParameters</span></span>
<span data-ttu-id="c48ac-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48ac-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48ac-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48ac-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c48ac-132">INPUTS</span></span>

## <span data-ttu-id="c48ac-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c48ac-133">OUTPUTS</span></span>

## <span data-ttu-id="c48ac-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c48ac-134">NOTES</span></span>

## <span data-ttu-id="c48ac-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c48ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="c48ac-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c48ac-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="c48ac-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c48ac-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="c48ac-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c48ac-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


