---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7acb8ccef79d24846c01978016ac6ec4e9a0a058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602256"
---
# <span data-ttu-id="622e3-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="622e3-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="622e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="622e3-102">SYNOPSIS</span></span>
<span data-ttu-id="622e3-103">Cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="622e3-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="622e3-104">SYNTAX</span></span>

### <span data-ttu-id="622e3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="622e3-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="622e3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="622e3-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622e3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="622e3-107">DESCRIPTION</span></span>
<span data-ttu-id="622e3-108">O cmdlet **New-AzureRmApplicationGatewayUrlPathMapConfig** cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="622e3-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="622e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="622e3-109">EXAMPLES</span></span>

### <span data-ttu-id="622e3-110">Exemplo 1: criar uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="622e3-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="622e3-111">Esse comando cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="622e3-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="622e3-112">OS</span><span class="sxs-lookup"><span data-stu-id="622e3-112">PARAMETERS</span></span>

### <span data-ttu-id="622e3-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="622e3-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="622e3-114">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="622e3-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="622e3-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="622e3-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="622e3-116">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="622e3-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="622e3-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="622e3-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="622e3-118">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="622e3-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="622e3-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="622e3-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="622e3-120">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="622e3-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="622e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622e3-121">-DefaultProfile</span></span>
<span data-ttu-id="622e3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="622e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622e3-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="622e3-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="622e3-124">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="622e3-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="622e3-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="622e3-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="622e3-126">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="622e3-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="622e3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="622e3-127">-Name</span></span>
<span data-ttu-id="622e3-128">Especifica o nome do mapa de caminho de URL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="622e3-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="622e3-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="622e3-129">-PathRules</span></span>
<span data-ttu-id="622e3-130">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="622e3-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="622e3-131">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="622e3-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="622e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622e3-132">CommonParameters</span></span>
<span data-ttu-id="622e3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622e3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622e3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="622e3-135">INPUTS</span></span>

### <span data-ttu-id="622e3-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="622e3-136">None</span></span>
<span data-ttu-id="622e3-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="622e3-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="622e3-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="622e3-138">OUTPUTS</span></span>

### <span data-ttu-id="622e3-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="622e3-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="622e3-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="622e3-140">NOTES</span></span>

## <span data-ttu-id="622e3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="622e3-141">RELATED LINKS</span></span>

[<span data-ttu-id="622e3-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="622e3-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="622e3-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="622e3-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="622e3-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="622e3-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="622e3-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="622e3-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


