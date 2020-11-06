---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: c555ce87f746d7f976add4fc49fb14b661a276d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441263"
---
# <span data-ttu-id="bb75f-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb75f-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bb75f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb75f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb75f-103">Adiciona uma regra de filtro de rota a um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bb75f-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb75f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb75f-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb75f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb75f-105">DESCRIPTION</span></span>
<span data-ttu-id="bb75f-106">O cmdlet Add-AzureRmRouteFilterRuleConfig adiciona uma regra de filtro de rota a um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb75f-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="bb75f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb75f-107">EXAMPLES</span></span>

### <span data-ttu-id="bb75f-108">Exemplo 1: adicionar uma regra de filtro de rota a um filtro de rota</span><span class="sxs-lookup"><span data-stu-id="bb75f-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="bb75f-109">O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="bb75f-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="bb75f-110">O comando armazena o filtro na variável $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="bb75f-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="bb75f-111">OS</span><span class="sxs-lookup"><span data-stu-id="bb75f-111">PARAMETERS</span></span>

### <span data-ttu-id="bb75f-112">-Acesso</span><span class="sxs-lookup"><span data-stu-id="bb75f-112">-Access</span></span>
<span data-ttu-id="bb75f-113">Especifica o acesso da regra de filtro de rota, os valores válidos são Deny ou Allow.</span><span class="sxs-lookup"><span data-stu-id="bb75f-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="bb75f-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="bb75f-114">-CommunityList</span></span>
<span data-ttu-id="bb75f-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="bb75f-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="bb75f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb75f-116">-DefaultProfile</span></span>
<span data-ttu-id="bb75f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb75f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb75f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bb75f-118">-Force</span></span>
<span data-ttu-id="bb75f-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="bb75f-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="bb75f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb75f-120">-Name</span></span>
<span data-ttu-id="bb75f-121">Especifica um nome da regra de filtro de rota a ser adicionada ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bb75f-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="bb75f-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb75f-122">-RouteFilter</span></span>
<span data-ttu-id="bb75f-123">Especifica o filtro de rota para o qual esse cmdlet adiciona uma regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bb75f-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="bb75f-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="bb75f-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="bb75f-125">Especifica o tipo de regra do filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="bb75f-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="bb75f-126">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="bb75f-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="bb75f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb75f-127">-Confirm</span></span>
<span data-ttu-id="bb75f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb75f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb75f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb75f-129">-WhatIf</span></span>
<span data-ttu-id="bb75f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb75f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb75f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb75f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb75f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb75f-132">CommonParameters</span></span>
<span data-ttu-id="bb75f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb75f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb75f-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb75f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb75f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb75f-135">INPUTS</span></span>

### <span data-ttu-id="bb75f-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb75f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="bb75f-137">Parâmetros: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb75f-137">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="bb75f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb75f-138">OUTPUTS</span></span>

### <span data-ttu-id="bb75f-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb75f-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bb75f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb75f-140">NOTES</span></span>
<span data-ttu-id="bb75f-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="bb75f-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bb75f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb75f-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb75f-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb75f-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="bb75f-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb75f-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="bb75f-145">New-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="bb75f-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="bb75f-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="bb75f-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="bb75f-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="bb75f-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="bb75f-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb75f-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
