---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433405"
---
# <span data-ttu-id="d9cb2-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d9cb2-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="d9cb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cb2-103">Obtenha os itens protegidos em um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9cb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9cb2-104">SYNTAX</span></span>

### <span data-ttu-id="d9cb2-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9cb2-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cb2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d9cb2-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cb2-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d9cb2-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9cb2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9cb2-108">DESCRIPTION</span></span>
<span data-ttu-id="d9cb2-109">O cmdlet **Get-AzureRmSiteRecoveryProtectableItem** Obtém os itens que protegem em um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d9cb2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9cb2-110">EXAMPLES</span></span>

## <span data-ttu-id="d9cb2-111">OS</span><span class="sxs-lookup"><span data-stu-id="d9cb2-111">PARAMETERS</span></span>

### <span data-ttu-id="d9cb2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cb2-112">-DefaultProfile</span></span>
<span data-ttu-id="d9cb2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9cb2-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d9cb2-114">-FriendlyName</span></span>
<span data-ttu-id="d9cb2-115">Especifica o nome amigável do item que protege o Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="d9cb2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9cb2-116">-Name</span></span>
<span data-ttu-id="d9cb2-117">Especifica o nome do item que protege o Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="d9cb2-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d9cb2-118">-ProtectionContainer</span></span>
<span data-ttu-id="d9cb2-119">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d9cb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cb2-120">CommonParameters</span></span>
<span data-ttu-id="d9cb2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cb2-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9cb2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cb2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9cb2-123">INPUTS</span></span>

### <span data-ttu-id="d9cb2-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d9cb2-124">ASRProtectionContainer</span></span>
<span data-ttu-id="d9cb2-125">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d9cb2-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="d9cb2-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9cb2-126">OUTPUTS</span></span>

### <span data-ttu-id="d9cb2-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d9cb2-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d9cb2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9cb2-128">NOTES</span></span>

## <span data-ttu-id="d9cb2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9cb2-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9cb2-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d9cb2-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="d9cb2-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d9cb2-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
