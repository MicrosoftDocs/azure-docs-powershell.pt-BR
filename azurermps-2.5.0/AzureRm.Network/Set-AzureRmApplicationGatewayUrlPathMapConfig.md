---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786077"
---
# <span data-ttu-id="26cef-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26cef-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="26cef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26cef-102">SYNOPSIS</span></span>
<span data-ttu-id="26cef-103">Define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26cef-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26cef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26cef-104">SYNTAX</span></span>

### <span data-ttu-id="26cef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26cef-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26cef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26cef-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26cef-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26cef-107">DESCRIPTION</span></span>
<span data-ttu-id="26cef-108">O cmdlet **set-AzureRmApplicationGatewayUrlPathMapConfig** define a configuração de uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26cef-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26cef-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26cef-109">EXAMPLES</span></span>

### <span data-ttu-id="26cef-110">1:</span><span class="sxs-lookup"><span data-stu-id="26cef-110">1:</span></span>
```

```

## <span data-ttu-id="26cef-111">OS</span><span class="sxs-lookup"><span data-stu-id="26cef-111">PARAMETERS</span></span>

### <span data-ttu-id="26cef-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26cef-112">-ApplicationGateway</span></span>
<span data-ttu-id="26cef-113">Especifica o gateway do aplicativo para o qual esse cmdlet define uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="26cef-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="26cef-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="26cef-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="26cef-115">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="26cef-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="26cef-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="26cef-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="26cef-117">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="26cef-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="26cef-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="26cef-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="26cef-119">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="26cef-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="26cef-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="26cef-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="26cef-121">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="26cef-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="26cef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cef-122">-DefaultProfile</span></span>
<span data-ttu-id="26cef-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26cef-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26cef-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26cef-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="26cef-125">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="26cef-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="26cef-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26cef-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="26cef-127">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="26cef-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="26cef-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="26cef-128">-Name</span></span>
<span data-ttu-id="26cef-129">Especifica o nome do mapa de caminho de URL no qual este cmdlet define a configuração.</span><span class="sxs-lookup"><span data-stu-id="26cef-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="26cef-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="26cef-130">-PathRules</span></span>
<span data-ttu-id="26cef-131">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="26cef-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="26cef-132">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="26cef-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="26cef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cef-133">CommonParameters</span></span>
<span data-ttu-id="26cef-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26cef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cef-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26cef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26cef-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26cef-136">INPUTS</span></span>

### <span data-ttu-id="26cef-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26cef-137">PSApplicationGateway</span></span>
<span data-ttu-id="26cef-138">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="26cef-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="26cef-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26cef-139">OUTPUTS</span></span>

### <span data-ttu-id="26cef-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26cef-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26cef-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26cef-141">NOTES</span></span>

## <span data-ttu-id="26cef-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26cef-142">RELATED LINKS</span></span>

[<span data-ttu-id="26cef-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26cef-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26cef-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26cef-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26cef-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26cef-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26cef-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26cef-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


