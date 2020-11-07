---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785737"
---
# <span data-ttu-id="e981e-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e981e-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e981e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e981e-102">SYNOPSIS</span></span>
<span data-ttu-id="e981e-103">Adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e981e-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e981e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e981e-104">SYNTAX</span></span>

### <span data-ttu-id="e981e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e981e-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e981e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e981e-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e981e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e981e-107">DESCRIPTION</span></span>
<span data-ttu-id="e981e-108">O cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e981e-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="e981e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e981e-109">EXAMPLES</span></span>

### <span data-ttu-id="e981e-110">1:</span><span class="sxs-lookup"><span data-stu-id="e981e-110">1:</span></span>
```

```

## <span data-ttu-id="e981e-111">OS</span><span class="sxs-lookup"><span data-stu-id="e981e-111">PARAMETERS</span></span>

### <span data-ttu-id="e981e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e981e-112">-ApplicationGateway</span></span>
<span data-ttu-id="e981e-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="e981e-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="e981e-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e981e-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e981e-115">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="e981e-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e981e-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e981e-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e981e-117">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="e981e-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e981e-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e981e-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e981e-119">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="e981e-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e981e-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e981e-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e981e-121">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="e981e-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e981e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e981e-122">-DefaultProfile</span></span>
<span data-ttu-id="e981e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e981e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e981e-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e981e-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e981e-125">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e981e-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e981e-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e981e-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e981e-127">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e981e-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e981e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e981e-128">-Name</span></span>
<span data-ttu-id="e981e-129">Especifica o nome do mapa de caminho de URL que este cmdlet adiciona ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e981e-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="e981e-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e981e-130">-PathRules</span></span>
<span data-ttu-id="e981e-131">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="e981e-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="e981e-132">As regras de caminho são sigilosas de ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="e981e-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e981e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e981e-133">CommonParameters</span></span>
<span data-ttu-id="e981e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e981e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e981e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e981e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e981e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e981e-136">INPUTS</span></span>

### <span data-ttu-id="e981e-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e981e-137">PSApplicationGateway</span></span>
<span data-ttu-id="e981e-138">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e981e-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e981e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e981e-139">OUTPUTS</span></span>

### <span data-ttu-id="e981e-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e981e-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e981e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e981e-141">NOTES</span></span>

## <span data-ttu-id="e981e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e981e-142">RELATED LINKS</span></span>

[<span data-ttu-id="e981e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e981e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e981e-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e981e-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e981e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e981e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e981e-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e981e-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


