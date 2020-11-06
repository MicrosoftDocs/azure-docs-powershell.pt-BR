---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 727df25a789720def7b16620869843ca560c513e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599972"
---
# <span data-ttu-id="14106-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14106-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="14106-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14106-102">SYNOPSIS</span></span>
<span data-ttu-id="14106-103">Modifica a regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="14106-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="14106-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14106-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14106-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14106-105">DESCRIPTION</span></span>
<span data-ttu-id="14106-106">O cmdlet **set-AzRouteFilterRuleConfig** modifica a regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="14106-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="14106-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14106-107">EXAMPLES</span></span>

### <span data-ttu-id="14106-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14106-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="14106-109">O primeiro comando obtém o filtro de rota chamado RouteFilter01 e o armazena na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="14106-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="14106-110">O segundo comando modifica a regra de filtro de rota chamada Rule01 e armazena o filtro de rota atualizado na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="14106-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="14106-111">O terceiro comando salva o filtro de rota atualizado.</span><span class="sxs-lookup"><span data-stu-id="14106-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="14106-112">OS</span><span class="sxs-lookup"><span data-stu-id="14106-112">PARAMETERS</span></span>

### <span data-ttu-id="14106-113">-Acesso</span><span class="sxs-lookup"><span data-stu-id="14106-113">-Access</span></span>
<span data-ttu-id="14106-114">O tipo de acesso da regra.</span><span class="sxs-lookup"><span data-stu-id="14106-114">The access type of the rule.</span></span>
<span data-ttu-id="14106-115">Os valores possíveis são: ' Allow ', ' Deny '</span><span class="sxs-lookup"><span data-stu-id="14106-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="14106-116">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="14106-116">-CommunityList</span></span>
<span data-ttu-id="14106-117">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="14106-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="14106-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14106-118">-DefaultProfile</span></span>
<span data-ttu-id="14106-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14106-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14106-120">-Force</span><span class="sxs-lookup"><span data-stu-id="14106-120">-Force</span></span>
<span data-ttu-id="14106-121">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="14106-121">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="14106-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="14106-122">-Name</span></span>
<span data-ttu-id="14106-123">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="14106-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="14106-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-124">-RouteFilter</span></span>
<span data-ttu-id="14106-125">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-125">The RouteFilter</span></span>

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

### <span data-ttu-id="14106-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="14106-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="14106-127">O tipo de regra de filtro de rota da regra.</span><span class="sxs-lookup"><span data-stu-id="14106-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="14106-128">Os valores possíveis são: "Comunidade"</span><span class="sxs-lookup"><span data-stu-id="14106-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="14106-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14106-129">-Confirm</span></span>
<span data-ttu-id="14106-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14106-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14106-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14106-131">-WhatIf</span></span>
<span data-ttu-id="14106-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14106-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14106-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14106-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14106-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14106-134">CommonParameters</span></span>
<span data-ttu-id="14106-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14106-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14106-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14106-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14106-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14106-137">INPUTS</span></span>

### <span data-ttu-id="14106-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="14106-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14106-139">OUTPUTS</span></span>

### <span data-ttu-id="14106-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="14106-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14106-141">NOTES</span></span>

## <span data-ttu-id="14106-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14106-142">RELATED LINKS</span></span>

[<span data-ttu-id="14106-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14106-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="14106-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14106-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="14106-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14106-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="14106-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14106-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="14106-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="14106-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="14106-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="14106-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14106-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
