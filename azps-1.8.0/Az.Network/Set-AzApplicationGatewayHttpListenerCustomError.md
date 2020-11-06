---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cf8d7453961796afb4b0aa94d549d80eb9279ab5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600052"
---
# <span data-ttu-id="f1dac-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f1dac-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f1dac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1dac-102">SYNOPSIS</span></span>
<span data-ttu-id="f1dac-103">Atualiza um erro personalizado em um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1dac-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f1dac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1dac-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1dac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1dac-105">DESCRIPTION</span></span>
<span data-ttu-id="f1dac-106">O cmdlet **set-AzApplicationGatewayCustomError** atualiza um erro personalizado em um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1dac-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="f1dac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1dac-107">EXAMPLES</span></span>

### <span data-ttu-id="f1dac-108">Exemplo 1: atualiza um erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="f1dac-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f1dac-109">Esse comando atualiza o erro personalizado do código de status http 502 no ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="f1dac-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="f1dac-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1dac-110">PARAMETERS</span></span>

### <span data-ttu-id="f1dac-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f1dac-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f1dac-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1dac-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f1dac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1dac-113">-DefaultProfile</span></span>
<span data-ttu-id="f1dac-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1dac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1dac-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f1dac-115">-HttpListener</span></span>
<span data-ttu-id="f1dac-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f1dac-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f1dac-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1dac-117">-StatusCode</span></span>
<span data-ttu-id="f1dac-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="f1dac-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f1dac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1dac-119">CommonParameters</span></span>
<span data-ttu-id="f1dac-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1dac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1dac-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1dac-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1dac-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1dac-122">INPUTS</span></span>

### <span data-ttu-id="f1dac-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f1dac-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f1dac-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1dac-124">OUTPUTS</span></span>

### <span data-ttu-id="f1dac-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1dac-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f1dac-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1dac-126">NOTES</span></span>

## <span data-ttu-id="f1dac-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1dac-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1dac-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f1dac-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f1dac-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f1dac-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f1dac-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f1dac-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
