---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601964"
---
# <span data-ttu-id="db3f0-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="db3f0-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="db3f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="db3f0-103">Atualiza um erro personalizado em um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db3f0-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db3f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db3f0-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db3f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db3f0-105">DESCRIPTION</span></span>
<span data-ttu-id="db3f0-106">O cmdlet **set-AzureRmApplicationGatewayCustomError** atualiza um erro personalizado em um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db3f0-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="db3f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db3f0-107">EXAMPLES</span></span>

### <span data-ttu-id="db3f0-108">Exemplo 1: atualiza um erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="db3f0-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="db3f0-109">Esse comando atualiza o erro personalizado do código de status http 502 no ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="db3f0-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="db3f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="db3f0-110">PARAMETERS</span></span>

### <span data-ttu-id="db3f0-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="db3f0-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="db3f0-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db3f0-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="db3f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3f0-113">-DefaultProfile</span></span>
<span data-ttu-id="db3f0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db3f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3f0-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="db3f0-115">-HttpListener</span></span>
<span data-ttu-id="db3f0-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="db3f0-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db3f0-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="db3f0-117">-StatusCode</span></span>
<span data-ttu-id="db3f0-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="db3f0-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="db3f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3f0-119">CommonParameters</span></span>
<span data-ttu-id="db3f0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="db3f0-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3f0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db3f0-122">INPUTS</span></span>

### <span data-ttu-id="db3f0-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db3f0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="db3f0-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db3f0-124">OUTPUTS</span></span>

### <span data-ttu-id="db3f0-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db3f0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="db3f0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db3f0-126">NOTES</span></span>

## <span data-ttu-id="db3f0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db3f0-127">RELATED LINKS</span></span>
