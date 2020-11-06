---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433397"
---
# <span data-ttu-id="fc824-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="fc824-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="fc824-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc824-102">SYNOPSIS</span></span>
<span data-ttu-id="fc824-103">Obtém classificações de armazenamento na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="fc824-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc824-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc824-104">SYNTAX</span></span>

### <span data-ttu-id="fc824-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc824-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc824-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fc824-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc824-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fc824-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc824-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="fc824-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc824-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="fc824-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc824-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc824-110">DESCRIPTION</span></span>
<span data-ttu-id="fc824-111">O cmdlet **Get-AzureRmSiteRecoveryStorageClassification** tem classificações de armazenamento no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fc824-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="fc824-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc824-112">EXAMPLES</span></span>

## <span data-ttu-id="fc824-113">OS</span><span class="sxs-lookup"><span data-stu-id="fc824-113">PARAMETERS</span></span>

### <span data-ttu-id="fc824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc824-114">-DefaultProfile</span></span>
<span data-ttu-id="fc824-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc824-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc824-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="fc824-116">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc824-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fc824-117">-FriendlyName</span></span>
<span data-ttu-id="fc824-118">Especifica o nome amigável da classificação de armazenamento que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fc824-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fc824-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc824-119">-Name</span></span>
<span data-ttu-id="fc824-120">Especifica o nome da classificação de armazenamento que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fc824-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fc824-121">-Servidor</span><span class="sxs-lookup"><span data-stu-id="fc824-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc824-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc824-122">CommonParameters</span></span>
<span data-ttu-id="fc824-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc824-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc824-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc824-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc824-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc824-125">INPUTS</span></span>

### <span data-ttu-id="fc824-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fc824-126">ASRFabric</span></span>
<span data-ttu-id="fc824-127">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="fc824-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="fc824-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="fc824-128">ASRServer</span></span>
<span data-ttu-id="fc824-129">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="fc824-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="fc824-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc824-130">OUTPUTS</span></span>

### <span data-ttu-id="fc824-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="fc824-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="fc824-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc824-132">NOTES</span></span>

## <span data-ttu-id="fc824-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc824-133">RELATED LINKS</span></span>

