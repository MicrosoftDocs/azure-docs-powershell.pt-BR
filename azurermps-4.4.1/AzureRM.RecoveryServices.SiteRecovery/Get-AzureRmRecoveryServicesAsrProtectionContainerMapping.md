---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440575"
---
# <span data-ttu-id="29c61-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="29c61-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="29c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29c61-102">SYNOPSIS</span></span>
<span data-ttu-id="29c61-103">Obtém mapeamentos de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="29c61-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29c61-104">SYNTAX</span></span>

### <span data-ttu-id="29c61-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="29c61-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="29c61-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="29c61-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="29c61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29c61-107">DESCRIPTION</span></span>
<span data-ttu-id="29c61-108">O cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política de replicação (Associação) no cofre para o contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="29c61-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="29c61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29c61-109">EXAMPLES</span></span>

### <span data-ttu-id="29c61-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29c61-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="29c61-111">Obtém todos os mapeamentos de contêiner de proteção para o contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="29c61-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="29c61-112">OS</span><span class="sxs-lookup"><span data-stu-id="29c61-112">PARAMETERS</span></span>

### <span data-ttu-id="29c61-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="29c61-113">-Name</span></span>
<span data-ttu-id="29c61-114">Especifica o nome do mapeamento de contêiner de proteção a obter.</span><span class="sxs-lookup"><span data-stu-id="29c61-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="29c61-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="29c61-115">-ProtectionContainer</span></span>
<span data-ttu-id="29c61-116">Obter mapeamentos de contêiner de proteção correspondentes ao objeto contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="29c61-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="29c61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c61-117">CommonParameters</span></span>
<span data-ttu-id="29c61-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c61-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c61-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29c61-120">INPUTS</span></span>

### <span data-ttu-id="29c61-121">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="29c61-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="29c61-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29c61-122">OUTPUTS</span></span>

### <span data-ttu-id="29c61-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29c61-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="29c61-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29c61-124">NOTES</span></span>

## <span data-ttu-id="29c61-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29c61-125">RELATED LINKS</span></span>

[<span data-ttu-id="29c61-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="29c61-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="29c61-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="29c61-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)