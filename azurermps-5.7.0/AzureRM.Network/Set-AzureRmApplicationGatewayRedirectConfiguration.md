---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 9a37bd3769fa7078e0d215b2d6c2452c4fc64bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611043"
---
# <span data-ttu-id="b9ffb-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9ffb-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b9ffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ffb-103">Define a configuração de redirecionamento em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9ffb-104">SYNTAX</span></span>

### <span data-ttu-id="b9ffb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ffb-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ffb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b9ffb-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ffb-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b9ffb-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9ffb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9ffb-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ffb-109">**O cmdlet Set-AzureRmApplicationGatewayRequestRoutingRule** modifica uma configuração de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="b9ffb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9ffb-110">EXAMPLES</span></span>

### <span data-ttu-id="b9ffb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9ffb-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="b9ffb-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b9ffb-113">O segundo comando modifica a configuração de redirecionamento para que o gateway do aplicativo redirecione o tipo permanente e use uma URL de destino.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="b9ffb-114">OS</span><span class="sxs-lookup"><span data-stu-id="b9ffb-114">PARAMETERS</span></span>

### <span data-ttu-id="b9ffb-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ffb-115">-ApplicationGateway</span></span>
<span data-ttu-id="b9ffb-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ffb-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ffb-117">-DefaultProfile</span></span>
<span data-ttu-id="b9ffb-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b9ffb-119">-IncludePath</span></span>
<span data-ttu-id="b9ffb-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-120">Include path in the redirected url.</span></span>
<span data-ttu-id="b9ffb-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b9ffb-122">-IncludeQueryString</span></span>
<span data-ttu-id="b9ffb-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="b9ffb-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9ffb-125">-Name</span></span>
<span data-ttu-id="b9ffb-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b9ffb-126">The name of the Redirect Configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="b9ffb-127">-RedirectType</span></span>
<span data-ttu-id="b9ffb-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b9ffb-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b9ffb-129">-TargetListener</span></span>
<span data-ttu-id="b9ffb-130">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="b9ffb-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b9ffb-131">-TargetListenerID</span></span>
<span data-ttu-id="b9ffb-132">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="b9ffb-132">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b9ffb-133">-TargetUrl</span></span>
<span data-ttu-id="b9ffb-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b9ffb-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ffb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ffb-135">CommonParameters</span></span>
<span data-ttu-id="b9ffb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ffb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ffb-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ffb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ffb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9ffb-138">INPUTS</span></span>

### <span data-ttu-id="b9ffb-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ffb-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9ffb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9ffb-140">OUTPUTS</span></span>

### <span data-ttu-id="b9ffb-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ffb-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9ffb-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9ffb-142">NOTES</span></span>

## <span data-ttu-id="b9ffb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ffb-143">RELATED LINKS</span></span>

