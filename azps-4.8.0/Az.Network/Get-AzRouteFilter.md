---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110541"
---
# <span data-ttu-id="326f7-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="326f7-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="326f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="326f7-102">SYNOPSIS</span></span>
<span data-ttu-id="326f7-103">Obtém um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="326f7-103">Gets a route filter.</span></span>

## <span data-ttu-id="326f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="326f7-104">SYNTAX</span></span>

### <span data-ttu-id="326f7-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="326f7-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="326f7-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="326f7-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326f7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="326f7-107">DESCRIPTION</span></span>
<span data-ttu-id="326f7-108">O cmdlet **Get-AzRouteFilter** Obtém um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="326f7-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="326f7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="326f7-109">EXAMPLES</span></span>

### <span data-ttu-id="326f7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="326f7-110">Example 1</span></span>
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

<span data-ttu-id="326f7-111">Esse comando obtém o filtro de rota chamado RouteFilter01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="326f7-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="326f7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="326f7-112">Example 2</span></span>
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

<span data-ttu-id="326f7-113">Esse comando obtém todos os filtros de rota que começam com "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="326f7-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="326f7-114">OS</span><span class="sxs-lookup"><span data-stu-id="326f7-114">PARAMETERS</span></span>

### <span data-ttu-id="326f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326f7-115">-DefaultProfile</span></span>
<span data-ttu-id="326f7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="326f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326f7-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="326f7-117">-ExpandResource</span></span>
<span data-ttu-id="326f7-118">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="326f7-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="326f7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="326f7-119">-Name</span></span>
<span data-ttu-id="326f7-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="326f7-120">The resource name.</span></span>

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

### <span data-ttu-id="326f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="326f7-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="326f7-122">The resource group name.</span></span>

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

### <span data-ttu-id="326f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326f7-123">CommonParameters</span></span>
<span data-ttu-id="326f7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326f7-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="326f7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326f7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="326f7-126">INPUTS</span></span>

### <span data-ttu-id="326f7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="326f7-127">System.String</span></span>

## <span data-ttu-id="326f7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="326f7-128">OUTPUTS</span></span>

### <span data-ttu-id="326f7-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="326f7-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="326f7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="326f7-130">NOTES</span></span>

## <span data-ttu-id="326f7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="326f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="326f7-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="326f7-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="326f7-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="326f7-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="326f7-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="326f7-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="326f7-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="326f7-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="326f7-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="326f7-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="326f7-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="326f7-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="326f7-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="326f7-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="326f7-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="326f7-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
