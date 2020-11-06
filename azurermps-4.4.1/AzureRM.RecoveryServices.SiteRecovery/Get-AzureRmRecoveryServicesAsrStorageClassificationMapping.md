---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609601"
---
# <span data-ttu-id="1ed05-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1ed05-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="1ed05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ed05-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed05-103">Obtém mapeamentos de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="1ed05-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ed05-104">SYNTAX</span></span>

### <span data-ttu-id="1ed05-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ed05-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="1ed05-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1ed05-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="1ed05-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ed05-107">DESCRIPTION</span></span>
<span data-ttu-id="1ed05-108">O cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** Obtém os detalhes de um mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="1ed05-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="1ed05-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ed05-109">EXAMPLES</span></span>

### <span data-ttu-id="1ed05-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ed05-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="1ed05-111">Listar todos os mapeamentos de classificação de armazenamento correspondentes à classificação de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="1ed05-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="1ed05-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ed05-112">PARAMETERS</span></span>

### <span data-ttu-id="1ed05-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ed05-113">-Name</span></span>
<span data-ttu-id="1ed05-114">Especifica o nome do mapeamento de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="1ed05-114">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="1ed05-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="1ed05-115">-StorageClassification</span></span>
<span data-ttu-id="1ed05-116">Especifica um objeto de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="1ed05-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="1ed05-117">O cmdlet obtém mapeamentos de classificação de armazenamento ASR correspondentes à classificação de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="1ed05-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed05-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed05-118">CommonParameters</span></span>
<span data-ttu-id="1ed05-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed05-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed05-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed05-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed05-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ed05-121">INPUTS</span></span>

### <span data-ttu-id="1ed05-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ed05-122">None</span></span>

## <span data-ttu-id="1ed05-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ed05-123">OUTPUTS</span></span>

### <span data-ttu-id="1ed05-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1ed05-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1ed05-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ed05-125">NOTES</span></span>

## <span data-ttu-id="1ed05-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ed05-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ed05-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1ed05-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="1ed05-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1ed05-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
