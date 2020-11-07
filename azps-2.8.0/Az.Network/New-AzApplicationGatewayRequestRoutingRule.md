---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 82f14ce9418566793572e2b5722d09460ab1e827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771925"
---
# <span data-ttu-id="af61b-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="af61b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af61b-102">SYNOPSIS</span></span>
<span data-ttu-id="af61b-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="af61b-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="af61b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af61b-104">SYNTAX</span></span>

### <span data-ttu-id="af61b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af61b-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af61b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="af61b-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af61b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af61b-107">DESCRIPTION</span></span>
<span data-ttu-id="af61b-108">**O cmdlet Add-AzApplicationGatewayRequestRoutingRule** cria uma regra de roteamento de solicitação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="af61b-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="af61b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af61b-109">EXAMPLES</span></span>

### <span data-ttu-id="af61b-110">Exemplo 1: criar uma regra de roteamento de solicitação para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="af61b-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="af61b-111">Esse comando cria uma regra básica de roteamento de solicitações chamada Rule01 e armazena o resultado na variável chamada $Rule.</span><span class="sxs-lookup"><span data-stu-id="af61b-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="af61b-112">OS</span><span class="sxs-lookup"><span data-stu-id="af61b-112">PARAMETERS</span></span>

### <span data-ttu-id="af61b-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af61b-113">-BackendAddressPool</span></span>
<span data-ttu-id="af61b-114">Especifica o pool de endereços back-end, como um objeto, para que a regra de roteamento de solicitação crie.</span><span class="sxs-lookup"><span data-stu-id="af61b-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="af61b-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="af61b-116">Especifica a ID do pool de endereços back-end da regra de roteamento de solicitação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="af61b-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="af61b-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="af61b-117">-BackendHttpSettings</span></span>
<span data-ttu-id="af61b-118">Especifica as configurações HTTP de back-end, como um objeto, para que a regra de roteamento de solicitação crie.</span><span class="sxs-lookup"><span data-stu-id="af61b-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="af61b-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="af61b-120">Especifica a ID de configurações HTTP de back-end da regra de roteamento de solicitação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="af61b-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="af61b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af61b-121">-DefaultProfile</span></span>
<span data-ttu-id="af61b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af61b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af61b-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="af61b-123">-HttpListener</span></span>
<span data-ttu-id="af61b-124">Especifica o ouvinte HTTP de back-end para a regra de roteamento de solicitação criar.</span><span class="sxs-lookup"><span data-stu-id="af61b-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="af61b-125">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="af61b-125">-HttpListenerId</span></span>
<span data-ttu-id="af61b-126">Especifica a ID do ouvinte HTTP de back-end para a regra de roteamento de solicitação criar.</span><span class="sxs-lookup"><span data-stu-id="af61b-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="af61b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="af61b-127">-Name</span></span>
<span data-ttu-id="af61b-128">Especifica o nome da regra de roteamento de solicitação que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="af61b-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="af61b-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="af61b-129">-RedirectConfiguration</span></span>
<span data-ttu-id="af61b-130">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="af61b-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="af61b-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="af61b-132">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="af61b-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="af61b-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af61b-133">-RewriteRuleSet</span></span>
<span data-ttu-id="af61b-134">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="af61b-134">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="af61b-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="af61b-136">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af61b-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="af61b-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="af61b-137">-RuleType</span></span>
<span data-ttu-id="af61b-138">Especifica o tipo da regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="af61b-138">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="af61b-139">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af61b-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="af61b-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="af61b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af61b-141">CommonParameters</span></span>
<span data-ttu-id="af61b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af61b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af61b-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af61b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af61b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af61b-144">INPUTS</span></span>

### <span data-ttu-id="af61b-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af61b-145">None</span></span>

## <span data-ttu-id="af61b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af61b-146">OUTPUTS</span></span>

### <span data-ttu-id="af61b-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="af61b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af61b-148">NOTES</span></span>

## <span data-ttu-id="af61b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af61b-149">RELATED LINKS</span></span>

[<span data-ttu-id="af61b-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="af61b-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="af61b-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="af61b-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af61b-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


