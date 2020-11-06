---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c92c3c6b66e1b1208c7a0425b27a7e966bf6689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600221"
---
# <span data-ttu-id="bef09-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bef09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bef09-102">SYNOPSIS</span></span>
<span data-ttu-id="bef09-103">Remove um erro personalizado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bef09-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="bef09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bef09-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef09-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bef09-105">DESCRIPTION</span></span>
<span data-ttu-id="bef09-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bef09-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="bef09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bef09-107">EXAMPLES</span></span>

### <span data-ttu-id="bef09-108">Exemplo 1: Remove o erro personalizado de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="bef09-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="bef09-109">Esse comando Remove o erro personalizado do código de status http 502 da $appgw do gateway do aplicativo e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="bef09-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="bef09-110">OS</span><span class="sxs-lookup"><span data-stu-id="bef09-110">PARAMETERS</span></span>

### <span data-ttu-id="bef09-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bef09-111">-ApplicationGateway</span></span>
<span data-ttu-id="bef09-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="bef09-112">The Application Gateway</span></span>

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

### <span data-ttu-id="bef09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef09-113">-DefaultProfile</span></span>
<span data-ttu-id="bef09-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bef09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef09-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bef09-115">-StatusCode</span></span>
<span data-ttu-id="bef09-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="bef09-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bef09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef09-117">CommonParameters</span></span>
<span data-ttu-id="bef09-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef09-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef09-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef09-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bef09-120">INPUTS</span></span>

### <span data-ttu-id="bef09-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bef09-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bef09-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bef09-122">OUTPUTS</span></span>

### <span data-ttu-id="bef09-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bef09-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bef09-124">NOTES</span></span>

## <span data-ttu-id="bef09-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bef09-125">RELATED LINKS</span></span>

[<span data-ttu-id="bef09-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bef09-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bef09-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bef09-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bef09-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
