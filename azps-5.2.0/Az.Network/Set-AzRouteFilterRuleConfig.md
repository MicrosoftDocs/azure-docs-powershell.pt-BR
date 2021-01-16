---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258201"
---
# <span data-ttu-id="6b687-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b687-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="6b687-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b687-102">SYNOPSIS</span></span>
<span data-ttu-id="6b687-103">Modifica a regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="6b687-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="6b687-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b687-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b687-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b687-105">DESCRIPTION</span></span>
<span data-ttu-id="6b687-106">O cmdlet **set-AzRouteFilterRuleConfig** modifica a regra de filtro de rota de um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="6b687-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="6b687-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b687-107">EXAMPLES</span></span>

### <span data-ttu-id="6b687-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b687-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="6b687-109">O primeiro comando obtém o filtro de rota chamado RouteFilter01 e o armazena na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="6b687-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="6b687-110">O segundo comando modifica a regra de filtro de rota chamada Rule01 e armazena o filtro de rota atualizado na variável $rf.</span><span class="sxs-lookup"><span data-stu-id="6b687-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="6b687-111">O terceiro comando salva o filtro de rota atualizado.</span><span class="sxs-lookup"><span data-stu-id="6b687-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="6b687-112">OS</span><span class="sxs-lookup"><span data-stu-id="6b687-112">PARAMETERS</span></span>

### <span data-ttu-id="6b687-113">-Acesso</span><span class="sxs-lookup"><span data-stu-id="6b687-113">-Access</span></span>
<span data-ttu-id="6b687-114">O tipo de acesso da regra.</span><span class="sxs-lookup"><span data-stu-id="6b687-114">The access type of the rule.</span></span>
<span data-ttu-id="6b687-115">Os valores possíveis são: ' Allow ', ' Deny '</span><span class="sxs-lookup"><span data-stu-id="6b687-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="6b687-116">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="6b687-116">-CommunityList</span></span>
<span data-ttu-id="6b687-117">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="6b687-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="6b687-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b687-118">-DefaultProfile</span></span>
<span data-ttu-id="6b687-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b687-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b687-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6b687-120">-Force</span></span>
<span data-ttu-id="6b687-121">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="6b687-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6b687-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b687-122">-Name</span></span>
<span data-ttu-id="6b687-123">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="6b687-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="6b687-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-124">-RouteFilter</span></span>
<span data-ttu-id="6b687-125">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-125">The RouteFilter</span></span>

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

### <span data-ttu-id="6b687-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="6b687-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="6b687-127">O tipo de regra de filtro de rota da regra.</span><span class="sxs-lookup"><span data-stu-id="6b687-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="6b687-128">Os valores possíveis são: "Comunidade"</span><span class="sxs-lookup"><span data-stu-id="6b687-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="6b687-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b687-129">-Confirm</span></span>
<span data-ttu-id="6b687-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b687-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b687-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b687-131">-WhatIf</span></span>
<span data-ttu-id="6b687-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b687-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b687-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b687-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b687-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b687-134">CommonParameters</span></span>
<span data-ttu-id="6b687-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b687-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b687-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b687-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b687-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b687-137">INPUTS</span></span>

### <span data-ttu-id="6b687-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6b687-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b687-139">OUTPUTS</span></span>

### <span data-ttu-id="6b687-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6b687-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b687-141">NOTES</span></span>

## <span data-ttu-id="6b687-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b687-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b687-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b687-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6b687-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b687-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6b687-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b687-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6b687-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b687-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6b687-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6b687-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="6b687-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="6b687-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b687-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
