---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ebb73225a8afa7bb4c1061326aa9262dd46d9dc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893138"
---
# <span data-ttu-id="e4ad7-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e4ad7-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e4ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ad7-103">Cria uma matriz de mapeamentos de caminho de URL para um pool de servidores de back-end.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e4ad7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4ad7-104">SYNTAX</span></span>

### <span data-ttu-id="e4ad7-105">BackendSetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4ad7-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4ad7-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4ad7-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="e4ad7-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4ad7-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4ad7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4ad7-109">DESCRIPTION</span></span>
<span data-ttu-id="e4ad7-110">O cmdlet **New-AzApplicationGatewayUrlPathMapConfig** cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e4ad7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-111">EXAMPLES</span></span>

### <span data-ttu-id="e4ad7-112">Exemplo 1: Criar uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="e4ad7-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="e4ad7-113">Este comando cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e4ad7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-114">PARAMETERS</span></span>

### <span data-ttu-id="e4ad7-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4ad7-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e4ad7-116">Especifica o pool de endereços de back-end padrão a ser roteado no caso de nenhuma das regras especificadas no *parâmetro pathRules* corresponder.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e4ad7-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e4ad7-118">Especifica a ID padrão do pool de endereços de back-end.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e4ad7-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e4ad7-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e4ad7-120">Especifica as configurações HTTP de back-end padrão a ser usadas no caso de nenhuma das regras especificadas no *parâmetro pathRules* corresponder.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e4ad7-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e4ad7-122">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e4ad7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ad7-123">-DefaultProfile</span></span>
<span data-ttu-id="e4ad7-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ad7-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4ad7-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e4ad7-126">RedirectConfiguration padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e4ad7-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e4ad7-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e4ad7-128">ID do gateway de aplicativo RedirectConfiguration padrão</span><span class="sxs-lookup"><span data-stu-id="e4ad7-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e4ad7-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4ad7-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="e4ad7-130">Conjunto de regras de regra de regra padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e4ad7-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="e4ad7-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e4ad7-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="e4ad7-132">ID do conjunto de regras de regra de regra padrão do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e4ad7-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="e4ad7-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e4ad7-133">-Name</span></span>
<span data-ttu-id="e4ad7-134">Especifica o nome do mapa do caminho da URL que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e4ad7-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e4ad7-135">-PathRules</span></span>
<span data-ttu-id="e4ad7-136">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="e4ad7-137">Observe que as regras de caminho são confidenciais de ordem, elas são aplicadas para que sejam especificadas.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e4ad7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ad7-138">CommonParameters</span></span>
<span data-ttu-id="e4ad7-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ad7-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ad7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ad7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-141">INPUTS</span></span>

### <span data-ttu-id="e4ad7-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e4ad7-142">None</span></span>

## <span data-ttu-id="e4ad7-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-143">OUTPUTS</span></span>

### <span data-ttu-id="e4ad7-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e4ad7-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="e4ad7-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4ad7-145">NOTES</span></span>

## <span data-ttu-id="e4ad7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-146">RELATED LINKS</span></span>

[<span data-ttu-id="e4ad7-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e4ad7-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e4ad7-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e4ad7-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e4ad7-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e4ad7-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e4ad7-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e4ad7-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


