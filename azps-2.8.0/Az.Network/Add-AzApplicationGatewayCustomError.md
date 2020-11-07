---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 0df6ae98692b7497448b0d3f15e88f1a18a87ae8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771842"
---
# <span data-ttu-id="b705e-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b705e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b705e-102">SYNOPSIS</span></span>
<span data-ttu-id="b705e-103">Adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b705e-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="b705e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b705e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b705e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b705e-105">DESCRIPTION</span></span>
<span data-ttu-id="b705e-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b705e-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="b705e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b705e-107">EXAMPLES</span></span>

### <span data-ttu-id="b705e-108">Exemplo 1: Adiciona um erro personalizado ao nível de gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="b705e-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b705e-109">Esse comando adiciona um erro personalizado de código de status http 502 ao gateway do aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="b705e-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="b705e-110">Exemplo 2: Adiciona um erro personalizado ao nível do ouvinte do aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="b705e-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b705e-111">Esse comando adiciona um erro personalizado de código de status http 502 ao gateway do aplicativo $appgw no nível do ouvinte e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="b705e-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="b705e-112">OS</span><span class="sxs-lookup"><span data-stu-id="b705e-112">PARAMETERS</span></span>

### <span data-ttu-id="b705e-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b705e-113">-ApplicationGateway</span></span>
<span data-ttu-id="b705e-114">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b705e-114">The Application Gateway</span></span>

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

### <span data-ttu-id="b705e-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b705e-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b705e-116">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b705e-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b705e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b705e-117">-DefaultProfile</span></span>
<span data-ttu-id="b705e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b705e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b705e-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b705e-119">-StatusCode</span></span>
<span data-ttu-id="b705e-120">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="b705e-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b705e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b705e-121">CommonParameters</span></span>
<span data-ttu-id="b705e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b705e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b705e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b705e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b705e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b705e-124">INPUTS</span></span>

### <span data-ttu-id="b705e-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b705e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b705e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b705e-126">OUTPUTS</span></span>

### <span data-ttu-id="b705e-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b705e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b705e-128">NOTES</span></span>

## <span data-ttu-id="b705e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b705e-129">RELATED LINKS</span></span>

[<span data-ttu-id="b705e-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b705e-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b705e-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b705e-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b705e-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
