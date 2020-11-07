---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945848"
---
# <span data-ttu-id="69be0-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="69be0-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="69be0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69be0-102">SYNOPSIS</span></span>
<span data-ttu-id="69be0-103">Inicia um trabalho de associação de política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="69be0-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="69be0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69be0-104">SYNTAX</span></span>

### <span data-ttu-id="69be0-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="69be0-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="69be0-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="69be0-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69be0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69be0-107">DESCRIPTION</span></span>
<span data-ttu-id="69be0-108">O cmdlet **Start-AzureSiteRecoveryProtectionProfileAssociationJob** inicia um trabalho de associação para associar uma política de replicação a um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="69be0-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="69be0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69be0-109">EXAMPLES</span></span>

### <span data-ttu-id="69be0-110">Exemplo 1: associar um perfil de proteção</span><span class="sxs-lookup"><span data-stu-id="69be0-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="69be0-111">O primeiro comando obtém um contêiner de proteção usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena esse contêiner na variável $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="69be0-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="69be0-112">O segundo comando cria um perfil de proteção usando o cmdlet **New-AzureSiteRecoveryProtectionProfileObject** e armazena esse perfil de proteção na variável $ProtectionProfile.</span><span class="sxs-lookup"><span data-stu-id="69be0-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="69be0-113">O terceiro comando obtém um contêiner de proteção e, em seguida, armazena-o na variável $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="69be0-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="69be0-114">O comando final associa o perfil de proteção armazenado em $ProtectionProfile ao contêiner armazenado no $ProtectionContainer 01 como o contêiner de proteção principal.</span><span class="sxs-lookup"><span data-stu-id="69be0-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="69be0-115">O comando associa o contêiner armazenado no $ProtectionContainer 02 como o contêiner de proteção de recuperação.</span><span class="sxs-lookup"><span data-stu-id="69be0-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="69be0-116">OS</span><span class="sxs-lookup"><span data-stu-id="69be0-116">PARAMETERS</span></span>

### <span data-ttu-id="69be0-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="69be0-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="69be0-118">Especifica o contêiner de proteção principal no qual aplicar as configurações do perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="69be0-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be0-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="69be0-119">-Profile</span></span>
<span data-ttu-id="69be0-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="69be0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69be0-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="69be0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69be0-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="69be0-122">-ProtectionProfile</span></span>
<span data-ttu-id="69be0-123">Especifica as configurações de perfil de proteção a serem aplicadas aos contêineres de proteção.</span><span class="sxs-lookup"><span data-stu-id="69be0-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="69be0-124">Para obter um objeto **ASRProtectionProfile** , use o cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="69be0-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69be0-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="69be0-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="69be0-126">Especifica o contêiner de proteção de recuperação no qual aplicar as configurações de perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="69be0-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69be0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be0-127">CommonParameters</span></span>
<span data-ttu-id="69be0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69be0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69be0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69be0-130">INPUTS</span></span>

## <span data-ttu-id="69be0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69be0-131">OUTPUTS</span></span>

## <span data-ttu-id="69be0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69be0-132">NOTES</span></span>

## <span data-ttu-id="69be0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69be0-133">RELATED LINKS</span></span>

[<span data-ttu-id="69be0-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="69be0-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="69be0-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="69be0-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="69be0-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="69be0-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


