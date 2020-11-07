---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786084"
---
# <span data-ttu-id="44bbc-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="44bbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="44bbc-103">Cria uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44bbc-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44bbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44bbc-104">SYNTAX</span></span>

### <span data-ttu-id="44bbc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="44bbc-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44bbc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="44bbc-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44bbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="44bbc-108">**O cmdlet Add-AzureRmApplicationGatewayRequestRoutingRule** cria uma regra de roteamento de solicitação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="44bbc-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="44bbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="44bbc-110">Exemplo 1: criar uma regra de roteamento de solicitação para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="44bbc-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="44bbc-111">Esse comando cria uma regra básica de roteamento de solicitações chamada Rule01 e armazena o resultado na variável chamada $Rule.</span><span class="sxs-lookup"><span data-stu-id="44bbc-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="44bbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="44bbc-112">PARAMETERS</span></span>

### <span data-ttu-id="44bbc-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="44bbc-113">-BackendAddressPool</span></span>
<span data-ttu-id="44bbc-114">Especifica o pool de endereços back-end, como um objeto, para que a regra de roteamento de solicitação crie.</span><span class="sxs-lookup"><span data-stu-id="44bbc-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bbc-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="44bbc-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="44bbc-116">Especifica a ID do pool de endereços back-end da regra de roteamento de solicitação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="44bbc-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="44bbc-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44bbc-117">-BackendHttpSettings</span></span>
<span data-ttu-id="44bbc-118">Especifica as configurações HTTP de back-end, como um objeto, para que a regra de roteamento de solicitação crie.</span><span class="sxs-lookup"><span data-stu-id="44bbc-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bbc-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="44bbc-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="44bbc-120">Especifica a ID de configurações HTTP de back-end da regra de roteamento de solicitação a ser criada.</span><span class="sxs-lookup"><span data-stu-id="44bbc-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="44bbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44bbc-121">-DefaultProfile</span></span>
<span data-ttu-id="44bbc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44bbc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44bbc-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="44bbc-123">-HttpListener</span></span>
<span data-ttu-id="44bbc-124">Especifica o ouvinte HTTP de back-end para a regra de roteamento de solicitação criar.</span><span class="sxs-lookup"><span data-stu-id="44bbc-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="44bbc-125">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="44bbc-125">-HttpListenerId</span></span>
<span data-ttu-id="44bbc-126">Especifica a ID do ouvinte HTTP de back-end para a regra de roteamento de solicitação criar.</span><span class="sxs-lookup"><span data-stu-id="44bbc-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="44bbc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="44bbc-127">-Name</span></span>
<span data-ttu-id="44bbc-128">Especifica o nome da regra de roteamento de solicitação que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="44bbc-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="44bbc-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="44bbc-129">-RedirectConfiguration</span></span>
<span data-ttu-id="44bbc-130">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="44bbc-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bbc-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="44bbc-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="44bbc-132">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="44bbc-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="44bbc-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="44bbc-133">-RuleType</span></span>
<span data-ttu-id="44bbc-134">Especifica o tipo da regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="44bbc-134">Specifies type of the request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bbc-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="44bbc-135">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44bbc-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="44bbc-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="44bbc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44bbc-137">CommonParameters</span></span>
<span data-ttu-id="44bbc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44bbc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44bbc-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44bbc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44bbc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44bbc-140">INPUTS</span></span>

### <span data-ttu-id="44bbc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="44bbc-141">System.String</span></span>

## <span data-ttu-id="44bbc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44bbc-142">OUTPUTS</span></span>

### <span data-ttu-id="44bbc-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="44bbc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44bbc-144">NOTES</span></span>

## <span data-ttu-id="44bbc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44bbc-145">RELATED LINKS</span></span>

[<span data-ttu-id="44bbc-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="44bbc-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="44bbc-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="44bbc-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44bbc-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


