---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bf187375ba625e40c147f7862d9faf4e0706f844
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778230"
---
# <span data-ttu-id="5aebc-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aebc-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5aebc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5aebc-102">SYNOPSIS</span></span>
<span data-ttu-id="5aebc-103">Adiciona uma configuração de redirecionamento a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5aebc-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="5aebc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5aebc-104">SYNTAX</span></span>

### <span data-ttu-id="5aebc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5aebc-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aebc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5aebc-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aebc-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="5aebc-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aebc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5aebc-108">DESCRIPTION</span></span>
<span data-ttu-id="5aebc-109">O cmdlet **Add-AzApplicationGatewayRedirectConfiguration** adiciona uma configuração de redirecionamento a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5aebc-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="5aebc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5aebc-110">EXAMPLES</span></span>

### <span data-ttu-id="5aebc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5aebc-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="5aebc-112">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5aebc-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5aebc-113">O segundo comando adiciona a configuração de redirecionamento ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5aebc-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="5aebc-114">OS</span><span class="sxs-lookup"><span data-stu-id="5aebc-114">PARAMETERS</span></span>

### <span data-ttu-id="5aebc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aebc-115">-ApplicationGateway</span></span>
<span data-ttu-id="5aebc-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aebc-116">The applicationGateway</span></span>

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

### <span data-ttu-id="5aebc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aebc-117">-DefaultProfile</span></span>
<span data-ttu-id="5aebc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5aebc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aebc-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="5aebc-119">-IncludePath</span></span>
<span data-ttu-id="5aebc-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="5aebc-120">Include path in the redirected url.</span></span>
<span data-ttu-id="5aebc-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="5aebc-121">Default is true.</span></span>

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

### <span data-ttu-id="5aebc-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="5aebc-122">-IncludeQueryString</span></span>
<span data-ttu-id="5aebc-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="5aebc-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="5aebc-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="5aebc-124">Default is true.</span></span>

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

### <span data-ttu-id="5aebc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5aebc-125">-Name</span></span>
<span data-ttu-id="5aebc-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="5aebc-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="5aebc-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="5aebc-127">-RedirectType</span></span>
<span data-ttu-id="5aebc-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="5aebc-128">The type of redirect</span></span>

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

### <span data-ttu-id="5aebc-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="5aebc-129">-TargetListener</span></span>
<span data-ttu-id="5aebc-130">Escuta HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="5aebc-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="5aebc-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="5aebc-131">-TargetListenerID</span></span>
<span data-ttu-id="5aebc-132">ID do ouvinte HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="5aebc-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="5aebc-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5aebc-133">-TargetUrl</span></span>
<span data-ttu-id="5aebc-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="5aebc-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="5aebc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aebc-135">CommonParameters</span></span>
<span data-ttu-id="5aebc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aebc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aebc-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aebc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aebc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5aebc-138">INPUTS</span></span>

### <span data-ttu-id="5aebc-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aebc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5aebc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5aebc-140">OUTPUTS</span></span>

### <span data-ttu-id="5aebc-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aebc-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5aebc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5aebc-142">NOTES</span></span>

## <span data-ttu-id="5aebc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5aebc-143">RELATED LINKS</span></span>

[<span data-ttu-id="5aebc-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aebc-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="5aebc-145">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aebc-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="5aebc-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aebc-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="5aebc-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aebc-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
