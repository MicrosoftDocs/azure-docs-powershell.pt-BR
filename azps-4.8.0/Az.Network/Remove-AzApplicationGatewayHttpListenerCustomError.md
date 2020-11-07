---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955394"
---
# <span data-ttu-id="1f1eb-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1f1eb-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1f1eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1eb-103">Remove um erro personalizado de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1f1eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f1eb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f1eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="1f1eb-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1f1eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="1f1eb-108">Exemplo 1: Remove o erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="1f1eb-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="1f1eb-109">Esse comando Remove o erro personalizado do código de status http 502 do ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="1f1eb-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f1eb-110">PARAMETERS</span></span>

### <span data-ttu-id="1f1eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1eb-111">-DefaultProfile</span></span>
<span data-ttu-id="1f1eb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f1eb-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1f1eb-113">-HttpListener</span></span>
<span data-ttu-id="1f1eb-114">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1f1eb-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1f1eb-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1f1eb-115">-StatusCode</span></span>
<span data-ttu-id="1f1eb-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1f1eb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1eb-117">CommonParameters</span></span>
<span data-ttu-id="1f1eb-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f1eb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1eb-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1eb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1eb-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f1eb-120">INPUTS</span></span>

### <span data-ttu-id="1f1eb-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1f1eb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1f1eb-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f1eb-122">OUTPUTS</span></span>

### <span data-ttu-id="1f1eb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1f1eb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1f1eb-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f1eb-124">NOTES</span></span>

## <span data-ttu-id="1f1eb-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f1eb-125">RELATED LINKS</span></span>

[<span data-ttu-id="1f1eb-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1f1eb-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1f1eb-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1f1eb-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1f1eb-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1f1eb-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
