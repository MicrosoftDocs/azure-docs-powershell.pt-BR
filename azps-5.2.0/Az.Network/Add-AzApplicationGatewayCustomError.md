---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257583"
---
# <span data-ttu-id="25202-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="25202-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25202-102">SYNOPSIS</span></span>
<span data-ttu-id="25202-103">Adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="25202-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="25202-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25202-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25202-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25202-105">DESCRIPTION</span></span>
<span data-ttu-id="25202-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="25202-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="25202-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25202-107">EXAMPLES</span></span>

### <span data-ttu-id="25202-108">Exemplo 1: Adiciona um erro personalizado ao nível de gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="25202-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="25202-109">Esse comando adiciona um erro personalizado de código de status http 502 ao gateway do aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="25202-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="25202-110">Exemplo 2: Adiciona um erro personalizado ao nível do ouvinte do aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="25202-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="25202-111">Esse comando adiciona um erro personalizado de código de status http 502 ao gateway do aplicativo $appgw no nível do ouvinte e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="25202-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="25202-112">OS</span><span class="sxs-lookup"><span data-stu-id="25202-112">PARAMETERS</span></span>

### <span data-ttu-id="25202-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25202-113">-ApplicationGateway</span></span>
<span data-ttu-id="25202-114">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="25202-114">The Application Gateway</span></span>

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

### <span data-ttu-id="25202-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="25202-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="25202-116">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="25202-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="25202-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25202-117">-DefaultProfile</span></span>
<span data-ttu-id="25202-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25202-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25202-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="25202-119">-StatusCode</span></span>
<span data-ttu-id="25202-120">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="25202-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="25202-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25202-121">CommonParameters</span></span>
<span data-ttu-id="25202-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25202-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25202-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25202-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25202-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25202-124">INPUTS</span></span>

### <span data-ttu-id="25202-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25202-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25202-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25202-126">OUTPUTS</span></span>

### <span data-ttu-id="25202-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="25202-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25202-128">NOTES</span></span>

## <span data-ttu-id="25202-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25202-129">RELATED LINKS</span></span>

[<span data-ttu-id="25202-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="25202-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="25202-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="25202-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="25202-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
