---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440578"
---
# <span data-ttu-id="2558d-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2558d-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="2558d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2558d-102">SYNOPSIS</span></span>
<span data-ttu-id="2558d-103">Obtenha os itens protegidos em um contêiner de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="2558d-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2558d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2558d-104">SYNTAX</span></span>

### <span data-ttu-id="2558d-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="2558d-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="2558d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2558d-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="2558d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2558d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="2558d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2558d-108">DESCRIPTION</span></span>
<span data-ttu-id="2558d-109">O cmdlet **Get-AzureRmRecoveryServicesAsrProtectableItem** Obtém os itens que protegem em um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2558d-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="2558d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2558d-110">EXAMPLES</span></span>

### <span data-ttu-id="2558d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2558d-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="2558d-112">Obtém todos os itens que protegem no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="2558d-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="2558d-113">OS</span><span class="sxs-lookup"><span data-stu-id="2558d-113">PARAMETERS</span></span>

### <span data-ttu-id="2558d-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2558d-114">-FriendlyName</span></span>
<span data-ttu-id="2558d-115">Especifica o nome amigável do item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="2558d-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="2558d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2558d-116">-Name</span></span>
<span data-ttu-id="2558d-117">Especifica o nome do item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="2558d-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="2558d-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2558d-118">-ProtectionContainer</span></span>
<span data-ttu-id="2558d-119">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2558d-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2558d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2558d-120">CommonParameters</span></span>
<span data-ttu-id="2558d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2558d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2558d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2558d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2558d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2558d-123">INPUTS</span></span>

### <span data-ttu-id="2558d-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2558d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2558d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2558d-125">OUTPUTS</span></span>

### <span data-ttu-id="2558d-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2558d-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2558d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2558d-127">NOTES</span></span>

## <span data-ttu-id="2558d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2558d-128">RELATED LINKS</span></span>

[<span data-ttu-id="2558d-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2558d-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="2558d-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2558d-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
