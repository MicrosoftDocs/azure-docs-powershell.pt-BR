---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603246"
---
# <span data-ttu-id="7b9ea-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="7b9ea-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="7b9ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9ea-103">Obtém as classificações de armazenamento ASR disponíveis (detectadas) no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b9ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b9ea-104">SYNTAX</span></span>

### <span data-ttu-id="7b9ea-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b9ea-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9ea-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7b9ea-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9ea-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7b9ea-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9ea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b9ea-108">DESCRIPTION</span></span>
<span data-ttu-id="7b9ea-109">O cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassification** Obtém detalhes das classificações de armazenamento ASR descobertos no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="7b9ea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b9ea-110">EXAMPLES</span></span>

### <span data-ttu-id="7b9ea-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b9ea-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="7b9ea-112">Listar as classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="7b9ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="7b9ea-113">PARAMETERS</span></span>

### <span data-ttu-id="7b9ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9ea-114">-DefaultProfile</span></span>
<span data-ttu-id="7b9ea-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b9ea-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="7b9ea-116">-Fabric</span></span>
<span data-ttu-id="7b9ea-117">Especifica um objeto de malha ASR.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="7b9ea-118">O cmdlet obtém os detalhes das classificações de armazenamento descobertas correspondentes à malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="7b9ea-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7b9ea-119">-FriendlyName</span></span>
<span data-ttu-id="7b9ea-120">Especifica o nome amigável do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="7b9ea-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b9ea-121">-Name</span></span>
<span data-ttu-id="7b9ea-122">Especifica o nome do objeto de classificação de armazenamento a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="7b9ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9ea-123">CommonParameters</span></span>
<span data-ttu-id="7b9ea-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9ea-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9ea-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b9ea-126">INPUTS</span></span>

### <span data-ttu-id="7b9ea-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7b9ea-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7b9ea-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b9ea-128">OUTPUTS</span></span>

### <span data-ttu-id="7b9ea-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7b9ea-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7b9ea-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b9ea-130">NOTES</span></span>

## <span data-ttu-id="7b9ea-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b9ea-131">RELATED LINKS</span></span>
