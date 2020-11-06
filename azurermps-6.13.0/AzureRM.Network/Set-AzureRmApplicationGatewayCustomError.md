---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430128"
---
# <span data-ttu-id="93b00-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="93b00-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="93b00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93b00-102">SYNOPSIS</span></span>
<span data-ttu-id="93b00-103">Atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93b00-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93b00-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b00-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93b00-105">DESCRIPTION</span></span>
<span data-ttu-id="93b00-106">O cmdlet **set-AzureRmApplicationGatewayCustomError** atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93b00-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="93b00-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93b00-107">EXAMPLES</span></span>

### <span data-ttu-id="93b00-108">Exemplo 1: atualiza o erro personalizado em um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="93b00-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="93b00-109">Esse comando atualiza o erro personalizado do código de status http 502 na $appgw do gateway do aplicativo e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="93b00-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="93b00-110">OS</span><span class="sxs-lookup"><span data-stu-id="93b00-110">PARAMETERS</span></span>

### <span data-ttu-id="93b00-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93b00-111">-ApplicationGateway</span></span>
<span data-ttu-id="93b00-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="93b00-112">The Application Gateway</span></span>

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

### <span data-ttu-id="93b00-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="93b00-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="93b00-114">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93b00-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="93b00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b00-115">-DefaultProfile</span></span>
<span data-ttu-id="93b00-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93b00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93b00-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="93b00-117">-StatusCode</span></span>
<span data-ttu-id="93b00-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="93b00-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="93b00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b00-119">CommonParameters</span></span>
<span data-ttu-id="93b00-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b00-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b00-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b00-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93b00-122">INPUTS</span></span>

### <span data-ttu-id="93b00-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93b00-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93b00-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93b00-124">OUTPUTS</span></span>

### <span data-ttu-id="93b00-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93b00-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93b00-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93b00-126">NOTES</span></span>

## <span data-ttu-id="93b00-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93b00-127">RELATED LINKS</span></span>
