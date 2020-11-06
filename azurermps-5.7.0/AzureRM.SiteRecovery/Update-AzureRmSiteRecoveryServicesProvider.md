---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432394"
---
# <span data-ttu-id="3b937-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3b937-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="3b937-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b937-102">SYNOPSIS</span></span>
<span data-ttu-id="3b937-103">Atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b937-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b937-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b937-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b937-105">DESCRIPTION</span></span>
<span data-ttu-id="3b937-106">O cmdlet **Update-AzureRmSiteRecoveryServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b937-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="3b937-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3b937-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="3b937-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b937-108">EXAMPLES</span></span>

## <span data-ttu-id="3b937-109">OS</span><span class="sxs-lookup"><span data-stu-id="3b937-109">PARAMETERS</span></span>

### <span data-ttu-id="3b937-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b937-110">-DefaultProfile</span></span>
<span data-ttu-id="3b937-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b937-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b937-112">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="3b937-112">-ServicesProvider</span></span>
<span data-ttu-id="3b937-113">Especifica o objeto do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b937-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b937-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b937-114">CommonParameters</span></span>
<span data-ttu-id="3b937-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b937-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b937-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b937-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b937-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b937-117">INPUTS</span></span>

### <span data-ttu-id="3b937-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3b937-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="3b937-119">O parâmetro ' Servicesprovider ' aceita o valor do tipo ' ASRRecoveryServicesProvider ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="3b937-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="3b937-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b937-120">OUTPUTS</span></span>

## <span data-ttu-id="3b937-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b937-121">NOTES</span></span>

## <span data-ttu-id="3b937-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b937-122">RELATED LINKS</span></span>

[<span data-ttu-id="3b937-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3b937-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="3b937-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3b937-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
