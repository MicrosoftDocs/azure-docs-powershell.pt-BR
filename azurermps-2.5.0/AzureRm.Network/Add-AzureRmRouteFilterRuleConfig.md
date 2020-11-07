---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786498"
---
# <span data-ttu-id="2b6c0-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b6c0-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="2b6c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6c0-103">Adiciona uma regra de filtro de rota a um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b6c0-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b6c0-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6c0-106">O cmdlet Add-AzureRmRouteFilterRuleConfig adiciona uma regra de filtro de rota a um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="2b6c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b6c0-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6c0-108">--------------------------Exemplo 1: adicionar uma regra de filtro de rota a um filtro de rota--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b6c0-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="2b6c0-109">O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="2b6c0-110">O comando armazena o filtro na variável $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="2b6c0-111">OS</span><span class="sxs-lookup"><span data-stu-id="2b6c0-111">PARAMETERS</span></span>

### <span data-ttu-id="2b6c0-112">-Acesso</span><span class="sxs-lookup"><span data-stu-id="2b6c0-112">-Access</span></span>
<span data-ttu-id="2b6c0-113">Especifica o acesso da regra de filtro de rota, os valores válidos são Deny ou Allow.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="2b6c0-114">-CommunityList</span></span>
<span data-ttu-id="2b6c0-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="2b6c0-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6c0-116">-DefaultProfile</span></span>
<span data-ttu-id="2b6c0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b6c0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2b6c0-118">-Force</span></span>
<span data-ttu-id="2b6c0-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="2b6c0-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b6c0-120">-Name</span></span>
<span data-ttu-id="2b6c0-121">Especifica um nome da regra de filtro de rota a ser adicionada ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="2b6c0-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b6c0-122">-RouteFilter</span></span>
<span data-ttu-id="2b6c0-123">Especifica o filtro de rota para o qual esse cmdlet adiciona uma regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="2b6c0-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="2b6c0-125">Especifica o tipo de regra do filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="2b6c0-126">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="2b6c0-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b6c0-127">-Confirm</span></span>
<span data-ttu-id="2b6c0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6c0-129">-WhatIf</span></span>
<span data-ttu-id="2b6c0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b6c0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6c0-132">CommonParameters</span></span>
<span data-ttu-id="2b6c0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6c0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6c0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b6c0-135">INPUTS</span></span>

### <span data-ttu-id="2b6c0-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b6c0-136">PSRouteFilter</span></span>
<span data-ttu-id="2b6c0-137">O parâmetro ' RouteFilter ' aceita o valor do tipo ' PSRouteFilter ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2b6c0-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="2b6c0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b6c0-138">OUTPUTS</span></span>

### <span data-ttu-id="2b6c0-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b6c0-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2b6c0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b6c0-140">NOTES</span></span>
<span data-ttu-id="2b6c0-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="2b6c0-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2b6c0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b6c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b6c0-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b6c0-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="2b6c0-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b6c0-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="2b6c0-145">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2b6c0-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

