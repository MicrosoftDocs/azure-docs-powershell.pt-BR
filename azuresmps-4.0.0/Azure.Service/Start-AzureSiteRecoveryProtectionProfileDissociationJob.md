---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946410"
---
# <span data-ttu-id="e7dcc-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="e7dcc-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="e7dcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="e7dcc-103">Inicia um trabalho de dissociação em uma política de replicação associada a um contêiner de proteção de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="e7dcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7dcc-104">SYNTAX</span></span>

### <span data-ttu-id="e7dcc-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7dcc-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e7dcc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e7dcc-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7dcc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7dcc-107">DESCRIPTION</span></span>
<span data-ttu-id="e7dcc-108">O cmdlet **Start-AzureSiteRecoveryProtectionProfileDissociationJob** inicia um trabalho de dissociação na política de replicação associada a um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="e7dcc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7dcc-109">EXAMPLES</span></span>

### <span data-ttu-id="e7dcc-110">Exemplo 1: dissociar um perfil de proteção</span><span class="sxs-lookup"><span data-stu-id="e7dcc-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e7dcc-111">O primeiro comando obtém um contêiner de proteção usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena esse contêiner na variável $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="e7dcc-112">O segundo comando obtém um contêiner de proteção e, em seguida, armazena-o na variável $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="e7dcc-113">O comando final dissocia o perfil de proteção do contêiner armazenado em $ProtectionContainer 01 como o contêiner de proteção principal.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="e7dcc-114">O comando dissocia o contêiner armazenado no $ProtectionContainer 02 como o contêiner de proteção de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="e7dcc-115">OS</span><span class="sxs-lookup"><span data-stu-id="e7dcc-115">PARAMETERS</span></span>

### <span data-ttu-id="e7dcc-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e7dcc-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="e7dcc-117">Especifica um contêiner de proteção principal.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="e7dcc-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e7dcc-118">-Profile</span></span>
<span data-ttu-id="e7dcc-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7dcc-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7dcc-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="e7dcc-121">-ProtectionProfile</span></span>
<span data-ttu-id="e7dcc-122">Especifica as configurações de perfil de proteção para desassociar dos contêineres de proteção.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="e7dcc-123">Especifica as configurações de perfil de proteção a serem aplicadas aos contêineres de proteção.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="e7dcc-124">Para obter um objeto **ASRProtectionProfile** , use o cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="e7dcc-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e7dcc-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="e7dcc-126">Especifica um contêiner de proteção de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="e7dcc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7dcc-127">CommonParameters</span></span>
<span data-ttu-id="e7dcc-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7dcc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7dcc-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7dcc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7dcc-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7dcc-130">INPUTS</span></span>

## <span data-ttu-id="e7dcc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7dcc-131">OUTPUTS</span></span>

## <span data-ttu-id="e7dcc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7dcc-132">NOTES</span></span>

## <span data-ttu-id="e7dcc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7dcc-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7dcc-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e7dcc-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e7dcc-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="e7dcc-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="e7dcc-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="e7dcc-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


