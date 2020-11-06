---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609602"
---
# <span data-ttu-id="66514-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="66514-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="66514-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66514-102">SYNOPSIS</span></span>
<span data-ttu-id="66514-103">Obtém os detalhes dos provedores de serviços de recuperação ASR registrados no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="66514-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66514-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66514-104">SYNTAX</span></span>

### <span data-ttu-id="66514-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="66514-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="66514-106">ByName</span><span class="sxs-lookup"><span data-stu-id="66514-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="66514-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="66514-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="66514-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66514-108">DESCRIPTION</span></span>
<span data-ttu-id="66514-109">O cmdlet **Get-AzureRmRecoveryServicesAsrServicesProvider** Obtém informações sobre os provedores do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="66514-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="66514-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66514-110">EXAMPLES</span></span>

### <span data-ttu-id="66514-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66514-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="66514-112">Liste todos os provedores de serviços de replicação ASR registrados no cofre de serviços de recuperação correspondente à malha especificada.</span><span class="sxs-lookup"><span data-stu-id="66514-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="66514-113">OS</span><span class="sxs-lookup"><span data-stu-id="66514-113">PARAMETERS</span></span>

### <span data-ttu-id="66514-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="66514-114">-Fabric</span></span>
<span data-ttu-id="66514-115">Especifica o objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="66514-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="66514-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="66514-116">-FriendlyName</span></span>
<span data-ttu-id="66514-117">Especifica o nome amigável do provedor de serviços de recuperação ASR para o qual obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="66514-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66514-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="66514-118">-Name</span></span>
<span data-ttu-id="66514-119">Especifica o nome do provedor de serviços de recuperação ASR para o qual obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="66514-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66514-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66514-120">CommonParameters</span></span>
<span data-ttu-id="66514-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66514-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66514-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66514-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66514-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66514-123">INPUTS</span></span>

### <span data-ttu-id="66514-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="66514-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="66514-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66514-125">OUTPUTS</span></span>

### <span data-ttu-id="66514-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="66514-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="66514-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66514-127">NOTES</span></span>

## <span data-ttu-id="66514-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66514-128">RELATED LINKS</span></span>

[<span data-ttu-id="66514-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="66514-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="66514-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="66514-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
