---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433403"
---
# <span data-ttu-id="ce205-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ce205-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="ce205-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce205-102">SYNOPSIS</span></span>
<span data-ttu-id="ce205-103">Obtém mapeamentos de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ce205-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce205-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce205-104">SYNTAX</span></span>

### <span data-ttu-id="ce205-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce205-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce205-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ce205-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce205-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce205-107">DESCRIPTION</span></span>
<span data-ttu-id="ce205-108">O cmdlet **Get-AzureRmSiteRecoveryProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política no cofre.</span><span class="sxs-lookup"><span data-stu-id="ce205-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="ce205-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce205-109">EXAMPLES</span></span>

## <span data-ttu-id="ce205-110">OS</span><span class="sxs-lookup"><span data-stu-id="ce205-110">PARAMETERS</span></span>

### <span data-ttu-id="ce205-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce205-111">-DefaultProfile</span></span>
<span data-ttu-id="ce205-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce205-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce205-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce205-113">-Name</span></span>
<span data-ttu-id="ce205-114">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="ce205-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="ce205-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ce205-115">-ProtectionContainer</span></span>
<span data-ttu-id="ce205-116">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ce205-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="ce205-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce205-117">CommonParameters</span></span>
<span data-ttu-id="ce205-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce205-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce205-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce205-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce205-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce205-120">INPUTS</span></span>

### <span data-ttu-id="ce205-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ce205-121">ASRProtectionContainer</span></span>
<span data-ttu-id="ce205-122">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ce205-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="ce205-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce205-123">OUTPUTS</span></span>

### <span data-ttu-id="ce205-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ce205-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ce205-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce205-125">NOTES</span></span>

## <span data-ttu-id="ce205-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce205-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce205-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ce205-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="ce205-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ce205-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
