---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: c851e075c4963477d8b8f6b18440780735c74f32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786076"
---
# <span data-ttu-id="bcef0-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcef0-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bcef0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcef0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcef0-103">Define a configuração de redirecionamento em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="bcef0-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcef0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcef0-104">SYNTAX</span></span>

### <span data-ttu-id="bcef0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcef0-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcef0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bcef0-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcef0-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="bcef0-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcef0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcef0-108">DESCRIPTION</span></span>
<span data-ttu-id="bcef0-109">**O cmdlet Set-AzureRmApplicationGatewayRequestRoutingRule** modifica uma configuração de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="bcef0-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="bcef0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcef0-110">EXAMPLES</span></span>

### <span data-ttu-id="bcef0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bcef0-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="bcef0-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bcef0-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bcef0-113">O segundo comando modifica a configuração de redirecionamento para que o gateway do aplicativo redirecione o tipo permanente e use uma URL de destino.</span><span class="sxs-lookup"><span data-stu-id="bcef0-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="bcef0-114">OS</span><span class="sxs-lookup"><span data-stu-id="bcef0-114">PARAMETERS</span></span>

### <span data-ttu-id="bcef0-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcef0-115">-ApplicationGateway</span></span>
<span data-ttu-id="bcef0-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcef0-116">The applicationGateway</span></span>

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

### <span data-ttu-id="bcef0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcef0-117">-DefaultProfile</span></span>
<span data-ttu-id="bcef0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcef0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcef0-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="bcef0-119">-IncludePath</span></span>
<span data-ttu-id="bcef0-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="bcef0-120">Include path in the redirected url.</span></span>
<span data-ttu-id="bcef0-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="bcef0-121">Default is true.</span></span>

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

### <span data-ttu-id="bcef0-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="bcef0-122">-IncludeQueryString</span></span>
<span data-ttu-id="bcef0-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="bcef0-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="bcef0-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="bcef0-124">Default is true.</span></span>

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

### <span data-ttu-id="bcef0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcef0-125">-Name</span></span>
<span data-ttu-id="bcef0-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="bcef0-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="bcef0-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="bcef0-127">-RedirectType</span></span>
<span data-ttu-id="bcef0-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="bcef0-128">The type of redirect</span></span>

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

### <span data-ttu-id="bcef0-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="bcef0-129">-TargetListener</span></span>
<span data-ttu-id="bcef0-130">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="bcef0-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="bcef0-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="bcef0-131">-TargetListenerID</span></span>
<span data-ttu-id="bcef0-132">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="bcef0-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="bcef0-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="bcef0-133">-TargetUrl</span></span>
<span data-ttu-id="bcef0-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="bcef0-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="bcef0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcef0-135">CommonParameters</span></span>
<span data-ttu-id="bcef0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcef0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcef0-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcef0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcef0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcef0-138">INPUTS</span></span>

### <span data-ttu-id="bcef0-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcef0-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bcef0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcef0-140">OUTPUTS</span></span>

### <span data-ttu-id="bcef0-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcef0-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bcef0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcef0-142">NOTES</span></span>

## <span data-ttu-id="bcef0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcef0-143">RELATED LINKS</span></span>

