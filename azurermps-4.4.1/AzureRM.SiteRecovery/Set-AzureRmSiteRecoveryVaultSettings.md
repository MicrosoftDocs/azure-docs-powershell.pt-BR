---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432537"
---
# <span data-ttu-id="33449-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="33449-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="33449-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33449-102">SYNOPSIS</span></span>
<span data-ttu-id="33449-103">Define o contexto do cofre de recuperação do site para outras operações.</span><span class="sxs-lookup"><span data-stu-id="33449-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33449-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33449-104">SYNTAX</span></span>

### <span data-ttu-id="33449-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="33449-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33449-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="33449-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33449-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33449-107">DESCRIPTION</span></span>
<span data-ttu-id="33449-108">O cmdlet **set-AzureRmSiteRecoveryVaultSettings** define o contexto do cofre do Azure site Recovery para outras operações.</span><span class="sxs-lookup"><span data-stu-id="33449-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="33449-109">Isso não se aplica a cofres de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="33449-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="33449-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33449-110">EXAMPLES</span></span>

## <span data-ttu-id="33449-111">OS</span><span class="sxs-lookup"><span data-stu-id="33449-111">PARAMETERS</span></span>

### <span data-ttu-id="33449-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="33449-112">-ARSVault</span></span>
<span data-ttu-id="33449-113">Especifica um objeto **ARSVault** .</span><span class="sxs-lookup"><span data-stu-id="33449-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33449-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="33449-114">-ASRVault</span></span>
<span data-ttu-id="33449-115">Especifica um objeto **ASRVault** .</span><span class="sxs-lookup"><span data-stu-id="33449-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33449-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33449-116">-DefaultProfile</span></span>
<span data-ttu-id="33449-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33449-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33449-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33449-118">CommonParameters</span></span>
<span data-ttu-id="33449-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33449-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33449-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33449-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33449-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33449-121">INPUTS</span></span>

### <span data-ttu-id="33449-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="33449-122">ARSVault</span></span>
<span data-ttu-id="33449-123">O parâmetro ' ARSVault ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="33449-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="33449-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="33449-124">ASRVault</span></span>
<span data-ttu-id="33449-125">O parâmetro ' ASRVault ' aceita o valor do tipo ' ASRVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="33449-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="33449-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33449-126">OUTPUTS</span></span>

### <span data-ttu-id="33449-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="33449-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="33449-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33449-128">NOTES</span></span>

## <span data-ttu-id="33449-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33449-129">RELATED LINKS</span></span>

[<span data-ttu-id="33449-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="33449-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
