---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: f5c36cc9e6133fbde4e7bae34b4bc6b479afb96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887385"
---
# <span data-ttu-id="16ed4-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="16ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="16ed4-103">Adiciona um erro personalizado a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16ed4-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="16ed4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="16ed4-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ed4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="16ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="16ed4-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16ed4-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="16ed4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16ed4-107">EXAMPLES</span></span>

### <span data-ttu-id="16ed4-108">Exemplo 1: adiciona erro personalizado ao nível do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="16ed4-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="16ed4-109">Este comando adiciona um erro personalizado do código de status http 502 ao gateway de aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="16ed4-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="16ed4-110">Exemplo 2: adiciona erro personalizado ao nível de ouvinte do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="16ed4-110">Example 2: Adds custom error to application gateway listener level</span></span>
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

<span data-ttu-id="16ed4-111">Este comando adiciona um erro personalizado do código de status http 502 ao gateway de aplicativo $appgw no nível do ouvinte e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="16ed4-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="16ed4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="16ed4-112">PARAMETERS</span></span>

### <span data-ttu-id="16ed4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16ed4-113">-ApplicationGateway</span></span>
<span data-ttu-id="16ed4-114">O Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="16ed4-114">The Application Gateway</span></span>

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

### <span data-ttu-id="16ed4-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="16ed4-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="16ed4-116">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16ed4-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="16ed4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ed4-117">-DefaultProfile</span></span>
<span data-ttu-id="16ed4-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16ed4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ed4-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="16ed4-119">-StatusCode</span></span>
<span data-ttu-id="16ed4-120">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16ed4-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="16ed4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ed4-121">CommonParameters</span></span>
<span data-ttu-id="16ed4-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ed4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ed4-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ed4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ed4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16ed4-124">INPUTS</span></span>

### <span data-ttu-id="16ed4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16ed4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16ed4-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="16ed4-126">OUTPUTS</span></span>

### <span data-ttu-id="16ed4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="16ed4-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="16ed4-128">NOTES</span></span>

## <span data-ttu-id="16ed4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16ed4-129">RELATED LINKS</span></span>

[<span data-ttu-id="16ed4-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="16ed4-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="16ed4-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="16ed4-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16ed4-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
