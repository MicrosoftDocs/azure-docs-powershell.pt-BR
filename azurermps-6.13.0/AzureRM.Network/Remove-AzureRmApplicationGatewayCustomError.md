---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428062"
---
# <span data-ttu-id="691a7-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="691a7-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="691a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="691a7-102">SYNOPSIS</span></span>
<span data-ttu-id="691a7-103">Remove um erro personalizado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="691a7-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="691a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="691a7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="691a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="691a7-105">DESCRIPTION</span></span>
<span data-ttu-id="691a7-106">O cmdlet **Remove-AzureRmApplicationGatewayCustomError** remove um erro personalizado de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="691a7-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="691a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="691a7-107">EXAMPLES</span></span>

### <span data-ttu-id="691a7-108">Exemplo 1: Remove o erro personalizado de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="691a7-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="691a7-109">Esse comando Remove o erro personalizado do código de status http 502 da $appgw do gateway do aplicativo e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="691a7-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="691a7-110">OS</span><span class="sxs-lookup"><span data-stu-id="691a7-110">PARAMETERS</span></span>

### <span data-ttu-id="691a7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="691a7-111">-ApplicationGateway</span></span>
<span data-ttu-id="691a7-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="691a7-112">The Application Gateway</span></span>

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

### <span data-ttu-id="691a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691a7-113">-DefaultProfile</span></span>
<span data-ttu-id="691a7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="691a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="691a7-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="691a7-115">-StatusCode</span></span>
<span data-ttu-id="691a7-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="691a7-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="691a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691a7-117">CommonParameters</span></span>
<span data-ttu-id="691a7-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691a7-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691a7-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="691a7-120">INPUTS</span></span>

### <span data-ttu-id="691a7-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="691a7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="691a7-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="691a7-122">OUTPUTS</span></span>

### <span data-ttu-id="691a7-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="691a7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="691a7-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="691a7-124">NOTES</span></span>

## <span data-ttu-id="691a7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="691a7-125">RELATED LINKS</span></span>
