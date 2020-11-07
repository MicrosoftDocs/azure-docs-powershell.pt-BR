---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771841"
---
# <span data-ttu-id="4d30a-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4d30a-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="4d30a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d30a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d30a-103">Adiciona um erro personalizado a um ouvinte HTTP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="4d30a-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="4d30a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d30a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d30a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d30a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d30a-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d30a-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="4d30a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d30a-107">EXAMPLES</span></span>

### <span data-ttu-id="4d30a-108">Exemplo 1: Adiciona um erro personalizado ao nível do ouvinte http</span><span class="sxs-lookup"><span data-stu-id="4d30a-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="4d30a-109">Esse comando adiciona um erro personalizado de código de status http 502 ao ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="4d30a-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="4d30a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4d30a-110">PARAMETERS</span></span>

### <span data-ttu-id="4d30a-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="4d30a-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="4d30a-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d30a-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4d30a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d30a-113">-DefaultProfile</span></span>
<span data-ttu-id="4d30a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d30a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d30a-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="4d30a-115">-HttpListener</span></span>
<span data-ttu-id="4d30a-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4d30a-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="4d30a-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4d30a-117">-StatusCode</span></span>
<span data-ttu-id="4d30a-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="4d30a-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4d30a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d30a-119">CommonParameters</span></span>
<span data-ttu-id="4d30a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d30a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d30a-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d30a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d30a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d30a-122">INPUTS</span></span>

### <span data-ttu-id="4d30a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4d30a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4d30a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d30a-124">OUTPUTS</span></span>

### <span data-ttu-id="4d30a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4d30a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4d30a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d30a-126">NOTES</span></span>

## <span data-ttu-id="4d30a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d30a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d30a-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4d30a-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4d30a-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4d30a-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4d30a-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4d30a-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)