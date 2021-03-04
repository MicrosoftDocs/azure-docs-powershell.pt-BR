---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 990c9624d949fa695b815a9530125a90693816ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885406"
---
# <span data-ttu-id="9624f-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9624f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9624f-102">SYNOPSIS</span></span>
<span data-ttu-id="9624f-103">Remove um erro personalizado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9624f-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="9624f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9624f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9624f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9624f-105">DESCRIPTION</span></span>
<span data-ttu-id="9624f-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9624f-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="9624f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9624f-107">EXAMPLES</span></span>

### <span data-ttu-id="9624f-108">Exemplo 1: remove o erro personalizado de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9624f-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="9624f-109">Este comando remove o erro personalizado do código de status http 502 do gateway de aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="9624f-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="9624f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9624f-110">PARAMETERS</span></span>

### <span data-ttu-id="9624f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9624f-111">-ApplicationGateway</span></span>
<span data-ttu-id="9624f-112">O Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="9624f-112">The Application Gateway</span></span>

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

### <span data-ttu-id="9624f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9624f-113">-DefaultProfile</span></span>
<span data-ttu-id="9624f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9624f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9624f-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9624f-115">-StatusCode</span></span>
<span data-ttu-id="9624f-116">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9624f-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9624f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9624f-117">CommonParameters</span></span>
<span data-ttu-id="9624f-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9624f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9624f-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9624f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9624f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9624f-120">INPUTS</span></span>

### <span data-ttu-id="9624f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9624f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9624f-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9624f-122">OUTPUTS</span></span>

### <span data-ttu-id="9624f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9624f-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="9624f-124">NOTES</span></span>

## <span data-ttu-id="9624f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9624f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9624f-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9624f-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9624f-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9624f-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9624f-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
