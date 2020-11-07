---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775646"
---
# <span data-ttu-id="e5835-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5835-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e5835-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5835-102">SYNOPSIS</span></span>
<span data-ttu-id="e5835-103">Adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e5835-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e5835-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5835-104">SYNTAX</span></span>

### <span data-ttu-id="e5835-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5835-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5835-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5835-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5835-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5835-107">DESCRIPTION</span></span>
<span data-ttu-id="e5835-108">O cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e5835-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="e5835-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5835-109">EXAMPLES</span></span>

### <span data-ttu-id="e5835-110">1:</span><span class="sxs-lookup"><span data-stu-id="e5835-110">1:</span></span>
```

```

## <span data-ttu-id="e5835-111">OS</span><span class="sxs-lookup"><span data-stu-id="e5835-111">PARAMETERS</span></span>

### <span data-ttu-id="e5835-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5835-112">-ApplicationGateway</span></span>
<span data-ttu-id="e5835-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="e5835-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="e5835-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e5835-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e5835-115">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="e5835-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e5835-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e5835-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e5835-117">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="e5835-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e5835-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5835-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e5835-119">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="e5835-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e5835-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e5835-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e5835-121">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="e5835-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e5835-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5835-122">-DefaultProfile</span></span>
<span data-ttu-id="e5835-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5835-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5835-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5835-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e5835-125">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e5835-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e5835-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e5835-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e5835-127">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e5835-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e5835-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5835-128">-Name</span></span>
<span data-ttu-id="e5835-129">Especifica o nome do mapa de caminho de URL que este cmdlet adiciona ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e5835-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="e5835-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e5835-130">-PathRules</span></span>
<span data-ttu-id="e5835-131">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="e5835-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="e5835-132">As regras de caminho são sigilosas de ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="e5835-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e5835-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5835-133">CommonParameters</span></span>
<span data-ttu-id="e5835-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5835-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5835-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5835-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5835-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5835-136">INPUTS</span></span>

### <span data-ttu-id="e5835-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5835-137">PSApplicationGateway</span></span>
<span data-ttu-id="e5835-138">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e5835-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e5835-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5835-139">OUTPUTS</span></span>

### <span data-ttu-id="e5835-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5835-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5835-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5835-141">NOTES</span></span>

## <span data-ttu-id="e5835-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5835-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5835-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5835-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e5835-144">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5835-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e5835-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5835-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e5835-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e5835-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


