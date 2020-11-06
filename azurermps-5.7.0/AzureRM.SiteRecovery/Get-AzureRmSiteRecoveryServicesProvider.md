---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433400"
---
# <span data-ttu-id="7f14c-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f14c-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="7f14c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f14c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f14c-103">Obtém informações sobre os provedores do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="7f14c-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f14c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f14c-104">SYNTAX</span></span>

### <span data-ttu-id="7f14c-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f14c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f14c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7f14c-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f14c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f14c-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f14c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f14c-108">DESCRIPTION</span></span>
<span data-ttu-id="7f14c-109">O cmdlet **Get-AzureRmSiteRecoveryServicesProvider** Obtém informações sobre os provedores do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="7f14c-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="7f14c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f14c-110">EXAMPLES</span></span>

## <span data-ttu-id="7f14c-111">OS</span><span class="sxs-lookup"><span data-stu-id="7f14c-111">PARAMETERS</span></span>

### <span data-ttu-id="7f14c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f14c-112">-DefaultProfile</span></span>
<span data-ttu-id="7f14c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f14c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f14c-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="7f14c-114">-Fabric</span></span>
<span data-ttu-id="7f14c-115">Especifica o objeto da malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7f14c-115">Specifies the Azure Site Recovery Fabric object.</span></span>

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

### <span data-ttu-id="7f14c-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f14c-116">-FriendlyName</span></span>
<span data-ttu-id="7f14c-117">Especifica o nome amigável do provedor de recuperação de site do Azure que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7f14c-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7f14c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f14c-118">-Name</span></span>
<span data-ttu-id="7f14c-119">Especifica o nome do provedor de recuperação do site do Azure que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7f14c-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7f14c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f14c-120">CommonParameters</span></span>
<span data-ttu-id="7f14c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f14c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f14c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f14c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f14c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f14c-123">INPUTS</span></span>

### <span data-ttu-id="7f14c-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7f14c-124">ASRFabric</span></span>
<span data-ttu-id="7f14c-125">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="7f14c-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="7f14c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f14c-126">OUTPUTS</span></span>

### <span data-ttu-id="7f14c-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7f14c-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7f14c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f14c-128">NOTES</span></span>

## <span data-ttu-id="7f14c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f14c-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f14c-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f14c-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="7f14c-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f14c-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
