---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: bf202a971497a9c43f7ed3731b7c53bc12e58d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427657"
---
# <span data-ttu-id="ad100-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ad100-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="ad100-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad100-102">SYNOPSIS</span></span>
<span data-ttu-id="ad100-103">Obtém o status de disponibilidade do ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ad100-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad100-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad100-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad100-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad100-105">DESCRIPTION</span></span>
<span data-ttu-id="ad100-106">O cmdlet **Get-AzureRmCdnEndpointNameAvailability** Obtém o status de disponibilidade do ponto de extremidade da rede de distribuição de conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad100-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ad100-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad100-107">EXAMPLES</span></span>

## <span data-ttu-id="ad100-108">OS</span><span class="sxs-lookup"><span data-stu-id="ad100-108">PARAMETERS</span></span>

### <span data-ttu-id="ad100-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad100-109">-DefaultProfile</span></span>
<span data-ttu-id="ad100-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ad100-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad100-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ad100-111">-EndpointName</span></span>
<span data-ttu-id="ad100-112">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ad100-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad100-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad100-113">CommonParameters</span></span>
<span data-ttu-id="ad100-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad100-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad100-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad100-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad100-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad100-116">INPUTS</span></span>

### <span data-ttu-id="ad100-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ad100-117">None</span></span>
<span data-ttu-id="ad100-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ad100-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad100-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad100-119">OUTPUTS</span></span>

### <span data-ttu-id="ad100-120">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="ad100-120">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="ad100-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad100-121">NOTES</span></span>

## <span data-ttu-id="ad100-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad100-122">RELATED LINKS</span></span>

