---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440573"
---
# <span data-ttu-id="89923-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="89923-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="89923-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89923-102">SYNOPSIS</span></span>
<span data-ttu-id="89923-103">Obtém as classificações de armazenamento ASR disponíveis (detectadas) no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="89923-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89923-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89923-104">SYNTAX</span></span>

### <span data-ttu-id="89923-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="89923-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="89923-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="89923-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="89923-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="89923-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="89923-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89923-108">DESCRIPTION</span></span>
<span data-ttu-id="89923-109">O cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassification** Obtém detalhes das classificações de armazenamento ASR descobertos no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="89923-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="89923-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89923-110">EXAMPLES</span></span>

### <span data-ttu-id="89923-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89923-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="89923-112">Listar as classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="89923-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="89923-113">OS</span><span class="sxs-lookup"><span data-stu-id="89923-113">PARAMETERS</span></span>

### <span data-ttu-id="89923-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="89923-114">-Fabric</span></span>
<span data-ttu-id="89923-115">Especifica um objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="89923-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="89923-116">O cmdlet obtém os detalhes das classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="89923-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="89923-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="89923-117">-FriendlyName</span></span>
<span data-ttu-id="89923-118">Especifica o nome amigável do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="89923-118">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="89923-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="89923-119">-Name</span></span>
<span data-ttu-id="89923-120">Especifica o nome do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="89923-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="89923-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89923-121">CommonParameters</span></span>
<span data-ttu-id="89923-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89923-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89923-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89923-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89923-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89923-124">INPUTS</span></span>

### <span data-ttu-id="89923-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="89923-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="89923-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89923-126">OUTPUTS</span></span>

### <span data-ttu-id="89923-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89923-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89923-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89923-128">NOTES</span></span>

## <span data-ttu-id="89923-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89923-129">RELATED LINKS</span></span>

