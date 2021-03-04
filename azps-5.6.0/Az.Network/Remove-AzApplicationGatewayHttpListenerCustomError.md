---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: fabe88c2b7606bac3d5a90011913a2beae513f09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889629"
---
# <span data-ttu-id="14eae-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14eae-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="14eae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14eae-102">SYNOPSIS</span></span>
<span data-ttu-id="14eae-103">Remove um erro personalizado de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14eae-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="14eae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14eae-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14eae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14eae-105">DESCRIPTION</span></span>
<span data-ttu-id="14eae-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14eae-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="14eae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14eae-107">EXAMPLES</span></span>

### <span data-ttu-id="14eae-108">Exemplo 1: remove o erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="14eae-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="14eae-109">Este comando remove o erro personalizado do código de status http 502 do ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="14eae-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="14eae-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14eae-110">PARAMETERS</span></span>

### <span data-ttu-id="14eae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eae-111">-DefaultProfile</span></span>
<span data-ttu-id="14eae-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14eae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14eae-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="14eae-113">-HttpListener</span></span>
<span data-ttu-id="14eae-114">O Ouvinte Http do Gateway de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="14eae-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="14eae-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="14eae-115">-StatusCode</span></span>
<span data-ttu-id="14eae-116">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14eae-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="14eae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eae-117">CommonParameters</span></span>
<span data-ttu-id="14eae-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14eae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eae-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14eae-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eae-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14eae-120">INPUTS</span></span>

### <span data-ttu-id="14eae-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14eae-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="14eae-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14eae-122">OUTPUTS</span></span>

### <span data-ttu-id="14eae-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14eae-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14eae-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="14eae-124">NOTES</span></span>

## <span data-ttu-id="14eae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14eae-125">RELATED LINKS</span></span>

[<span data-ttu-id="14eae-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14eae-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="14eae-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14eae-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="14eae-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14eae-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
