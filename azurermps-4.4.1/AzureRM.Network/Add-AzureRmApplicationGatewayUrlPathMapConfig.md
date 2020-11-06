---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 821f31ba8f42ff8a7b94839aad344a2f144353d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433080"
---
# <span data-ttu-id="010bf-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="010bf-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="010bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="010bf-102">SYNOPSIS</span></span>
<span data-ttu-id="010bf-103">Adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="010bf-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="010bf-104">SYNTAX</span></span>

### <span data-ttu-id="010bf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="010bf-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="010bf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="010bf-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="010bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="010bf-107">DESCRIPTION</span></span>
<span data-ttu-id="010bf-108">O cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** adiciona uma matriz de mapeamentos de caminho de URL a um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="010bf-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="010bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="010bf-109">EXAMPLES</span></span>

## <span data-ttu-id="010bf-110">OS</span><span class="sxs-lookup"><span data-stu-id="010bf-110">PARAMETERS</span></span>

### <span data-ttu-id="010bf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="010bf-111">-ApplicationGateway</span></span>
<span data-ttu-id="010bf-112">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="010bf-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="010bf-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="010bf-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="010bf-114">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="010bf-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="010bf-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="010bf-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="010bf-116">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="010bf-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="010bf-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="010bf-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="010bf-118">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="010bf-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="010bf-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="010bf-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="010bf-120">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="010bf-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="010bf-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="010bf-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="010bf-122">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="010bf-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="010bf-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="010bf-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="010bf-124">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="010bf-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="010bf-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="010bf-125">-Name</span></span>
<span data-ttu-id="010bf-126">Especifica o nome do mapa de caminho de URL que este cmdlet adiciona ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="010bf-126">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="010bf-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="010bf-127">-PathRules</span></span>
<span data-ttu-id="010bf-128">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="010bf-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="010bf-129">As regras de caminho são sigilosas de ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="010bf-129">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="010bf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010bf-130">-DefaultProfile</span></span>
<span data-ttu-id="010bf-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="010bf-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010bf-132">CommonParameters</span></span>
<span data-ttu-id="010bf-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010bf-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010bf-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="010bf-135">INPUTS</span></span>

### <span data-ttu-id="010bf-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="010bf-136">PSApplicationGateway</span></span>
<span data-ttu-id="010bf-137">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="010bf-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="010bf-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="010bf-138">OUTPUTS</span></span>

### <span data-ttu-id="010bf-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="010bf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="010bf-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="010bf-140">NOTES</span></span>

## <span data-ttu-id="010bf-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="010bf-141">RELATED LINKS</span></span>

[<span data-ttu-id="010bf-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="010bf-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="010bf-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="010bf-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="010bf-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="010bf-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="010bf-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="010bf-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


