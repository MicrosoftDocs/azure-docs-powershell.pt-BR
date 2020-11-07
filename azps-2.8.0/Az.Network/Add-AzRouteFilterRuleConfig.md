---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: f73a41d313ccd41c60c2e59292b570e50876bd3a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772079"
---
# <span data-ttu-id="9bd0a-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bd0a-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="9bd0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd0a-103">Adiciona uma regra de filtro de rota a um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="9bd0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bd0a-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bd0a-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd0a-106">O cmdlet Add-AzRouteFilterRuleConfig adiciona uma regra de filtro de rota a um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="9bd0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bd0a-107">EXAMPLES</span></span>

### <span data-ttu-id="9bd0a-108">Exemplo 1: adicionar uma regra de filtro de rota a um filtro de rota</span><span class="sxs-lookup"><span data-stu-id="9bd0a-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="9bd0a-109">O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="9bd0a-110">O comando armazena o filtro na variável $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="9bd0a-111">OS</span><span class="sxs-lookup"><span data-stu-id="9bd0a-111">PARAMETERS</span></span>

### <span data-ttu-id="9bd0a-112">-Acesso</span><span class="sxs-lookup"><span data-stu-id="9bd0a-112">-Access</span></span>
<span data-ttu-id="9bd0a-113">Especifica o acesso da regra de filtro de rota, os valores válidos são Deny ou Allow.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="9bd0a-114">-CommunityList</span></span>
<span data-ttu-id="9bd0a-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="9bd0a-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd0a-116">-DefaultProfile</span></span>
<span data-ttu-id="9bd0a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd0a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9bd0a-118">-Force</span></span>
<span data-ttu-id="9bd0a-119">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="9bd0a-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bd0a-120">-Name</span></span>
<span data-ttu-id="9bd0a-121">Especifica um nome da regra de filtro de rota a ser adicionada ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="9bd0a-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-122">-RouteFilter</span></span>
<span data-ttu-id="9bd0a-123">Especifica o filtro de rota para o qual esse cmdlet adiciona uma regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="9bd0a-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="9bd0a-125">Especifica o tipo de regra do filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="9bd0a-126">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="9bd0a-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bd0a-127">-Confirm</span></span>
<span data-ttu-id="9bd0a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd0a-129">-WhatIf</span></span>
<span data-ttu-id="9bd0a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bd0a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd0a-132">CommonParameters</span></span>
<span data-ttu-id="9bd0a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd0a-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd0a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd0a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bd0a-135">INPUTS</span></span>

### <span data-ttu-id="9bd0a-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9bd0a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bd0a-137">OUTPUTS</span></span>

### <span data-ttu-id="9bd0a-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9bd0a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bd0a-139">NOTES</span></span>
<span data-ttu-id="9bd0a-140">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="9bd0a-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9bd0a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bd0a-141">RELATED LINKS</span></span>

[<span data-ttu-id="9bd0a-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bd0a-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bd0a-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bd0a-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bd0a-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bd0a-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bd0a-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9bd0a-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="9bd0a-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="9bd0a-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="9bd0a-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="9bd0a-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9bd0a-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
