---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114123"
---
# <span data-ttu-id="75e98-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="75e98-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="75e98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75e98-102">SYNOPSIS</span></span>
<span data-ttu-id="75e98-103">Remove um erro personalizado de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75e98-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="75e98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75e98-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75e98-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="75e98-105">DESCRIPTION</span></span>
<span data-ttu-id="75e98-106">O cmdlet **Remove-AzApplicationGatewayCustomError** remove um erro personalizado de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75e98-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="75e98-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75e98-107">EXAMPLES</span></span>

### <span data-ttu-id="75e98-108">Exemplo 1: remove o erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="75e98-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="75e98-109">Esse comando remove o erro personalizado do código de status http 502 do ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="75e98-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="75e98-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75e98-110">PARAMETERS</span></span>

### <span data-ttu-id="75e98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e98-111">-DefaultProfile</span></span>
<span data-ttu-id="75e98-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75e98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e98-113">-httpListener</span><span class="sxs-lookup"><span data-stu-id="75e98-113">-HttpListener</span></span>
<span data-ttu-id="75e98-114">O gateway de aplicativo http ouvinte</span><span class="sxs-lookup"><span data-stu-id="75e98-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="75e98-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="75e98-115">-StatusCode</span></span>
<span data-ttu-id="75e98-116">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75e98-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="75e98-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e98-117">CommonParameters</span></span>
<span data-ttu-id="75e98-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e98-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e98-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e98-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e98-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="75e98-120">INPUTS</span></span>

### <span data-ttu-id="75e98-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="75e98-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="75e98-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="75e98-122">OUTPUTS</span></span>

### <span data-ttu-id="75e98-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="75e98-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="75e98-124">Notas</span><span class="sxs-lookup"><span data-stu-id="75e98-124">NOTES</span></span>

## <span data-ttu-id="75e98-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75e98-125">RELATED LINKS</span></span>

[<span data-ttu-id="75e98-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="75e98-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="75e98-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="75e98-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="75e98-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="75e98-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
