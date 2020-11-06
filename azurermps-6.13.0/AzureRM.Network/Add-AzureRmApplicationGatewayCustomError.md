---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428085"
---
# <span data-ttu-id="0563c-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0563c-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0563c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0563c-102">SYNOPSIS</span></span>
<span data-ttu-id="0563c-103">Adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0563c-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0563c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0563c-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0563c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0563c-105">DESCRIPTION</span></span>
<span data-ttu-id="0563c-106">O cmdlet **Add-AzureRmApplicationGatewayCustomError** adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0563c-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="0563c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0563c-107">EXAMPLES</span></span>

### <span data-ttu-id="0563c-108">Exemplo 1: Adiciona um erro personalizado ao nível de gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="0563c-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="0563c-109">Esse comando adiciona um erro personalizado de código de status http 502 ao gateway do aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="0563c-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="0563c-110">OS</span><span class="sxs-lookup"><span data-stu-id="0563c-110">PARAMETERS</span></span>

### <span data-ttu-id="0563c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0563c-111">-ApplicationGateway</span></span>
<span data-ttu-id="0563c-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0563c-112">The Application Gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0563c-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="0563c-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="0563c-114">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0563c-114">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0563c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0563c-115">-DefaultProfile</span></span>
<span data-ttu-id="0563c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0563c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0563c-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0563c-117">-StatusCode</span></span>
<span data-ttu-id="0563c-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="0563c-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0563c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0563c-119">CommonParameters</span></span>
<span data-ttu-id="0563c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0563c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0563c-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0563c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0563c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0563c-122">INPUTS</span></span>

### <span data-ttu-id="0563c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0563c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0563c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0563c-124">OUTPUTS</span></span>

### <span data-ttu-id="0563c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0563c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0563c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0563c-126">NOTES</span></span>

## <span data-ttu-id="0563c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0563c-127">RELATED LINKS</span></span>
