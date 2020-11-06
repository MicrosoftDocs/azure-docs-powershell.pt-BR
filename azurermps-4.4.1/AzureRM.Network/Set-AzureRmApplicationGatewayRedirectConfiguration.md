---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602700"
---
# <span data-ttu-id="b1abc-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1abc-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b1abc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1abc-102">SYNOPSIS</span></span>
<span data-ttu-id="b1abc-103">Define a configuração de redirecionamento em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="b1abc-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1abc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1abc-104">SYNTAX</span></span>

### <span data-ttu-id="b1abc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1abc-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1abc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b1abc-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1abc-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b1abc-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1abc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1abc-108">DESCRIPTION</span></span>
<span data-ttu-id="b1abc-109">**O cmdlet Set-AzureRmApplicationGatewayRequestRoutingRule** modifica uma configuração de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="b1abc-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="b1abc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1abc-110">EXAMPLES</span></span>

### <span data-ttu-id="b1abc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1abc-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="b1abc-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b1abc-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b1abc-113">O segundo comando modifica a configuração de redirecionamento para que o gateway do aplicativo redirecione o tipo permanente e use uma URL de destino.</span><span class="sxs-lookup"><span data-stu-id="b1abc-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="b1abc-114">OS</span><span class="sxs-lookup"><span data-stu-id="b1abc-114">PARAMETERS</span></span>

### <span data-ttu-id="b1abc-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1abc-115">-ApplicationGateway</span></span>
<span data-ttu-id="b1abc-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1abc-116">The applicationGateway</span></span>

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

### <span data-ttu-id="b1abc-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b1abc-117">-IncludePath</span></span>
<span data-ttu-id="b1abc-118">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="b1abc-118">Include path in the redirected url.</span></span>
<span data-ttu-id="b1abc-119">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b1abc-119">Default is true.</span></span>

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

### <span data-ttu-id="b1abc-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b1abc-120">-IncludeQueryString</span></span>
<span data-ttu-id="b1abc-121">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="b1abc-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="b1abc-122">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b1abc-122">Default is true.</span></span>

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

### <span data-ttu-id="b1abc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1abc-123">-Name</span></span>
<span data-ttu-id="b1abc-124">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b1abc-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="b1abc-125">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="b1abc-125">-RedirectType</span></span>
<span data-ttu-id="b1abc-126">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b1abc-126">The type of redirect</span></span>

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

### <span data-ttu-id="b1abc-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b1abc-127">-TargetListener</span></span>
<span data-ttu-id="b1abc-128">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="b1abc-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="b1abc-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b1abc-129">-TargetListenerID</span></span>
<span data-ttu-id="b1abc-130">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="b1abc-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="b1abc-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b1abc-131">-TargetUrl</span></span>
<span data-ttu-id="b1abc-132">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="b1abc-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="b1abc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1abc-133">-DefaultProfile</span></span>
<span data-ttu-id="b1abc-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1abc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1abc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1abc-135">CommonParameters</span></span>
<span data-ttu-id="b1abc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1abc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1abc-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1abc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1abc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1abc-138">INPUTS</span></span>

### <span data-ttu-id="b1abc-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1abc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1abc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1abc-140">OUTPUTS</span></span>

### <span data-ttu-id="b1abc-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1abc-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1abc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1abc-142">NOTES</span></span>

## <span data-ttu-id="b1abc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1abc-143">RELATED LINKS</span></span>

