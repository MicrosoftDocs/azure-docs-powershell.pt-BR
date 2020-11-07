---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946569"
---
# <span data-ttu-id="13b3c-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="13b3c-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="13b3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="13b3c-103">Obtém informações sobre máquinas virtuais gerenciadas por site Recovery.</span><span class="sxs-lookup"><span data-stu-id="13b3c-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="13b3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13b3c-104">SYNTAX</span></span>

### <span data-ttu-id="13b3c-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="13b3c-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13b3c-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="13b3c-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13b3c-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="13b3c-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13b3c-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="13b3c-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13b3c-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="13b3c-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="13b3c-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="13b3c-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13b3c-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13b3c-111">DESCRIPTION</span></span>
<span data-ttu-id="13b3c-112">O cmdlet **Get-AzureSiteRecoveryVM** Obtém informações sobre máquinas virtuais gerenciadas no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="13b3c-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="13b3c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13b3c-113">EXAMPLES</span></span>

### <span data-ttu-id="13b3c-114">Exemplo 1: obter informações sobre uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="13b3c-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="13b3c-115">O primeiro comando usa o cmdlet **Get-AzureSiteRecoveryProtectionContainer** para obter um contêiner protegido e, em seguida, armazena-o na variável $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="13b3c-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="13b3c-116">O segundo comando obtém informações sobre as máquinas virtuais em $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="13b3c-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="13b3c-117">OS</span><span class="sxs-lookup"><span data-stu-id="13b3c-117">PARAMETERS</span></span>

### <span data-ttu-id="13b3c-118">-ID</span><span class="sxs-lookup"><span data-stu-id="13b3c-118">-Id</span></span>
<span data-ttu-id="13b3c-119">Especifica a ID da máquina virtual sobre a qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="13b3c-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="13b3c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="13b3c-120">-Name</span></span>
<span data-ttu-id="13b3c-121">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13b3c-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="13b3c-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="13b3c-122">-Profile</span></span>
<span data-ttu-id="13b3c-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="13b3c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13b3c-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="13b3c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13b3c-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="13b3c-125">-ProtectionContainer</span></span>
<span data-ttu-id="13b3c-126">Especifica o objeto contêiner da proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="13b3c-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="13b3c-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="13b3c-127">-ProtectionContainerId</span></span>
<span data-ttu-id="13b3c-128">Especifica a ID de um contêiner protegido sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="13b3c-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="13b3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b3c-129">CommonParameters</span></span>
<span data-ttu-id="13b3c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b3c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b3c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b3c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13b3c-132">INPUTS</span></span>

## <span data-ttu-id="13b3c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13b3c-133">OUTPUTS</span></span>

## <span data-ttu-id="13b3c-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13b3c-134">NOTES</span></span>

## <span data-ttu-id="13b3c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13b3c-135">RELATED LINKS</span></span>

[<span data-ttu-id="13b3c-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="13b3c-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


