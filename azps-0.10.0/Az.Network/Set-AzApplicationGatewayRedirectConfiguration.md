---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 9e9dbd8cef57c4621e009cf0a086616a252eae67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776562"
---
# <span data-ttu-id="76cb6-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="76cb6-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="76cb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="76cb6-103">Define a configuração de redirecionamento em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="76cb6-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="76cb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76cb6-104">SYNTAX</span></span>

### <span data-ttu-id="76cb6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76cb6-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76cb6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="76cb6-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76cb6-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="76cb6-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76cb6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76cb6-108">DESCRIPTION</span></span>
<span data-ttu-id="76cb6-109">**O cmdlet Set-AzApplicationGatewayRequestRoutingRule** modifica uma configuração de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="76cb6-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="76cb6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76cb6-110">EXAMPLES</span></span>

### <span data-ttu-id="76cb6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76cb6-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="76cb6-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="76cb6-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="76cb6-113">O segundo comando modifica a configuração de redirecionamento para que o gateway do aplicativo redirecione o tipo permanente e use uma URL de destino.</span><span class="sxs-lookup"><span data-stu-id="76cb6-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="76cb6-114">OS</span><span class="sxs-lookup"><span data-stu-id="76cb6-114">PARAMETERS</span></span>

### <span data-ttu-id="76cb6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76cb6-115">-ApplicationGateway</span></span>
<span data-ttu-id="76cb6-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="76cb6-116">The applicationGateway</span></span>

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

### <span data-ttu-id="76cb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cb6-117">-DefaultProfile</span></span>
<span data-ttu-id="76cb6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76cb6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cb6-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="76cb6-119">-IncludePath</span></span>
<span data-ttu-id="76cb6-120">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="76cb6-120">Include path in the redirected url.</span></span>
<span data-ttu-id="76cb6-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="76cb6-121">Default is true.</span></span>

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

### <span data-ttu-id="76cb6-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="76cb6-122">-IncludeQueryString</span></span>
<span data-ttu-id="76cb6-123">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="76cb6-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="76cb6-124">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="76cb6-124">Default is true.</span></span>

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

### <span data-ttu-id="76cb6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="76cb6-125">-Name</span></span>
<span data-ttu-id="76cb6-126">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="76cb6-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="76cb6-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="76cb6-127">-RedirectType</span></span>
<span data-ttu-id="76cb6-128">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="76cb6-128">The type of redirect</span></span>

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

### <span data-ttu-id="76cb6-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="76cb6-129">-TargetListener</span></span>
<span data-ttu-id="76cb6-130">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="76cb6-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="76cb6-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="76cb6-131">-TargetListenerID</span></span>
<span data-ttu-id="76cb6-132">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="76cb6-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="76cb6-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="76cb6-133">-TargetUrl</span></span>
<span data-ttu-id="76cb6-134">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="76cb6-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="76cb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cb6-135">CommonParameters</span></span>
<span data-ttu-id="76cb6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cb6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76cb6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cb6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76cb6-138">INPUTS</span></span>

### <span data-ttu-id="76cb6-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76cb6-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76cb6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76cb6-140">OUTPUTS</span></span>

### <span data-ttu-id="76cb6-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76cb6-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76cb6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76cb6-142">NOTES</span></span>

## <span data-ttu-id="76cb6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76cb6-143">RELATED LINKS</span></span>

