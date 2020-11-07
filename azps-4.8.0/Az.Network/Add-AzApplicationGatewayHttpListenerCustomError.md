---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947722"
---
# <span data-ttu-id="f7f06-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f7f06-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f7f06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7f06-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f06-103">Adiciona um erro personalizado a um ouvinte HTTP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="f7f06-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f7f06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7f06-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7f06-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f06-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7f06-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f7f06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7f06-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f06-108">Exemplo 1: Adiciona um erro personalizado ao nível do ouvinte http</span><span class="sxs-lookup"><span data-stu-id="f7f06-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f7f06-109">Esse comando adiciona um erro personalizado de código de status http 502 ao ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="f7f06-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f7f06-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7f06-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f06-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f7f06-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f7f06-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7f06-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f7f06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f06-113">-DefaultProfile</span></span>
<span data-ttu-id="f7f06-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f06-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f7f06-115">-HttpListener</span></span>
<span data-ttu-id="f7f06-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f7f06-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f06-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f7f06-117">-StatusCode</span></span>
<span data-ttu-id="f7f06-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="f7f06-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f7f06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f06-119">CommonParameters</span></span>
<span data-ttu-id="f7f06-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f06-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f06-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f06-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7f06-122">INPUTS</span></span>

### <span data-ttu-id="f7f06-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f7f06-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f7f06-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7f06-124">OUTPUTS</span></span>

### <span data-ttu-id="f7f06-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f7f06-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f7f06-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7f06-126">NOTES</span></span>

## <span data-ttu-id="f7f06-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7f06-127">RELATED LINKS</span></span>

[<span data-ttu-id="f7f06-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f7f06-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f7f06-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f7f06-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f7f06-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f7f06-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
