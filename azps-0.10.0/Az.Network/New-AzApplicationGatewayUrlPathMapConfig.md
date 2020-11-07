---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775409"
---
# <span data-ttu-id="52fec-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="52fec-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="52fec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52fec-102">SYNOPSIS</span></span>
<span data-ttu-id="52fec-103">Cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="52fec-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="52fec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52fec-104">SYNTAX</span></span>

### <span data-ttu-id="52fec-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="52fec-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52fec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="52fec-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52fec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52fec-107">DESCRIPTION</span></span>
<span data-ttu-id="52fec-108">O cmdlet **New-AzApplicationGatewayUrlPathMapConfig** cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="52fec-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="52fec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52fec-109">EXAMPLES</span></span>

### <span data-ttu-id="52fec-110">Exemplo 1: criar uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="52fec-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="52fec-111">Esse comando cria uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="52fec-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="52fec-112">OS</span><span class="sxs-lookup"><span data-stu-id="52fec-112">PARAMETERS</span></span>

### <span data-ttu-id="52fec-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="52fec-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="52fec-114">Especifica o pool de endereços de back-end padrão a ser roteado em caso de nenhuma das regras especificadas no parâmetro *pathRules* correspondente.</span><span class="sxs-lookup"><span data-stu-id="52fec-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="52fec-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="52fec-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="52fec-116">Especifica a ID do pool de endereços de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="52fec-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="52fec-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="52fec-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="52fec-118">Especifica as configurações HTTP de back-end padrão a serem usadas caso nenhuma das regras especificadas no parâmetro *pathRules* CORRESP.</span><span class="sxs-lookup"><span data-stu-id="52fec-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="52fec-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="52fec-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="52fec-120">Especifica a ID de configurações HTTP de back-end padrão.</span><span class="sxs-lookup"><span data-stu-id="52fec-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="52fec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fec-121">-DefaultProfile</span></span>
<span data-ttu-id="52fec-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52fec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fec-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="52fec-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="52fec-124">RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="52fec-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="52fec-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="52fec-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="52fec-126">ID da RedirectConfiguration padrão do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="52fec-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="52fec-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="52fec-127">-Name</span></span>
<span data-ttu-id="52fec-128">Especifica o nome do mapa de caminho de URL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="52fec-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="52fec-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="52fec-129">-PathRules</span></span>
<span data-ttu-id="52fec-130">Especifica uma lista de regras de caminho.</span><span class="sxs-lookup"><span data-stu-id="52fec-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="52fec-131">Observe que as regras de caminho são confidenciais da ordem, elas são aplicadas na ordem em que são especificadas.</span><span class="sxs-lookup"><span data-stu-id="52fec-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="52fec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fec-132">CommonParameters</span></span>
<span data-ttu-id="52fec-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fec-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fec-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fec-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52fec-135">INPUTS</span></span>

## <span data-ttu-id="52fec-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52fec-136">OUTPUTS</span></span>

### <span data-ttu-id="52fec-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="52fec-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="52fec-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52fec-138">NOTES</span></span>

## <span data-ttu-id="52fec-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52fec-139">RELATED LINKS</span></span>

[<span data-ttu-id="52fec-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="52fec-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="52fec-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="52fec-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="52fec-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="52fec-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="52fec-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="52fec-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


