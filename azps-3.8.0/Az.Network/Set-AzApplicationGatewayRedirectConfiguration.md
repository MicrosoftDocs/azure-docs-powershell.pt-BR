---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: da6acfddcee30861b73145d7d8e66871de02568d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941348"
---
# <span data-ttu-id="7afac-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afac-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7afac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7afac-102">SYNOPSIS</span></span>
<span data-ttu-id="7afac-103">Define a configuração de redirecionamento em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="7afac-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="7afac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7afac-104">SYNTAX</span></span>

### <span data-ttu-id="7afac-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7afac-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7afac-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7afac-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7afac-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="7afac-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7afac-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7afac-108">DESCRIPTION</span></span>
<span data-ttu-id="7afac-109">**O cmdlet Set-AzApplicationGatewayRequestRoutingRule** modifica uma configuração de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="7afac-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="7afac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7afac-110">EXAMPLES</span></span>

### <span data-ttu-id="7afac-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7afac-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="7afac-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7afac-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7afac-113">O segundo comando modifica a configuração de redirecionamento para que o gateway do aplicativo redirecione o tipo permanente e use uma URL de destino.</span><span class="sxs-lookup"><span data-stu-id="7afac-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="7afac-114">OS</span><span class="sxs-lookup"><span data-stu-id="7afac-114">PARAMETERS</span></span>

### <span data-ttu-id="7afac-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7afac-115">-ApplicationGateway</span></span>
<span data-ttu-id="7afac-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7afac-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7afac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afac-117">-DefaultProfile</span></span>
<span data-ttu-id="7afac-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7afac-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7afac-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="7afac-119">-IncludePath</span></span>
<span data-ttu-id="7afac-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="7afac-120">Include path in the redirected url.</span></span>
<span data-ttu-id="7afac-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7afac-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="7afac-122">-IncludeQueryString</span></span>
<span data-ttu-id="7afac-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="7afac-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="7afac-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7afac-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7afac-125">-Name</span></span>
<span data-ttu-id="7afac-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="7afac-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="7afac-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="7afac-127">-RedirectType</span></span>
<span data-ttu-id="7afac-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="7afac-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="7afac-129">-TargetListener</span></span>
<span data-ttu-id="7afac-130">Escuta HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="7afac-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="7afac-131">-TargetListenerID</span></span>
<span data-ttu-id="7afac-132">ID do ouvinte HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="7afac-132">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="7afac-133">-TargetUrl</span></span>
<span data-ttu-id="7afac-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="7afac-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afac-135">CommonParameters</span></span>
<span data-ttu-id="7afac-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7afac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afac-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7afac-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afac-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7afac-138">INPUTS</span></span>

### <span data-ttu-id="7afac-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7afac-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7afac-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7afac-140">OUTPUTS</span></span>

### <span data-ttu-id="7afac-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7afac-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7afac-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7afac-142">NOTES</span></span>

## <span data-ttu-id="7afac-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7afac-143">RELATED LINKS</span></span>

[<span data-ttu-id="7afac-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afac-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7afac-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afac-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7afac-146">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afac-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7afac-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7afac-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
