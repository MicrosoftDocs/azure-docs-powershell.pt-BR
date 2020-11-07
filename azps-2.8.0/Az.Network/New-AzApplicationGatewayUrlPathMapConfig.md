---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1e9a97d01fd42bae636d93311b41bc6150394d9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771907"
---
# <span data-ttu-id="527fc-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="527fc-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="527fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="527fc-102">SYNOPSIS</span></span>
<span data-ttu-id="527fc-103">Cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="527fc-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="527fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="527fc-104">SYNTAX</span></span>

### <span data-ttu-id="527fc-105">BackendSetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="527fc-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="527fc-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="527fc-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527fc-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="527fc-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527fc-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="527fc-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="527fc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="527fc-109">DESCRIPTION</span></span>
<span data-ttu-id="527fc-110">O cmdlet **New-AzApplicationGatewayUrlPathMapConfig** cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="527fc-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="527fc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="527fc-111">EXAMPLES</span></span>

### <span data-ttu-id="527fc-112">Exemplo 1: criar uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="527fc-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="527fc-113">Esse comando cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="527fc-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="527fc-114">OS</span><span class="sxs-lookup"><span data-stu-id="527fc-114">PARAMETERS</span></span>

### <span data-ttu-id="527fc-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="527fc-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="527fc-116">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="527fc-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="527fc-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="527fc-118">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="527fc-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="527fc-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="527fc-120">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="527fc-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="527fc-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="527fc-122">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="527fc-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527fc-123">-DefaultProfile</span></span>
<span data-ttu-id="527fc-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="527fc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="527fc-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="527fc-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="527fc-126">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="527fc-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="527fc-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="527fc-128">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="527fc-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="527fc-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="527fc-130">Conjunto de regras de regravação padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="527fc-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="527fc-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="527fc-132">ID do conjunto de regras de regravação padrão do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="527fc-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="527fc-133">-Name</span></span>
<span data-ttu-id="527fc-134">Especifica o nome do mapa de caminho de URL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="527fc-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="527fc-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="527fc-135">-PathRules</span></span>
<span data-ttu-id="527fc-136">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="527fc-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="527fc-137">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="527fc-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527fc-138">CommonParameters</span></span>
<span data-ttu-id="527fc-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527fc-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527fc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527fc-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="527fc-141">INPUTS</span></span>

### <span data-ttu-id="527fc-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="527fc-142">None</span></span>

## <span data-ttu-id="527fc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="527fc-143">OUTPUTS</span></span>

### <span data-ttu-id="527fc-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="527fc-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="527fc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="527fc-145">NOTES</span></span>

## <span data-ttu-id="527fc-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="527fc-146">RELATED LINKS</span></span>

[<span data-ttu-id="527fc-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="527fc-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="527fc-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="527fc-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="527fc-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="527fc-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="527fc-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="527fc-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

