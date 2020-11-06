---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433381"
---
# <span data-ttu-id="5b296-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5b296-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="5b296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b296-102">SYNOPSIS</span></span>
<span data-ttu-id="5b296-103">Remove um mapeamento de rede do cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="5b296-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b296-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b296-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b296-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b296-105">DESCRIPTION</span></span>
<span data-ttu-id="5b296-106">O cmdlet **Remove-AzureRMSiteRecoveryNetworkMapping** remove um mapeamento de rede do cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="5b296-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5b296-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b296-107">EXAMPLES</span></span>

## <span data-ttu-id="5b296-108">OS</span><span class="sxs-lookup"><span data-stu-id="5b296-108">PARAMETERS</span></span>

### <span data-ttu-id="5b296-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b296-109">-DefaultProfile</span></span>
<span data-ttu-id="5b296-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b296-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b296-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5b296-111">-NetworkMapping</span></span>
<span data-ttu-id="5b296-112">Especifica o objeto de mapeamento de rede.</span><span class="sxs-lookup"><span data-stu-id="5b296-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b296-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b296-113">CommonParameters</span></span>
<span data-ttu-id="5b296-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b296-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b296-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b296-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b296-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b296-116">INPUTS</span></span>

### <span data-ttu-id="5b296-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5b296-117">ASRNetworkMapping</span></span>
<span data-ttu-id="5b296-118">O parâmetro ' NetworkMapping ' aceita o valor do tipo ' ASRNetworkMapping ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5b296-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="5b296-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b296-119">OUTPUTS</span></span>

### <span data-ttu-id="5b296-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5b296-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5b296-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b296-121">NOTES</span></span>

## <span data-ttu-id="5b296-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b296-122">RELATED LINKS</span></span>

[<span data-ttu-id="5b296-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5b296-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="5b296-124">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5b296-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
