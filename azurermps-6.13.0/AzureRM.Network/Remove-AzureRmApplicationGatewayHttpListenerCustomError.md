---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428058"
---
# <span data-ttu-id="7ab9a-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7ab9a-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7ab9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ab9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab9a-103">Remove um erro personalizado de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ab9a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ab9a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab9a-106">O cmdlet **Remove-AzureRmApplicationGatewayCustomError** remove um erro personalizado de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7ab9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ab9a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab9a-108">Exemplo 1: Remove o erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="7ab9a-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="7ab9a-109">Esse comando Remove o erro personalizado do código de status http 502 do ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="7ab9a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7ab9a-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab9a-111">-DefaultProfile</span></span>
<span data-ttu-id="7ab9a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab9a-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7ab9a-113">-HttpListener</span></span>
<span data-ttu-id="7ab9a-114">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7ab9a-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="7ab9a-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7ab9a-115">-StatusCode</span></span>
<span data-ttu-id="7ab9a-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7ab9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab9a-117">CommonParameters</span></span>
<span data-ttu-id="7ab9a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ab9a-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab9a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ab9a-120">INPUTS</span></span>

### <span data-ttu-id="7ab9a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7ab9a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7ab9a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ab9a-122">OUTPUTS</span></span>

### <span data-ttu-id="7ab9a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7ab9a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7ab9a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ab9a-124">NOTES</span></span>

## <span data-ttu-id="7ab9a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ab9a-125">RELATED LINKS</span></span>
