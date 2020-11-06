---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440978"
---
# <span data-ttu-id="7d337-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d337-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="7d337-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d337-102">SYNOPSIS</span></span>
<span data-ttu-id="7d337-103">Obtém contêineres de proteção ASR no cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7d337-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d337-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d337-104">SYNTAX</span></span>

### <span data-ttu-id="7d337-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d337-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="7d337-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7d337-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="7d337-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d337-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="7d337-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d337-108">DESCRIPTION</span></span>
<span data-ttu-id="7d337-109">O cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainer** Obtém contêineres de proteção do Azure site Recovery no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7d337-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="7d337-110">Um contêiner de proteção é um contêiner lógico para objetos protegidos (detectados) e protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="7d337-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="7d337-111">As políticas de replicação definem as configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="7d337-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="7d337-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d337-112">EXAMPLES</span></span>

### <span data-ttu-id="7d337-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d337-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="7d337-114">Obtém todos os contêineres de proteção ASR na malha ASR especificada (a entrada de pipeline no exemplo acima).</span><span class="sxs-lookup"><span data-stu-id="7d337-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="7d337-115">OS</span><span class="sxs-lookup"><span data-stu-id="7d337-115">PARAMETERS</span></span>

### <span data-ttu-id="7d337-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="7d337-116">-Fabric</span></span>
<span data-ttu-id="7d337-117">Procure o contêiner de proteção na malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="7d337-117">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d337-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7d337-118">-FriendlyName</span></span>
<span data-ttu-id="7d337-119">Especifica o nome amigável do contêiner de proteção ASR a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="7d337-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="7d337-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d337-120">-Name</span></span>
<span data-ttu-id="7d337-121">Especifica o nome do contêiner de proteção ASR a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="7d337-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="7d337-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d337-122">CommonParameters</span></span>
<span data-ttu-id="7d337-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d337-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d337-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d337-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d337-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d337-125">INPUTS</span></span>

### <span data-ttu-id="7d337-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7d337-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7d337-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d337-127">OUTPUTS</span></span>

### <span data-ttu-id="7d337-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7d337-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7d337-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d337-129">NOTES</span></span>

## <span data-ttu-id="7d337-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d337-130">RELATED LINKS</span></span>

