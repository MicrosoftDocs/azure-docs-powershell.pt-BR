---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440976"
---
# <span data-ttu-id="c690f-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c690f-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c690f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c690f-102">SYNOPSIS</span></span>
<span data-ttu-id="c690f-103">Obtém as propriedades de itens protegidos de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c690f-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c690f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c690f-104">SYNTAX</span></span>

### <span data-ttu-id="c690f-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c690f-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="c690f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c690f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="c690f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c690f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="c690f-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="c690f-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="c690f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c690f-109">DESCRIPTION</span></span>
<span data-ttu-id="c690f-110">O cmdlet **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** Obtém as propriedades de todos ou o item protegido de replicação ASR especificado do contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="c690f-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="c690f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c690f-111">EXAMPLES</span></span>

### <span data-ttu-id="c690f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c690f-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="c690f-113">Lista todos os itens protegidos de replicação no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="c690f-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="c690f-114">OS</span><span class="sxs-lookup"><span data-stu-id="c690f-114">PARAMETERS</span></span>

### <span data-ttu-id="c690f-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c690f-115">-FriendlyName</span></span>
<span data-ttu-id="c690f-116">Especifica o nome amigável do item protegido de replicação a obter.</span><span class="sxs-lookup"><span data-stu-id="c690f-116">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c690f-117">-Name</span></span>
<span data-ttu-id="c690f-118">Especifica o nome do item protegido da replicação a obter.</span><span class="sxs-lookup"><span data-stu-id="c690f-118">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c690f-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c690f-119">-ProtectableItem</span></span>
<span data-ttu-id="c690f-120">Especifica um objeto de item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="c690f-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="c690f-121">O cmdlet obtém o item protegido de replicação ASR correspondente ao item protegido ASR especificado, se o item estiver protegido.</span><span class="sxs-lookup"><span data-stu-id="c690f-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c690f-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c690f-122">-ProtectionContainer</span></span>
<span data-ttu-id="c690f-123">Especifica o objeto de contêiner de proteção ASR do contêiner de proteção ASR correspondente ao item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="c690f-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c690f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690f-124">CommonParameters</span></span>
<span data-ttu-id="c690f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c690f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c690f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c690f-127">INPUTS</span></span>

### <span data-ttu-id="c690f-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c690f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="c690f-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c690f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c690f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c690f-130">OUTPUTS</span></span>

### <span data-ttu-id="c690f-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c690f-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c690f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c690f-132">NOTES</span></span>

## <span data-ttu-id="c690f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c690f-133">RELATED LINKS</span></span>

[<span data-ttu-id="c690f-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c690f-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c690f-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c690f-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c690f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c690f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
