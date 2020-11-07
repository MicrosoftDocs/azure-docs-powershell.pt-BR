---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943552"
---
# <span data-ttu-id="43942-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="43942-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="43942-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43942-102">SYNOPSIS</span></span>
<span data-ttu-id="43942-103">Obtém erro (s) personalizado (s) de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43942-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="43942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43942-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43942-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43942-105">DESCRIPTION</span></span>
<span data-ttu-id="43942-106">O cmdlet **Get-AzApplicationGatewayCustomError** Obtém erro (s) personalizado (s) de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43942-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="43942-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43942-107">EXAMPLES</span></span>

### <span data-ttu-id="43942-108">Exemplo 1: Obtém um erro personalizado em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="43942-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="43942-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="43942-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="43942-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="43942-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="43942-111">Esse comando obtém e retorna a lista de todos os erros personalizados do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="43942-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="43942-112">OS</span><span class="sxs-lookup"><span data-stu-id="43942-112">PARAMETERS</span></span>

### <span data-ttu-id="43942-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43942-113">-DefaultProfile</span></span>
<span data-ttu-id="43942-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43942-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43942-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="43942-115">-HttpListener</span></span>
<span data-ttu-id="43942-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="43942-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="43942-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="43942-117">-StatusCode</span></span>
<span data-ttu-id="43942-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="43942-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43942-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43942-119">CommonParameters</span></span>
<span data-ttu-id="43942-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43942-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43942-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43942-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43942-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43942-122">INPUTS</span></span>

### <span data-ttu-id="43942-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="43942-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="43942-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43942-124">OUTPUTS</span></span>

### <span data-ttu-id="43942-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="43942-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="43942-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43942-126">NOTES</span></span>

## <span data-ttu-id="43942-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43942-127">RELATED LINKS</span></span>

[<span data-ttu-id="43942-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="43942-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="43942-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="43942-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="43942-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="43942-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
