---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955396"
---
# <span data-ttu-id="89052-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="89052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89052-102">SYNOPSIS</span></span>
<span data-ttu-id="89052-103">Remove um erro personalizado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89052-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="89052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89052-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89052-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89052-105">DESCRIPTION</span></span>
<span data-ttu-id="89052-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="89052-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="89052-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89052-107">EXAMPLES</span></span>

### <span data-ttu-id="89052-108">Exemplo 1: Remove o erro personalizado de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="89052-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="89052-109">Esse comando Remove o erro personalizado do código de status http 502 da $appgw do gateway do aplicativo e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="89052-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="89052-110">OS</span><span class="sxs-lookup"><span data-stu-id="89052-110">PARAMETERS</span></span>

### <span data-ttu-id="89052-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89052-111">-ApplicationGateway</span></span>
<span data-ttu-id="89052-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="89052-112">The Application Gateway</span></span>

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

### <span data-ttu-id="89052-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89052-113">-DefaultProfile</span></span>
<span data-ttu-id="89052-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89052-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89052-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="89052-115">-StatusCode</span></span>
<span data-ttu-id="89052-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="89052-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="89052-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89052-117">CommonParameters</span></span>
<span data-ttu-id="89052-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89052-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89052-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89052-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89052-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89052-120">INPUTS</span></span>

### <span data-ttu-id="89052-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89052-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89052-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89052-122">OUTPUTS</span></span>

### <span data-ttu-id="89052-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="89052-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89052-124">NOTES</span></span>

## <span data-ttu-id="89052-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89052-125">RELATED LINKS</span></span>

[<span data-ttu-id="89052-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="89052-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="89052-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="89052-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="89052-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
