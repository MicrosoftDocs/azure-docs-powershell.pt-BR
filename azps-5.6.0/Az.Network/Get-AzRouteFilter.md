---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 5ae145c79012a62ae5e46c14bd649b17460f8d3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885647"
---
# <span data-ttu-id="5232d-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5232d-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="5232d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5232d-102">SYNOPSIS</span></span>
<span data-ttu-id="5232d-103">Obtém um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="5232d-103">Gets a route filter.</span></span>

## <span data-ttu-id="5232d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5232d-104">SYNTAX</span></span>

### <span data-ttu-id="5232d-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="5232d-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5232d-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="5232d-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5232d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5232d-107">DESCRIPTION</span></span>
<span data-ttu-id="5232d-108">O cmdlet **Get-AzRouteFilter** obtém um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="5232d-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="5232d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5232d-109">EXAMPLES</span></span>

### <span data-ttu-id="5232d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5232d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="5232d-111">Este comando obtém o filtro de rota chamado RouteFilter01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5232d-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="5232d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5232d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="5232d-113">Este comando obtém todos os filtros de rota que começam com "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="5232d-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="5232d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5232d-114">PARAMETERS</span></span>

### <span data-ttu-id="5232d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5232d-115">-DefaultProfile</span></span>
<span data-ttu-id="5232d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5232d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5232d-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5232d-117">-ExpandResource</span></span>
<span data-ttu-id="5232d-118">A referência de recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="5232d-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5232d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5232d-119">-Name</span></span>
<span data-ttu-id="5232d-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5232d-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5232d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5232d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5232d-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5232d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5232d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5232d-123">CommonParameters</span></span>
<span data-ttu-id="5232d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5232d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5232d-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5232d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5232d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5232d-126">INPUTS</span></span>

### <span data-ttu-id="5232d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5232d-127">System.String</span></span>

## <span data-ttu-id="5232d-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5232d-128">OUTPUTS</span></span>

### <span data-ttu-id="5232d-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5232d-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5232d-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="5232d-130">NOTES</span></span>

## <span data-ttu-id="5232d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5232d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5232d-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5232d-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="5232d-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5232d-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="5232d-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5232d-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="5232d-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5232d-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5232d-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5232d-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5232d-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5232d-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5232d-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5232d-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="5232d-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5232d-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
