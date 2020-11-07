---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 6db510e79d2c1796cf62a1fd00e55e7860164af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772114"
---
# <span data-ttu-id="51287-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51287-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="51287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51287-102">SYNOPSIS</span></span>
<span data-ttu-id="51287-103">Adiciona uma configuração de redirecionamento a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51287-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="51287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51287-104">SYNTAX</span></span>

### <span data-ttu-id="51287-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51287-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51287-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51287-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51287-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="51287-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51287-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51287-108">DESCRIPTION</span></span>
<span data-ttu-id="51287-109">O cmdlet **Add-AzApplicationGatewayRedirectConfiguration** adiciona uma configuração de redirecionamento a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51287-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="51287-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51287-110">EXAMPLES</span></span>

### <span data-ttu-id="51287-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51287-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="51287-112">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="51287-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="51287-113">O segundo comando adiciona a configuração de redirecionamento ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51287-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="51287-114">OS</span><span class="sxs-lookup"><span data-stu-id="51287-114">PARAMETERS</span></span>

### <span data-ttu-id="51287-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51287-115">-ApplicationGateway</span></span>
<span data-ttu-id="51287-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="51287-116">The applicationGateway</span></span>

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

### <span data-ttu-id="51287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51287-117">-DefaultProfile</span></span>
<span data-ttu-id="51287-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51287-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51287-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="51287-119">-IncludePath</span></span>
<span data-ttu-id="51287-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="51287-120">Include path in the redirected url.</span></span>
<span data-ttu-id="51287-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="51287-121">Default is true.</span></span>

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

### <span data-ttu-id="51287-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="51287-122">-IncludeQueryString</span></span>
<span data-ttu-id="51287-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="51287-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="51287-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="51287-124">Default is true.</span></span>

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

### <span data-ttu-id="51287-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="51287-125">-Name</span></span>
<span data-ttu-id="51287-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="51287-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="51287-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="51287-127">-RedirectType</span></span>
<span data-ttu-id="51287-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="51287-128">The type of redirect</span></span>

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

### <span data-ttu-id="51287-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="51287-129">-TargetListener</span></span>
<span data-ttu-id="51287-130">Escuta HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="51287-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="51287-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="51287-131">-TargetListenerID</span></span>
<span data-ttu-id="51287-132">ID do ouvinte HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="51287-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="51287-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="51287-133">-TargetUrl</span></span>
<span data-ttu-id="51287-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="51287-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="51287-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51287-135">CommonParameters</span></span>
<span data-ttu-id="51287-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51287-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51287-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51287-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51287-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51287-138">INPUTS</span></span>

### <span data-ttu-id="51287-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51287-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51287-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51287-140">OUTPUTS</span></span>

### <span data-ttu-id="51287-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51287-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51287-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51287-142">NOTES</span></span>

## <span data-ttu-id="51287-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51287-143">RELATED LINKS</span></span>

[<span data-ttu-id="51287-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51287-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="51287-145">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51287-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="51287-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51287-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="51287-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51287-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
