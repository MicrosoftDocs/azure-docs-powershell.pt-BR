---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 8e2b563563ca50e0fdf6913a9e9999e1a642ff9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610161"
---
# <span data-ttu-id="527fe-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="527fe-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="527fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="527fe-102">SYNOPSIS</span></span>
<span data-ttu-id="527fe-103">Obtém classificações de armazenamento na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="527fe-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="527fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="527fe-104">SYNTAX</span></span>

### <span data-ttu-id="527fe-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="527fe-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527fe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="527fe-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="527fe-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="527fe-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="527fe-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="527fe-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="527fe-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="527fe-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="527fe-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="527fe-110">DESCRIPTION</span></span>
<span data-ttu-id="527fe-111">O cmdlet **Get-AzureRmSiteRecoveryStorageClassification** tem classificações de armazenamento no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="527fe-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="527fe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="527fe-112">EXAMPLES</span></span>

## <span data-ttu-id="527fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="527fe-113">PARAMETERS</span></span>

### <span data-ttu-id="527fe-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="527fe-114">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="527fe-115">-FriendlyName</span></span>
<span data-ttu-id="527fe-116">Especifica o nome amigável da classificação de armazenamento que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="527fe-116">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="527fe-117">-Name</span></span>
<span data-ttu-id="527fe-118">Especifica o nome da classificação de armazenamento que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="527fe-118">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-119">-Servidor</span><span class="sxs-lookup"><span data-stu-id="527fe-119">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527fe-120">-DefaultProfile</span></span>
<span data-ttu-id="527fe-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="527fe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527fe-122">CommonParameters</span></span>
<span data-ttu-id="527fe-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527fe-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527fe-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="527fe-125">INPUTS</span></span>

### <span data-ttu-id="527fe-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="527fe-126">ASRFabric</span></span>
<span data-ttu-id="527fe-127">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="527fe-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="527fe-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="527fe-128">ASRServer</span></span>
<span data-ttu-id="527fe-129">O parâmetro ' Server ' aceita o valor do tipo ' ASRServer ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="527fe-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="527fe-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="527fe-130">OUTPUTS</span></span>

### <span data-ttu-id="527fe-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="527fe-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="527fe-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="527fe-132">NOTES</span></span>

## <span data-ttu-id="527fe-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="527fe-133">RELATED LINKS</span></span>

