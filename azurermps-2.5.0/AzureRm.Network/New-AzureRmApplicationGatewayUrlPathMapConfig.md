---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: e43d5277566311fe77ee239d88e55f658aca8b40
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785316"
---
# <span data-ttu-id="2b537-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b537-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2b537-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b537-102">SYNOPSIS</span></span>
<span data-ttu-id="2b537-103">Cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="2b537-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b537-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b537-104">SYNTAX</span></span>

### <span data-ttu-id="2b537-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b537-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b537-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2b537-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b537-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b537-107">DESCRIPTION</span></span>
<span data-ttu-id="2b537-108">O cmdlet **New-AzureRmApplicationGatewayUrlPathMapConfig** cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="2b537-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2b537-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b537-109">EXAMPLES</span></span>

### <span data-ttu-id="2b537-110">Exemplo 1: criar uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="2b537-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="2b537-111">Esse comando cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="2b537-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2b537-112">OS</span><span class="sxs-lookup"><span data-stu-id="2b537-112">PARAMETERS</span></span>

### <span data-ttu-id="2b537-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b537-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="2b537-114">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="2b537-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="2b537-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2b537-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="2b537-116">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="2b537-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="2b537-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b537-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="2b537-118">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="2b537-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="2b537-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2b537-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="2b537-120">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="2b537-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="2b537-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b537-121">-DefaultProfile</span></span>
<span data-ttu-id="2b537-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b537-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b537-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b537-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="2b537-124">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2b537-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="2b537-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2b537-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="2b537-126">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2b537-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="2b537-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b537-127">-Name</span></span>
<span data-ttu-id="2b537-128">Especifica o nome do mapa de caminho de URL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2b537-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2b537-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="2b537-129">-PathRules</span></span>
<span data-ttu-id="2b537-130">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="2b537-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="2b537-131">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="2b537-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="2b537-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b537-132">CommonParameters</span></span>
<span data-ttu-id="2b537-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b537-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b537-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b537-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b537-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b537-135">INPUTS</span></span>

## <span data-ttu-id="2b537-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b537-136">OUTPUTS</span></span>

### <span data-ttu-id="2b537-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2b537-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="2b537-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b537-138">NOTES</span></span>

## <span data-ttu-id="2b537-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b537-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b537-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b537-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2b537-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b537-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2b537-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b537-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2b537-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2b537-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


