---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 395c02303ad5cf0c42c510511263e4a0201315ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603352"
---
# <span data-ttu-id="1bf8b-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1bf8b-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1bf8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bf8b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf8b-103">Define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bf8b-104">SYNTAX</span></span>

### <span data-ttu-id="1bf8b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf8b-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf8b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1bf8b-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf8b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bf8b-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf8b-108">O cmdlet **set-AzureRmApplicationGatewayUrlPathMapConfig** define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1bf8b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bf8b-109">EXAMPLES</span></span>

## <span data-ttu-id="1bf8b-110">OS</span><span class="sxs-lookup"><span data-stu-id="1bf8b-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf8b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf8b-111">-ApplicationGateway</span></span>
<span data-ttu-id="1bf8b-112">Especifica o gateway do aplicativo para o qual esse cmdlet define uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="1bf8b-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1bf8b-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="1bf8b-114">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1bf8b-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1bf8b-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="1bf8b-116">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="1bf8b-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1bf8b-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="1bf8b-118">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1bf8b-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1bf8b-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="1bf8b-120">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="1bf8b-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bf8b-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="1bf8b-122">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1bf8b-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1bf8b-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1bf8b-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="1bf8b-124">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1bf8b-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1bf8b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bf8b-125">-Name</span></span>
<span data-ttu-id="1bf8b-126">Especifica o nome do mapa de caminho de URL no qual este cmdlet define a configuração.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-126">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="1bf8b-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="1bf8b-127">-PathRules</span></span>
<span data-ttu-id="1bf8b-128">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="1bf8b-129">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-129">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="1bf8b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf8b-130">-DefaultProfile</span></span>
<span data-ttu-id="1bf8b-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf8b-132">CommonParameters</span></span>
<span data-ttu-id="1bf8b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf8b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf8b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf8b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bf8b-135">INPUTS</span></span>

### <span data-ttu-id="1bf8b-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf8b-136">PSApplicationGateway</span></span>
<span data-ttu-id="1bf8b-137">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1bf8b-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="1bf8b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bf8b-138">OUTPUTS</span></span>

### <span data-ttu-id="1bf8b-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf8b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bf8b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bf8b-140">NOTES</span></span>

## <span data-ttu-id="1bf8b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bf8b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1bf8b-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1bf8b-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1bf8b-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1bf8b-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1bf8b-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1bf8b-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1bf8b-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1bf8b-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


